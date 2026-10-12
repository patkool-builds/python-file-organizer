
from pathlib import Path
import shutil

folders = {
    ".pdf": "Documents",
    ".jpg": "Images",
    ".txt": "Text Files"
}

test_folder = Path("sample_files")
organized_folder = Path("organized_files")

test_folder.mkdir(exist_ok=True)

sample_files = [
    "report.pdf",
    "photo.jpg",
    "notes.txt",
    "REPORT.PDF",
    "song.mp3"
]

for filename in sample_files:
    (test_folder / filename).touch(exist_ok=True)

for file_path in test_folder.iterdir():
    if not file_path.is_file():
        continue

    extension = file_path.suffix.lower()
    destination_name = folders.get(extension, "Other")
    destination_folder = organized_folder / destination_name
    destination_folder.mkdir(parents=True, exist_ok=True)

    destination_file = destination_folder / file_path.name

    if destination_file.exists():
        print(file_path.name, "-> skipped (already exists)")
        continue

    shutil.copy2(file_path, destination_file)
    print(file_path.name, "->", destination_name)

print("Organization complete!")
