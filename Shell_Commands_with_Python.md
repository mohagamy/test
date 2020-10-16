# How to Execute Shell Commands with Python

## `os` Module
you can’t get the resulting output as a variable.

```python
import os
os.system('ls -l') 
```

```python
import os
stream = os.popen('echo Returned output')
output = stream.read()
```

## `subprocess` Module

- `subprocess.Popen`
you are not able to pipe commands

```python
import subprocess, PIPE
process = subprocess.Popen(['echo', 'More output'], stdout=PIPE, stderr=PIPE) 
stdout, stderr = process.communicate()
```

or

```python
with open('test.txt', 'w') as f:
    process = subprocess.Popen(['ls', '-l'], stdout=f)
```
the output is of type bytes, so 'stdout.decode('utf-8')' or add 'universal_newlines=True' when calling subprocess.Popen.

check the status in realtime 

```python
process = subprocess.Popen(['ping', '-c 4', 'python.org'], 
                           stdout=subprocess.PIPE,
                           universal_newlines=True)

while True:
    output = process.stdout.readline()
    print(output.strip())
    # Do something else
    return_code = process.poll()
    if return_code is not None:
        print('RETURN CODE', return_code)
        # Process has finished, read rest of the output 
        for output in process.stdout.readlines():
            print(output.strip())
        break
```
You can use the `.poll()` function to check the return code of the process. 

Also note, that you won’t need quotations for arguments with spaces in between like '\"More output\"'. 

If you are unsure how to tokenize the arguments from the command, you can use the `shlex.split()` function:

```python
import shlex
shlex.split("/bin/prog -i data.txt -o \"more data.txt\"")
['/bin/prog', '-i', 'data.txt', '-o', 'more data.txt']
```

- `subprocess.call()`
You have also the `subprocess.call()` function to your disposal which works like the Popen class, but it waits until the command completes and gives you the return code as in `return_code = subprocess.call(['echo', 'Even more output'])`. 

- `subprocess.run()`
The recommended way however is to use `subprocess.run()` which works since Python 3.5. It has been added as a simplification of `subprocess.Popen`. The function will return a `subprocess.CompletedProcess` object:

```python
process = subprocess.run(['echo', 'Even more output'], 
                         stdout=subprocess.PIPE, 
                         universal_newlines=True)
```
process
CompletedProcess(args=['echo', 'Even more output'], returncode=0, stdout='Even more output\n')
You can now find the resulting output in this variable:
process.stdout
'Even more output\n'

Similar to subprocess.call() and the previous .communicate() function, it will wait untill the process is completed. Finally, here is a more advanced example on how to access a server with ssh and the subprocess module:

```python
import subprocess

ssh = subprocess.Popen(["ssh", "-i .ssh/id_rsa", "user@host"],
                        stdin =subprocess.PIPE,
                        stdout=subprocess.PIPE,
                        stderr=subprocess.PIPE,
                        universal_newlines=True,
                        bufsize=0)
 
# Send ssh commands to stdin
ssh.stdin.write("uname -a\n")
ssh.stdin.write("uptime\n")
ssh.stdin.close()

# Fetch output
for line in ssh.stdout:
    print(line.strip())
```
Here you can see how to write input to the process. In this case you need to set the bufsize=0 in order to have unbuffered output. After you are finished writing to the stdin, you need to close the connection.

## Conclusion
You have seen now how to run external commands in Python. The most effective way is to use the subprocess module with all the functionality it offers. Most notably, you should consider using subprocess.run. For a short and quick script you might just want to use the os.system() or os.popen() functions. If you have any questions, feel free to leave them in the comments below. There are also other useful libraries that support shell commands in Python, like `plumbum`, `sh`, `psutils` and `pexpect`.

