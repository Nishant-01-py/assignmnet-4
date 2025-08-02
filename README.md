
Task 1: Read a File and Handle Errors filename = "sample.txt"

try:
    file = open('sample.txt','r')
    reading_file = file.read()
    print(reading_file)
except FileNotFoundError:
    print(f"Error: The file '{filename}' was not found.")



# Task 2: Write and Append Data to a File

file_name = "output.txt"
a1=input("Enter text to write to the file: ")
file = open('output.txt','w')
writing_file = file.write(a1+ '\n')
print (f"Data successfully written to {file_name}.")
print()

add_data = input("Enter additional text to append: ")
try:
    with open('output.txt','a') as file:
        file.write(add_data)
    print("Data successfully appended.")
except IOError as e:
    print(f"An error occurred while appending to the file: {e}")
    
print()

print("Final content of output.txt:")
try:
    file = open('output.txt', 'r')
    final_content = file.read()
    print(final_content)

except FileNotFoundError:
    print("Error: The file 'output.txt' was not found.")
except IOError as e:
    print(f"An error occurred while reading the file: {e}")
