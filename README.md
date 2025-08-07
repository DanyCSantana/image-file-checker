# 🖼️ image-file-checker

A simple Python tool to verify the presence of expected image files in a target folder and generate a report listing any missing files.

## 📌 Description

This script helps validate whether all required image files (e.g., movie posters, thumbnails) are present in a specific directory.  
It compares the contents of a folder with a reference list provided in a `.txt` file and generates a summary report of any missing files.

Useful for:
- Media asset validation
- QC in metadata pipelines
- Automation of folder checks in content delivery workflows

## 🛠️ How it works

1. Reads a `.txt` file containing the list of expected filenames (one per line)
2. Scans the target folder for existing image files
3. Compares the list with actual files
4. Creates a `relatorio_faltando.txt` file listing any missing images and summary stats

## 📂 Folder Structure Example

