# SAGE Dependencies Guide

## Required Dependencies

### 1. Tesseract OCR
**Purpose**: Text extraction from images and PDFs

**Installation Steps**:
1. Download Tesseract installer from [UB-Mannheim/tesseract](https://github.com/UB-Mannheim/tesseract/wiki)
2. Run the installer
3. Install to default location: `C:\Program Files\Tesseract-OCR`
4. During installation:
   - Select "Add to PATH"
   - Install all language packs needed

**Verification**:
```cmd
tesseract --version
```

### 2. Poppler
**Purpose**: PDF processing and conversion

**Installation Steps**:
1. Download Poppler for Windows from [Poppler Windows](http://blog.alivate.com.au/poppler-windows/)
2. Extract the downloaded file
3. Copy contents to a permanent location (e.g., `C:\Program Files\poppler`)
4. Add bin folder to system PATH:
   - Open System Properties (Win + Pause/Break)
   - Click "Advanced system settings"
   - Click "Environment Variables"
   - Under System Variables, find "Path"
   - Click "Edit" and add new entry: `C:\Program Files\poppler\bin`

**Verification**:
```cmd
pdfinfo --version
```

### 3. Visual C++ Redistributable
**Purpose**: Required runtime components

**Installation Steps**:
1. Download latest version from [Microsoft Visual C++ Downloads](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist)
2. Run the installer
3. Follow installation prompts
4. Restart computer if prompted

## Setting Up PATH Variables

### Automatic Verification
1. Open Command Prompt (cmd.exe)
2. Run the following commands:
```cmd
echo %PATH%
tesseract --version
pdfinfo --version
```

### Manual PATH Setup
If PATH variables weren't set automatically:

1. Open System Properties:
   - Press Win + Pause/Break
   - Click "Advanced system settings"
   - Click "Environment Variables"

2. Under "System Variables", find and select "Path"

3. Click "Edit" and add these entries:
   ```
   C:\Program Files\Tesseract-OCR
   C:\Program Files\poppler\bin
   ```

4. Click "OK" on all windows

## Troubleshooting

### Common Issues

1. **"Tesseract is not recognized..."**
   - Verify installation path
   - Check PATH variable
   - Reinstall with "Add to PATH" option
   - Restart Command Prompt after changes

2. **"Poppler command not found"**
   - Verify bin folder location
   - Check PATH variable
   - Ensure files are extracted to correct location
   - Restart Command Prompt after changes

3. **"VCRUNTIME140.dll missing"**
   - Install/reinstall Visual C++ Redistributable
   - Install both x86 and x64 versions
   - Restart computer

### Verification Steps

After installation, verify all components:

1. **Check Tesseract**:
```cmd
tesseract --version
```
Expected: Version information display

2. **Check Poppler**:
```cmd
pdfinfo --version
```
Expected: Version information display

3. **Check Visual C++**:
- Open Control Panel
- Programs and Features
- Look for "Microsoft Visual C++ Redistributable"

## Important Notes

1. **System Requirements**
   - Windows 10/11 (64-bit)
   - 8GB RAM minimum
   - 2GB free disk space
   - Administrator privileges for installation

2. **Best Practices**
   - Install dependencies in default locations
   - Allow PATH modifications during installation
   - Restart computer after all installations
   - Verify each component before running SAGE

3. **Maintenance**
   - Keep Visual C++ Redistributable updated
   - Check for Tesseract updates periodically
   - Maintain adequate disk space

## Getting Help

If you encounter issues:

1. **Check Common Solutions**:
   - Verify all installations
   - Check PATH variables
   - Restart computer
   - Run as administrator

2. **Report Issues**:
   - Create GitHub issue with:
     - Full error message
     - System specifications
     - Installation logs
     - Steps to reproduce

3. **Contact Support**:
   - Via GitHub Issues
   - Include all verification outputs
   - List installed dependency versions

Remember to restart your computer after installing all dependencies to ensure proper system integration.
