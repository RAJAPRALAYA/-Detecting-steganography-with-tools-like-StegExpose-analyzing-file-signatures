# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures

## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
List of Images with Steganography Detection Scores and File Signature Details
<img width="920" height="261" alt="Screenshot 2025-10-22 001351" src="https://github.com/user-attachments/assets/d07fd65a-7e6c-425f-b1a2-624f2097ba10" />


<img width="946" height="244" alt="Screenshot 2025-10-22 001359" src="https://github.com/user-attachments/assets/ceffd93c-aad6-4aa4-8abf-c2a4d351c507" />



<img width="1039" height="816" alt="Screenshot 2025-10-22 001415" src="https://github.com/user-attachments/assets/da26cd36-4762-440e-9ea8-0f9acdfed422" />



## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
