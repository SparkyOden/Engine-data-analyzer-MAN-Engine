# Engine Data Analyzer

A standalone HTML application for analyzing and visualizing engine measurement data from Excel files. This tool provides an intuitive interface for viewing time-series engine data with interactive charts and filtering capabilities.

![Engine Data Analyzer](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## Features

- 📊 **Interactive Charts** - Visualize engine measurements with line or bar charts
- 📈 **Multi-Metric Comparison** - Display multiple measurements simultaneously
- ⏱️ **Time Period Filtering** - Focus on specific time ranges with slider controls
- 🔍 **Engine Serial Display** - Automatically extracts and displays engine serial number
- 📋 **Data Table View** - View raw measurement data in an organized table
- 💻 **Standalone Application** - No installation required, runs entirely in your browser
- 🔒 **Privacy-Focused** - All data processing happens locally in your browser

## Usage

### Quick Start

1. Download the `engine-analyzer.html` file
2. Open it in any modern web browser (Chrome, Firefox, Safari, Edge)
3. Click the upload area or drag and drop your Excel file
4. Select measurements to visualize and adjust the time range as needed

### Excel File Format Requirements

Your Excel file must follow this specific structure:

| Location | Content | Description |
|----------|---------|-------------|
| **Cell B3** | Engine Serial Number | The unique identifier for the engine |
| **Row 10 (Columns B→)** | Time Values | Time points for each measurement (e.g., timestamps, intervals) |
| **Column A (Row 11→)** | Measurement Names | Names/descriptions of each measurement type |
| **Columns B→ (Row 11→)** | Measurement Data | The actual measurement values |

#### Example Excel Structure:

```
Row 1-2:  [Header information - ignored]
Row 3:    [A: Label] [B: ENGINE-12345] [C: ...] [D: ...]
Row 4-9:  [Additional metadata - ignored]
Row 10:   [A: Time] [B: 10:00] [C: 10:01] [D: 10:02] [E: 10:03]
Row 11:   [A: Temperature] [B: 75] [C: 76] [D: 77] [E: 78]
Row 12:   [A: Pressure] [B: 100] [C: 102] [D: 101] [E: 103]
Row 13:   [A: Speed] [B: 1500] [C: 1550] [D: 1600] [E: 1650]
```

## Features in Detail

### Chart Visualization
- Toggle between **Line Chart** and **Bar Chart** views
- Multiple measurements displayed with different colors
- Interactive tooltips showing exact values
- Responsive design that works on all screen sizes

### Time Period Filtering
- Use dual sliders to select start and end points
- Real-time chart updates as you adjust the range
- View selected time range and data point count

### Measurement Selection
- Checkbox interface for easy metric selection
- Select one or multiple measurements to compare
- Color-coded visualization for each metric

### Data Table
- View up to 20 rows of filtered data
- Selected measurements highlighted in the table
- Sticky time column for easy reference

## Browser Compatibility

- ✅ Chrome/Edge (version 90+)
- ✅ Firefox (version 88+)
- ✅ Safari (version 14+)
- ✅ Opera (version 76+)

## Technical Details

### Built With
- **Chart.js** (v3.9.1) - Chart rendering
- **SheetJS/xlsx** (v0.18.5) - Excel file parsing
- Pure JavaScript (ES6+)
- No framework dependencies

### Data Processing
- All data processing occurs in the browser
- No data is sent to external servers
- Excel files are parsed using the SheetJS library
- Charts rendered using Chart.js

## Privacy & Security

- **100% Client-Side**: All data processing happens in your browser
- **No Data Upload**: Your Excel files never leave your computer
- **No Tracking**: No analytics or tracking code included
- **Offline Capable**: Works without internet connection (after initial load)

## Troubleshooting

### File won't upload
- Ensure the file is in `.xlsx` or `.xls` format
- Check that the file isn't corrupted
- Verify the file structure matches the requirements

### Chart not displaying
- Make sure at least one measurement is selected
- Check that your Excel file has data in the correct format
- Ensure row 10 contains time values and row 11+ contains measurements

### Data appears incorrect
- Verify that cell B3 contains the engine serial number
- Check that row 10 (columns B onwards) contains your time values
- Ensure column A (row 11 onwards) contains measurement names
- Confirm measurement data starts at column B, row 11

## Contributing

Contributions are welcome! Feel free to:
- Report bugs by opening an issue
- Suggest new features
- Submit pull requests with improvements

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Chart.js team for the excellent charting library
- SheetJS team for the robust Excel parsing library
- All contributors and users of this tool

## Support

If you encounter any issues or have questions:
1. Check the Troubleshooting section above
2. Review the Excel format requirements
3. Open an issue on GitHub with details about your problem

---

**Made with ❤️ for engine data analysis**
