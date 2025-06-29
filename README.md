# digital-forensics-toolkit

Preview
https://github.com/bharanikumar25/digital-forensics-toolkit/blob/e3018b3920e372ff0b67586e8d3a81b28a5c2392/Preview_Dark.png
Features 🌟      ⬆️
✅ *Image Mounting: Mount forensic disk images. (Windows only)
✅ Tree Viewer: Navigate through the disk image structure, including partitions and files.
✅ Detailed File Analysis: View file content in different formats, such as HEX, text, and application-specific views.
✅ EXIF Data Extraction: Extract and display EXIF metadata from photos.
✅ Registry Viewer: View and examine Windows registry files.
✅ Basic File Carving: Recover deleted files from disk images.
✅ Virus Total API Integration: Check files for malware using the Virus Total API.
✅ E01 Image Verification: Verify the integrity of E01 disk images.
✅ Convert E01 to Raw: Convert E01 disk images to raw format.
✅ Message Decoding: Decode messages from base64, binary, and other encodings.


Screenshots 📸      ⬆️
Registry Browser 🗂️

Registry Browser

File Carving 🔪

File Carving

File Search 🔍

Image Verification

Image Verification ✅

Image Verification


Supported Image Formats 💾      ⬆️
Image Format	Extensions	Split	Unsplit
EnCase® Image File (EVF / Expert Witness Format)	*.E01 *.Ex01	✔️	✔️
SMART/Expert Witness Image File	*.s01	✔️	✔️
Single Image Unix / Linux DD / Raw	*.dd, *.img, *.raw	✔️	✔️
ISO Image File	*.iso		✔️
AccessData Image File	*.ad1	✔️	✔️

Tested File Systems 🗂️      ⬆️
File System	Tested
NTFS	✔️
FAT32	
exFAT	
HFS+	
APFS	
EXT2,3,4	

Cross-Platform Compatibility 💻🖥️      ⬆️
Operating System	Screenshot
macOS Sonoma 🍏	macOS Screenshot
Kali Linux 2024 🐧	Kali Linux Screenshot
*WSL2 - Ubuntu 22.04.3 LTS 🐧	Kali Linux Screenshot
Windows 10 🗔	Windows Screenshot
Getting Started 🚀      ⬆️
Prerequisites 🔧
For Windows:
*There's a compatibility issue with Python 3.12. Please install Python 3.11 from the official Python website: https://www.python.org/downloads/release/python-3110/

If you don't already have Microsoft C++ Build Tools installed, you'll need to install them to compile required packages like libewf-python and pytsk3.

*If you encounter this error while installing dependencies:

"Microsoft Visual C++ 14.0 or greater is required"
It means your C++ Build Tools are missing or outdated.
Please follow the steps below to install the latest version of "C++ Build Tools".
Step 1: Download and Install Microsoft C++ Build Tools - https://visualstudio.microsoft.com/visual-cpp-build-tools/ During the installation, make sure to select the following workloads:

Desktop development with C++
C++ build tools
Step 2: Install the Dependencies

pip install -r requirements.txt
For macOS - Apple Silicon:
Create a virtual environment with python 3.11

python3.11 -m venv venv
source venv/bin/activate
chmod +x install_macos_silicon.sh
./install_macos_silicon.sh
This script will:

Check if Homebrew is installed and offer to install it if it’s not.
Install necessary system dependencies (ffmpeg and poppler) using Homebrew.
Install all Python dependencies specified in requirements_macos_silicon.txt using pip.
For Ubuntu on WSL:
chmod +x WSL_Ubuntu_install.sh
./WSL_Ubuntu_install.sh
This script will:

Update package lists and install necessary system packages including graphics libraries and sound management tools.
Install necessary Python dependencies from requirements_macos_silicon.txt (same requirements for Ubuntu).
Configuration ⚙️
API Keys Configuration:The tool integrates with VirusTotal and Veriphone APIs, and you will need to provide your own API keys to use these features. To update the API keys, go to the Options menu and select API Keys submenu.

Running the Tool ▶️
python main.py

Built With 🧱      ⬆️
pytsk3 - Python bindings for the SleuthKit
libewf-python - Library to access the Expert Witness Compression Format (EWF)
PySide6 - Used for the GUI components.
Arsenal Image Mounter - For mounting forensic disk images.
Work in Progress 🧑‍🔧      ⬆️
Direct Video/Audio Playback: Currently, the video and audio player saves files temporarily before playing them, which can cause delays. The goal is to enable direct playback for faster performance.
Integrated File Search and Viewer: The file search functionality is not yet connected to the "Viewer Tab," which displays HEX, text, application-specific views, metadata, and other details. This integration needs to be implemented.
Cross-Platform Image Mounting: Image mounting currently works only on Windows using the Arsenal Image Mounter executable. The aim is to make this feature work across all platforms without relying on external executables.
File Carving and Viewer Integration: The file carving functionality is not yet connected to the "Viewer Tab," where users can view HEX, text, application-specific views, and metadata. Additionally, the current file carving process does not distinguish between deleted and non-deleted files; it will "carve" all files of the selected type from the disk image.
Color Issues in Dark Mode: The software currently has some colour display issues on Linux and macOS systems when using dark mode. Certain UI elements may not be clearly visible or may appear incorrectly.
Testing & Feedback 🧪      ⬆️
Tested Formats: The tool has primarily been tested with dd and E01 files. While these formats are well-supported, additional testing with other formats, such as Ex01, Lx01, s01, and others, is needed.
Tested File Systems: Currently, the tool has only been tested on the NTFS file system. Testing on additional file systems like FAT32, exFAT, HFS+, APFS, EXT4, and others is needed to ensure broader compatibility.
Call for Samples: If you have disk images in formats that are less tested (Ex01, Lx01, s01, etc.), your contributions would be greatly appreciated to help improve the tool's compatibility and robustness.
Feedback Welcome: Please report any issues or unexpected behaviour to help improve the tool. Contributions and testing feedback are encouraged and welcomed.
Contributing 🤝      ⬆️
I welcome contributions from the community to help improve TRACE! If you're interested in contributing, here’s how you can get involved:

How to Contribute
Report Issues: If you find any bugs or have suggestions for improvements, please open an issue on GitHub. Provide as much detail as possible to help address the issue effectively.
Submit a Pull Request: If you have a fix or feature you’d like to contribute, please fork the repository, make your changes, and submit a pull request. Ensure your code adheres to the coding standards and includes tests where applicable.
Provide Testing Samples: If you have disk images in formats that are less tested (Ex01, Lx01, s01, etc.), your contributions would be greatly appreciated to help improve the tool’s compatibility and robustness. You can share these samples by contacting me.
Review and Feedback: Review the changes submitted by others and provide feedback to help refine and enhance the tool.
