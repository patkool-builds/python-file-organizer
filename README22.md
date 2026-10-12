Python File Organizer

A beginner Python project by Patkool, built to practise file handling, automation, and organizing files by type.

What It Does

* Identifies file types using their extensions.
* Creates folders for different file categories.
* Organizes files into folders such as Documents, Images, and Text Files.
* Handles uppercase extensions, such as .PDF.
* Skips destination files that already exist instead of overwriting them.
* Prints a message showing what happened to each file.

Technologies Used

* Python
* pathlib for working with file paths and folders
* shutil for copying files

How It Works

The program checks each file’s extension, chooses the matching destination folder, creates that folder if necessary, and copies the file when a destination copy does not already exist.

How to Run

1. Install Python 3.
2. Download or clone this repository.
3. Open a terminal in the project folder.
4. Run:
    python main.py

Depending on your system, you may need to use python3 main.py instead.

Current Limitations

* The current version uses sample files for testing.
* It copies files rather than moving the originals.
* It skips files when a destination file with the same name already exists.
* The project is still under development.

What I’m Learning

This project is helping me practise Python loops, conditional statements, dictionaries, file paths, folder creation, and basic automation.

Author

Patkool — learning Python and building practical projects as part of my journey into IT and cybersecurity.
