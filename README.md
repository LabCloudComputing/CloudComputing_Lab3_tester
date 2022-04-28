# 2022_Lab3_tester

## Test script of lab3

### Usage

`./lab3_testing.sh ./Lab3 your_sudo_password result_folder`

For example:
`./lab3_testing.sh ./Lab3 XXXXXX ./Lab3`

You need to pass 3 arguments (the lab3 path and your sudo password, result_folder is a existing floder to store testing result) to the script, **and that's enough**. 

***Why need sudo privilege:***

For the sake of convenience, we will create several virtual NICs and set some parameters (such as delay, packet loss rate, etc), and these operations require sudo privilege. Ease up, there have no 'dangerous' operations in this script.
