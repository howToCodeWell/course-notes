## Method one : Create directories one at a time

Create a directory called temp
```bash
$ mkdir temp
```
List the contents of the current working directory and notice the new temp folder
```bash
$ ls
temp
```
Move into the new temp directory
```bash
cd temp
```
List the contents of the new temp directory. This will return a blank prompt
```bash
$ ls 

```
Create a new directory in the temp directory called test
```bash
$ mkdir test
```
List the contents of the temp directory. Notice the new sub directory called test
```bash
$ ls 
test
```

## Method two : Create nested directories using one command
This will create intermediate directories if they don't exist.
```bash
$ mkdir -p temp/test/src/Controller
```
The `-p` argument will create the `src` and the `Controller` directories.
Without the `-p` argument an error will be raised if the requested directory already exists

```bash
$ mkdir  temp/test/src/Controller
mkdir: temp/test/src/Controller: File exists
```
