<html>
<center>
<h1>
Lab3 Tester
</h1></center>
</html>

# Usage of test scripts

`./lab3_testing.sh ./Lab3 your_sudo_password result_folder`

For example:
`./lab3_testing.sh ./Lab3 XXXXXX ./Lab3`

You need to pass 3 arguments (the lab3 path and your sudo password, result_folder is a existing folder to store testing result) to the script, **and that's enough**. 

***Why need sudo privilege:***

For the sake of convenience, we will create several virtual NICs and set some parameters (such as delay, packet loss rate, etc), and these operations require sudo privilege. Ease up, there have no 'dangerous' operations in this script.

***How do you know your score:***

When the test script finishes running, it will be displayed at the bottom.

```shell
------ Score ------
Test items 1 PASSED 
Test items 2 PASSED 
Test items 3 PASSED 
Test items 4 PASSED 
Test items 5 PASSED 
Test items 6 PASSED 
Test items 7 PASSED 
Test items 8 PASSED 
Test items 9 PASSED
Test items 10 PASSED
```

# Scoring criteria

Please carefully read the [implementation requirements](https://github.com/LabCloudComputing/CloudComputingLabs_22/tree/2022/Lab3#4-implementation-requirements) provided in the lab3 guide book. The specific testing items for each scoring point will be provided below.

## Basic Version(18 points totally)

### 1st level of basic version(15 points)

- Test item 1: Run kvstore2pcsystem.

- Test item 2: Set key to hold string value.

- Test item 3: Get the value of the key.

- Test item 4: Return nil if the key does not exist.

- Test item 5: If the DEL command executed, return the number of keys that were removed.

- Test item 6: When associating a new value to an existing key, it should overwrite the value of the existing entry

- Test item 7: Correctness testing of DEL command.

The above testing items are all functional tests aimed at testing whether your KV storage system can correctly complete the implementation tasks given in the lab3 guide book.

### 2nd level of basic version(16 points)

- Test item 8: Kill one of the participants, execute SET and GET behaviors again.

- Test item 9: Kill all of the participants, execute GET behavior again.

The above testing items aim to test the fault-tolerant ability of the KV storage system you have implemented. We kill different numbers of participants and request the system to rate you based on the returned results

### 3rd level of basic version(18 points)

- Test item 10: Kill certain numbers of the participants, then restart the killed participants, execute SET and GET behaviors again.

The above test item is designed to test the robustness of the KV storage system you have implemented. By killing a certain number of participants and restarting (there will be 10 seconds after restarting, so that the restarted service can copy the data stored by other alive services), the teaching assistant will score according to the returned results.

## Advanced Version(20 points)

The test script for advanced version will be released later. If you have already implemented it and completed the self-test, please contact the teaching assistant for offline acceptance if the test script has not been launched at that time.
