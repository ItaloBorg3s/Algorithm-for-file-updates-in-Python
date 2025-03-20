# Algorithm for File Updates in Python

## Project Description
In this project, the goal was to update an allow list of IP addresses by removing unwanted addresses. The project involves reading an existing text file, processing the data, and then updating the file with a revised list of IP addresses. Below are the steps taken to complete the task using Python.

### Open the file that contains the allow list
In this task, the file containing the list of allowed IP addresses is opened using the `open()` function with the "r" parameter to read the contents.

```python
import_file = "allow_list.txt"
remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

# First line of `with` statement
with open(import_file, "r") as file:
```

Task 2: Aqui vai a captura de tela da Tarefa 2
![task 2](https://github.com/user-attachments/assets/690b9472-b5f0-4e59-a77d-40f1287f10dd)


### Read the file contents
The file contents are read using the `.read()` method and stored in the `ip_addresses` variable. The data is displayed to verify its current format.

```python
with open(import_file, "r") as file:
    ip_addresses = file.read()

# Display `ip_addresses`
print(ip_addresses)
```

Task 3: Aqui vai a captura de tela da Tarefa 3
![task 3](https://github.com/user-attachments/assets/afb3ab59-d2cd-4808-94de-7012249b1f07)


### Convert the string into a list
To work with the data in a more manageable form, the string containing all IP addresses is split into a list using the `.split()` method.

```python
ip_addresses = ip_addresses.split()
# Display `ip_addresses`
print(ip_addresses)
```

Task 4: Aqui vai a captura de tela da Tarefa 4
![task 4](https://github.com/user-attachments/assets/98b62257-5d5b-4130-ac83-6a399868574e)


### Iterate through the remove list
The program then loops through the `remove_list` and checks each IP address in the `ip_addresses` list to determine if it should be removed.

```python
for element in ip_addresses:
    print(element)
```

Task 5: Aqui vai a captura de tela da Tarefa 5
![task 5](https://github.com/user-attachments/assets/baa8b11b-0576-426b-bce2-ff8ae2c24652)


### Remove IP addresses that are on the remove list
In each iteration, a conditional check is used to determine if the current IP address should be removed. If it is found in the `remove_list`, the `.remove()` method is applied to remove that IP address.

```python
for element in ip_addresses:
    if element in remove_list:
        ip_addresses.remove(element)
```

Task 6: Aqui vai a captura de tela da Tarefa 6
![task 6](https://github.com/user-attachments/assets/4cbfc528-a820-4485-8d91-0c88a56a7355)


### Update the file with the revised list of IP addresses
After removing the unwanted IPs, the list is converted back into a string using `.join()` so it can be written back to the file.

```python
ip_addresses = "\n".join(ip_addresses)

# Rewrite the file with the updated IP addresses
with open(import_file, "w") as file:
    file.write(ip_addresses)
```

Task 7: Aqui vai a captura de tela da Tarefa 7
![task 7](https://github.com/user-attachments/assets/b90812e7-ce65-4c1e-9ba6-e87e3cd947cf)


### Summary
This Python project automates the process of updating an IP address allow list by removing specified addresses. It reads an input file, processes the list, and then writes the updated list back into the original file. The solution involves reading, iterating, modifying, and writing data efficiently using Python's built-in methods such as `.read()`, `.split()`, `.remove()`, and `.join()`. The project demonstrates how to manage and update data in text files using basic Python functionalities.

