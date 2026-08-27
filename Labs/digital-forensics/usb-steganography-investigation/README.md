# USB Digital Forensics & Steganography Investigation

## Overview

This project documents a digital forensics investigation completed as
part of my cybersecurity coursework.

The investigation involved analyzing a forensic image of a USB storage
device to identify suspicious files, recover hidden evidence, verify
file integrity, and document potential security policy violations.

This repository is intended to demonstrate my practical experience with
digital forensics concepts and tools.

## Objectives

The investigation focused on:

- Examining a forensic USB image
- Identifying suspicious files and artifacts
- Calculating and documenting file hashes
- Examining Windows Zone Identifier information
- Detecting files containing hidden data
- Recovering embedded JPEG images
- Using file signatures and magic numbers
- Documenting evidence and policy violations
- Maintaining a structured forensic investigation report

## Tools Used

### Autopsy 4.21
Used to process and analyze the forensic image of the USB storage device.

### WinMD5
Used to calculate and verify MD5 hashes associated with evidence files.

### Hexed.it
Used for hexadecimal analysis and identification of embedded file data.

## Forensic Techniques Demonstrated

### Disk Image Analysis
The USB evidence image was imported into Autopsy and examined for
relevant artifacts.

### File Hashing
Hashes were documented to help uniquely identify evidence files and
support evidence integrity.

### File Signature Analysis

JPEG files were identified using their hexadecimal signatures:

JPEG Header:
FF D8 FF

JPEG End-of-File Marker:
FF D9

These signatures were useful when identifying and recovering embedded
image data.

### Steganography Analysis

Several files appeared to contain additional image data hidden within
otherwise normal image files.

Hexadecimal analysis was used to identify the beginning and ending
signatures of embedded JPEG files.

### Zone Identifier Analysis

Windows Zone Identifier metadata was examined to help determine the
origin of downloaded files.

For example, ZoneId=3 indicates that a file originated from the
Internet zone.

## Investigation Workflow

1. Obtain forensic evidence image
2. Verify evidence integrity
3. Create forensic case in Autopsy
4. Import USB image
5. Examine files and metadata
6. Identify suspicious artifacts
7. Calculate/document hashes
8. Examine suspicious files using hexadecimal analysis
9. Locate JPEG file signatures
10. Recover embedded images
11. Document findings
12. Compare findings against organizational security policies
13. Produce final forensic report

## Skills Demonstrated

- Digital Forensics
- Autopsy
- Evidence Analysis
- File Hashing
- MD5
- Metadata Analysis
- Windows Zone Identifiers
- Hexadecimal Analysis
- File Carving
- Steganography Detection
- File Signatures / Magic Numbers
- Incident Documentation
- Security Policy Analysis

## Key Takeaway

This investigation demonstrated how apparently normal files can contain
additional hidden information and why analysts should examine file
content, metadata, hashes, and hexadecimal structures rather than relying
only on filenames or extensions.

It also provided experience documenting evidence in a structured
forensic report and relating technical findings to organizational
security policies.

## Full Report

The sanitized forensic investigation report is available in the
`report/` directory.

## Disclaimer

This project was completed in an authorized academic lab environment.
The scenario, evidence, and individuals referenced in the exercise are
part of a cybersecurity training exercise. No testing or investigation
was performed against systems without authorization.
