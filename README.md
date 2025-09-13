# EEG Electrode Mapper

A browser-based tool for creating custom EEG electrode layouts using the international 10-10 system. Generate high-quality SVG diagrams for research, clinical documentation, and publication.

## Features

- **76 standard 10-10 electrodes** with accurate positioning
- **Interactive electrode selection** with visual head map
- **12 preset configurations** for common electrode arrangements
- **High-quality SVG export** with customizable layouts
- **Region-based color coding** for easy identification
- **No installation required** - runs directly in web browser

## Quick Start

### Using VSCode Live Server (Recommended)

1. Install the Live Server extension in VSCode
2. Open `eeg_electrode_selector_en.html` in VSCode
3. Right-click and select "Open with Live Server"

### Alternative Web Servers

```bash
# Python
python -m http.server 8000

# Node.js
npx http-server -p 8000

# PHP
php -S localhost:8000
```

## Available Files

| File | Description |
|------|-------------|
| `eeg_electrode_selector_en.html` | English version with full features |
| `eeg_electrode_selector_numbered_standalone.html` | Version with numbered electrodes |
| `eeg_electrode_selector_pdf.html` | PDF-optimized version |
| `electrode_correction_list_new.json` | Electrode coordinate data |

## Usage

### Electrode Selection
- **Individual Selection**: Click electrodes on the head map
- **Preset Selection**: Use buttons for common electrode configurations
- **Search**: Filter electrodes by name or region

### Available Presets

| Preset | Count | Description |
|--------|-------|-------------|
| Standard 21 | 20 | Basic clinical EEG set |
| Motor Cortex | 5 | C3, C1, Cz, C2, C4 |
| Frontal | ~30 | Fp, AF, F electrodes |
| Central | ~20 | FC, C electrodes |
| Parietal | ~15 | CP, P electrodes |
| Occipital | ~20 | PO, O, I electrodes |
| Temporal | ~10 | FT, T, TP electrodes |
| Left Hemisphere | ~35 | Odd-numbered electrodes |
| Right Hemisphere | ~35 | Even-numbered electrodes |
| Midline | ~10 | z-line electrodes |
| All Electrodes | 76 | Complete 10-10 system |

### Export Options
- **High-quality SVG**: Scalable vector graphics for publications
- **Complete layout**: Includes nose/ear markers and legend
- **Automatic naming**: `EEG_10-10_layout_XXch_timestamp.svg`

## Technical Specifications

### Coordinate System
- **Normalized coordinates**: -1.0 to +1.0 range
- **Origin**: Head center (near Cz)
- **Y-axis**: Positive toward nose
- **Mapping accuracy**: 53 electrodes with distance < 0.1

### Data Structure
```javascript
{
    "name": "Cz",           // Standard 10-10 electrode name
    "x": -0.002,            // Normalized X coordinate
    "y": 0.078,             // Normalized Y coordinate
    "pixel_x": 424,         // Original pixel coordinates
    "pixel_y": 390,
    "radius": 22,           // Detection radius
    "assignment_distance": 0.078  // Mapping accuracy
}
```

### Browser Compatibility
- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari
- ⚠️ Internet Explorer 11 (limited support)

## Region Color Coding

| Region | Color | Example Electrodes |
|--------|-------|-------------------|
| Frontal | Orange | Fp1, AF3, F7, F3, Fz |
| Central | Green | FC1, C3, Cz, C4 |
| Parietal | Purple | CP3, P7, P3, Pz |
| Occipital | Brown | PO3, O1, Oz, I1 |
| Temporal | Blue | FT7, T7, TP7 |

## Troubleshooting

### Server Issues
1. Ensure HTML file is open in VSCode
2. Verify Live Server extension is installed
3. Check if port is available (try different port)

### Display Problems
1. Open browser console (F12) to check for errors
2. Verify JavaScript is enabled
3. Try a different browser

### Export Issues
1. Disable popup blockers
2. Check download settings
3. Try alternative browser

## Quality Assurance

### Mapping Accuracy
- **Good**: 53 electrodes (distance < 0.1)
- **Acceptable**: 4 electrodes (0.1 ≤ distance < 0.2)
- **Needs adjustment**: 19 electrodes (distance ≥ 0.2)

### Key Electrode Accuracy
- Cz: distance 0.078 ✅
- F3: distance 0.084 ✅
- P3: distance 0.085 ✅
- AFz: distance 0.078 ✅

## License

This project is open source and available for academic and research use.