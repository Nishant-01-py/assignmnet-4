filename = "sample.txt"
try:
    file = open('sample.txt','r')
    reading_file = file.read()
    print(reading_file)
except FileNotFoundError:
    print(f"Error: The file '{filename}' was not found.")
