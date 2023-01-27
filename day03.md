# Day 3: Exploring Bash Shell Scripting

## LPIC-1 Objective 105.2
<br></br>

### Notes

Bash script files have the suffix `.sh`

The first line of a shell script, sometimes called the *shebang* looks like this: `#!/PATH/of/Target/interpreter`. For a bash script the first line looks like this: `#!/bin/bash`.

You can specify which interpreter you want to use by using the PATH to that interpreter in the *shebang*.

The `#` symbol allows you to make comments in in bash scripts.

`exit` at the end of a script is good practice.

You can run scripts by entering `bash script.sh` in the terminal.

You can also run scripts with execute permissions on the script file and using the following command: `./scriptname.sh`.

You can run scripts from different locations with the absolute directory path then the script name: `PATH script.sh`
*Sourcing* is a way to run a script in the current shell, rather than creating a subshell to run the script. Often this will log you out of the current shell. `source script.sh` or `exec script.sh`.


### Bash Script Variables

Variables can be assinged in a script with the `=` operator. Example `a = "apple"`

Variables can hold commands. When variables are called in a script they must be prefixed with a `$`.

You can see the result of the last executed command with: `echo $?`.

### The `test` Command

To test if a file exists: `test -f /PATH/`

You can use`[]` instead of the `test` command, ensuring there is a space after the first bracket and before the last bracket: `[ -f /PATH/ ]`.

`-z` option within brackets is `TRUE` if the variable does not exist.


### Looping in Bash

For loops and the `seq` command

Example:

```bash
#!/bin/bash
#
for loopVar in $(seq 1 6)
do
    echo "The number is: " $loopVar
done
exit
```

While loops

Example:

```bash
#!/bin/bash
#
loopVar=1
while [ $loopVar -ne 10 ]
do
    echo "The number is: " $loopVar
    loopVar=$[ $loopVar + 1]
done
exit
```

User input:

Use the `read -p "Display Text" InputVariable` command syntax.
