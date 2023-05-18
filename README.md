# -Write-a-Python-program-to-read-an-entire-text-file.
def read_text_file(file_path):
    try:
        with open(file_path, 'r') as file:
            contents = file.read()
            return contents
    except FileNotFoundError:
        print("File not found.")
    except IOError:
        print("An error occurred while reading the file.")

# Example usage
file_path = 'path/to/your/text/file.txt'  # Replace with the actual file path
file_contents = read_text_file(file_path)
if file_contents:
    print("File contents:")
    print(file_contents)
