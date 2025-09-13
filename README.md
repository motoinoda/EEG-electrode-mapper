# EEG Electrode Mapper

A standalone HTML tool for creating custom EEG electrode layouts using the international 10-10 system. **No server required** - just open in your browser and start selecting electrodes for your research.

## Features

- **🚀 Zero setup** - Double-click HTML file and start immediately
- **Interactive head map** - Visual 3D-style electrode placement
- **Click-to-select electrodes** - Individual electrode selection with hover effects
- **6 anatomical presets** - Frontal, Central, Parietal, Occipital, Temporal, All
- **Dual export formats** - High-quality SVG and PNG downloads
- **Live electrode editing** - Rename electrodes with edit mode
- **Search functionality** - Find electrodes by name
- **Real-time counter** - See selected electrode count instantly

## Quick Start

### Method 1: Direct Browser Launch (Easiest)

**Just double-click the HTML file** - works instantly:

- `eeg_electrode_selector_main_en.html` - **Main English version** (recommended)
- `eeg_electrode_selector_main_jp.html` - Japanese version
- `eeg_electrode_selector_archive.html` - Archive version

### Method 2: Using VSCode Live Server (Optional)

For development workflow:

1. Install Live Server extension in VSCode
2. Right-click HTML file → "Open with Live Server"

## Available Files

| File | Description | Language |
|------|-------------|----------|
| `eeg_electrode_selector_main_en.html` | **Main version** with all features | English |
| `eeg_electrode_selector_main_jp.html` | Full-featured version | Japanese |
| `eeg_electrode_selector_archive.html` | Archive/backup version | Mixed |
| `electrode_correction_list_new.json` | Electrode coordinate data | - |

## How to Use

### Step-by-Step Guide

1. **Open the tool** - Double-click `eeg_electrode_selector_main_en.html`
2. **Select electrodes** - Click individual electrodes on the head map
3. **Use presets** - Or click preset buttons for common configurations
4. **Export layout** - Click "Export SVG" or "Export PNG" to save

### Interactive Features

- **Hover effects** - Electrodes scale up and highlight when hovered
- **Real-time feedback** - Selected electrode count updates instantly
- **Search box** - Type to find specific electrodes quickly
- **Edit mode** - Toggle to rename electrodes (click Edit Mode button)
- **Clear all** - Reset selection with one click

### Available Presets

| Preset | Example Electrodes | Use Case |
|--------|-------------------|----------|
| **Frontal** | Fp1, Fp2, AF3, AF4, F1-F8, Fz | Attention, executive function |
| **Central** | FC1-FC6, C1-C6, Cz | Motor control, sensorimotor |
| **Parietal** | CP1-CP6, P1-P8, Pz | Spatial processing, attention |
| **Occipital** | PO3, PO4, O1, O2, Oz | Visual processing |
| **Temporal** | T7, T8, TP7-TP10, FC7-FC10 | Auditory, language |
| **All** | Complete 10-10 system | Full coverage studies |

### Export Features

- **SVG format** - Scalable vector graphics, perfect for publications
- **PNG format** - High-resolution bitmap for presentations
- **Auto-naming** - Files named with electrode count and date
- **Complete layout** - Includes head outline, nose, and ear markers

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
- ✅ **Chrome/Edge** (recommended) - Full support with all animations
- ✅ **Firefox** - Full support
- ✅ **Safari** - Full support
- ✅ **Mobile browsers** - Touch-friendly interface
- ⚠️ **Internet Explorer** - Not recommended, use Edge instead

### Visual Design
- **3D-style head outline** with nose and ear markers for orientation
- **Interactive electrodes** with hover scaling and visual feedback
- **Clean modern interface** with gradient backgrounds
- **Responsive design** that works on different screen sizes
- **Color-coded selection** - Selected electrodes turn red

## Troubleshooting

### File Won't Open in Browser
1. Make sure you're opening an HTML file (not JSON)
2. Try right-click → "Open with" → select your browser
3. If using Chrome, may need to use `file://` protocol

### Display Problems
1. Ensure JavaScript is enabled in your browser
2. Try a different browser (Chrome/Firefox/Safari recommended)
3. Check browser console (F12) for error messages

### Export Issues
1. Disable popup blockers for SVG downloads
2. Check browser download settings
3. Try right-click → "Save as" if download button doesn't work

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

## Perfect for Research

### Academic Applications
- **EEG study design** - Plan electrode montages before data collection
- **Paper illustrations** - Generate publication-quality electrode diagrams
- **Grant proposals** - Visual representation of planned electrode coverage
- **Teaching** - Demonstrate 10-10 system to students
- **Clinical documentation** - Document electrode placement for patients

### Key Advantages
- **Zero installation** - No software to install or update
- **Instant startup** - Double-click and start working immediately
- **Publication ready** - SVG format scales perfectly for any publication
- **Offline capable** - Works without internet connection
- **Cross-platform** - Same experience on Windows, Mac, Linux
- **Version independent** - No compatibility issues or updates required

## License

This project is open source and available for academic and research use.

---

**💡 Pro tip:** Bookmark `eeg_electrode_selector_main_en.html` in your browser for instant access!