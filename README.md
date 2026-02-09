# Fisoo

A Python command line tool that automatically organizes messy folders by file type.

[![Python Version](https://img.shields.io/badge/python-3.6%2B-blue)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

## Features

-  Organizes files into categories (Documents, Images, Videos, Archives)
-  Dry run mode to preview changes before executing
-  Handles duplicate files (rename or skip)
-  Moves uncategorized files to "unsorted" folder
-  Summary report of all moved files

## Requirements
- Python 3.6 or higher
- No external dependencies (uses standard library only)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/PhenPen/Fisoo.git
   cd Fisoo```
   ```
2. Ensure Python 3.6+ is installed:
	- python --version

## Usage
1. Run the script: python sort.py
2. Follow the prompts:
	- Enter the path to the folder you want to organize
	- Choose whether to preview changes (dry run) or organize immediately
3. View the summary of moved files

#### Command Line Example

```
 > $ python sort.py
Enter location of folder to sort: /Users/john/Downloads
Display files to be moved or move directly? y/n:    y 
```

Select 'y' to select DRY RUN MODE - No files will be moved and summary would be displayed instead

```
Will move report.pdf from /Users/john/Downloads/report.pdf to /Users/john/Downloads/Documents/report.pdf
Will move photo.png from /Users/john/Downloads/photo.png to /Users/john/Downloads/Images/photo.png
...

> Move files? y/n: y

Moved report.pdf
Moved photo.png
...

Total files in folder: 47
Moved a total of 45 files
```

#### Example
##### Before organizing:
Downloads/
├── report.pdf
├── photo.png
├── video.mp4
├── document.docx
├── presentation.pptx
└── random_file.xyz

##### After organizing:
Downloads/
├── Documents/
│   ├── report.pdf
│   ├── document.docx
│   └── presentation.pptx
├── Images/
│   └── photo.png
├── Videos/
│   └── video.mp4
└── unsorted/
    └── random_file.xyz

## Supported files
| Category  | Supported File Types |
| --------- | -------------------- |
| Documents | PDF, DOCX, DOC, XLSX |
| Images    | PNG                  |
| Videos    | MOV, MP4             |
| Archives  | ZIP                  |

## Features in Detail
####  Dry Run Mode
	- Preview what will happen before making any changes:
	- Shows which files will be moved
	- Shows destination folders
	- Asks for confirmation before proceeding
	- Safe way to test without affecting your files
#### Duplicate Handling
	- When a file with the same name already exists in the destination:
	- Option 1: Rename (adds _1, _2, etc. to filename)
	- Option 2: Skip the duplicate file
	- You choose which option when prompted.
#### Unsorted Files
	- Files that don't match any category are moved to an "unsorted" folder for manual review. This ensures nothing gets lost.

## Project Structure
Fisoo/
├── sort.py              # Main script
├── README.md            # Documentation
└── LICENSE              # MIT License

## Contributing
	- Contributions are welcome! Here's how you can help:
	- Report bugs: Open an issue describing the problem
	- Suggest features: Open an issue with your idea
	- Submit fixes: Fork the repo, make changes, submit a pull request

	- Follow PEP 8 guidelines andm comments to code and test changes before submitting



## Why I Built This
I built this project as part of my Python journey. My downloads folder was always a mess, and I wanted to automate the clean up process. This was on of my first complete Python CLI tools, built in about 4 hours (initially coded on mobile phone!).

## Authors / Contributors

<!-- ALL-CONTRIBUTORS-LIST:START -->
| [<img src="https://github.com/PhenPen.png" width="100px;" alt="Phen"/><br /><sub><b>Phen</b></sub>](https://github.com/PhenPen)<br /> | [<img src="https://github.com/Raze92.png" width="100px;" alt="Chidera Onyegbule"/><br /><sub><b>Chidera Onyegbule</b></sub>](https://github.com/Raze92)<br />[LinkedIn](https://linkedin.com/in/chidera-onyegbule) |
| :---: | :---: |
<!-- ALL-CONTRIBUTORS-LIST:END -->

## Acknowledgments
Inspired by the constant struggle of messy download folders
Built as one of my first projects in my programming journey
Thanks to the Python community for excellent documentation

⭐ If you found this helpful, please star the repository!
---