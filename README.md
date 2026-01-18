# bambu2prusa

A command-line tool to convert 3mf files containing colored, painted models created with Bambu Studio to PrusaSlicer-compatible files.

## Credits

**Original Author:** Jaime C. Acosta

**Original Project:** [3mf_bambu2prusa](https://github.com/raistlinJ/3mf_bambu2prusa) - GUI-based Bambu to Prusa 3mf converter

This tool was originally created by Jaime C. Acosta as a GUI application using tkinter. The conversion logic and 3mf file format analysis are entirely his work. This version has been modified to run as a CLI tool only.

## Description

This was created by analyzing 3mf files directly and not the specification. It handles the conversion of paint/color data from Bambu's format to Prusa's `slic3rpe:mmu_segmentation` format.

## Installation

1. Create and activate a virtual environment:

```
python3 -m venv env
source env/bin/activate
```

2. Install requirements:

```
pip install -r requirements.txt
```

## Usage

```
python bambu2prusa.py <input.3mf> [output.3mf]
```

If no output file is specified, the default is `<input>-prusa.3mf`.

### Options

- `-v, --verbose` - Enable verbose/debug output
- `-h, --help` - Show help message

### Examples

```
# Basic conversion (outputs my_bambu_model-prusa.3mf)
python bambu2prusa.py my_bambu_model.3mf

# Specify output filename
python bambu2prusa.py my_bambu_model.3mf my_prusa_model.3mf

# With verbose output
python bambu2prusa.py -v my_bambu_model.3mf
```

## License

GPL 3.0
