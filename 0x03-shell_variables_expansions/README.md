alias ls="rm *" creates an alias.
echo "hello $USER" prints hello user, where user is the current Linux user.
export PATH=${PATH}:/action adds /action to the PATH. /action should be the last directory the shell looks into when looking for a program.
echo $PATH | tr ":" "\n" | wc -l counts the number of directories in the PATH.
printenv lists environment variables.
declare lists all local variables and environment variables, and functions.


