# Bash commands
Get nth column from CSV

`cut -d, -fn <filename>`

Combine multiple lines into 1

`tr -d ‘\n’`

Find file with setuid bit set and rw-r-r

`find / -perm 4644 -exec ls -l {} \;`

Calculate numbers from output of file (6th field in csv)

`cat test.csv | cut -f 6 -d, | sed -e "s/\"//g" | tail -n +2 | paste -sd+ | bc`  
 

Get information about ports and associated binaries

`ss -natup`