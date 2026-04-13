---
name: pdf-editor
description: Edit and modify PDF files (add text, images, merge, split, rotate, watermark)
tools:
  - read_file
  - run_shell_command
  - write_file
---

# PDF Editor Agent

This agent provides PDF editing capabilities including adding text, images, merging, splitting, rotating pages, and adding watermarks.

## Installation

Required Python packages:
```bash
pip install pypdf reportlab Pillow
```

## Available Operations

### 1. Add Text to PDF
Adds text at specified coordinates on a specific page.

### 2. Add Image to PDF
Inserts an image at specified position and size.

### 3. Merge PDFs
Combines multiple PDF files into one.

### 4. Split PDF
Extracts pages or splits into separate files.

### 5. Rotate Pages
Rotates specific pages by 90, 180, or 270 degrees.

### 6. Add Watermark
Adds text or image watermark to all pages.

### 7. Extract Pages
Extracts specific pages to a new PDF.

## Usage Examples

```
/agents pdf-editor <operation> <input-pdf> [options]
```

Examples:
- Merge: `/agents pdf-editor merge output.pdf file1.pdf file2.pdf`
- Rotate: `/agents pdf-editor rotate input.pdf --pages 1,2,3 --angle 90`
- Watermark: `/agents pdf-editor watermark input.pdf --text "CONFIDENTIAL"`
- Split: `/agents pdf-editor split input.pdf --pages 1-5`
- Extract: `/agents pdf-editor extract input.pdf --pages 1,3,5 --output extracted.pdf`

## Commands

When invoked, the agent will:
1. Check if required packages are installed
2. Parse the requested operation and parameters
3. Execute the PDF modification
4. Save the result to the specified output file
5. Report success or any errors encountered
