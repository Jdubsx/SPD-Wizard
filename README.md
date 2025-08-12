# SPD Wizard

A professional web application for selecting the perfect Surge Protection Device (SPD) for electrical systems. Built for Alltec to help engineers and electricians find optimal surge protection solutions based on their specific requirements.

## Features

- **Multi-step Wizard Interface**: Intuitive step-by-step form for gathering system requirements
- **Dynamic Form Controls**: Voltage protection selectors appear only when relevant protection modes are selected
- **Advanced Filtering**: Search by system voltage, MCOV, surge current rating, SPD type, and more
- **Professional Results Display**: Clean card-based layout showing device specifications and actions
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **CSV Database Management**: Easy-to-use converter for updating the SPD database from Excel/CSV files

## Quick Start

1. **Clone the repository**
   ```bash
   git clone [your-repo-url]
   cd spd-wizard
   ```

2. **Open the application**
   - Simply open `index.html` in your web browser
   - No server setup required - it's a pure client-side application

3. **Start using the wizard**
   - Fill out the system requirements step by step
   - Get personalized SPD recommendations based on your specifications

## File Structure

```
spd-wizard/
├── index.html              # Main application page
├── script.js               # Application logic and SPD database
├── styles.css              # Professional styling and responsive design
├── csv-to-js-converter.html # Database management tool
├── Assets/
│   └── Alltec_Logo_RGB.png # Company logo
├── SPD_Database_Template.csv # Template for database updates
└── SPD_Database_Management_Guide.md # Documentation for database management
```

## Usage

### For End Users

1. **System Information**: Enter your electrical system's voltage and configuration
2. **Protection Requirements**: Select required protection modes and specify ratings
3. **Additional Filters**: Choose SPD type, MCOV, surge current rating, and enclosure level
4. **Get Results**: View recommended SPDs with detailed specifications
5. **Access Resources**: Click device cards to view datasheets and product information

### For Database Management

1. Open `csv-to-js-converter.html` in your browser
2. Prepare your SPD data using the provided CSV template
3. Upload your CSV file to the converter
4. Copy the generated JavaScript code
5. Replace the `spdDatabase` object in `script.js` with the new code

## Technical Details

- **Pure HTML/CSS/JavaScript**: No frameworks or build tools required
- **Responsive Design**: Mobile-first approach with professional styling
- **Modern Browser Support**: Uses ES6+ features and modern CSS
- **Accessible**: Semantic HTML and keyboard navigation support
- **Performance Optimized**: Efficient search algorithms and minimal dependencies

## Database Structure

The SPD database is organized hierarchically:
```
spdDatabase
├── Type 1
│   ├── [Voltage]
│   │   ├── [Phase Configuration]
│   │   │   └── [Array of SPD Objects]
└── Type 2
    ├── [Voltage]
    │   ├── [Phase Configuration]
    │   │   └── [Array of SPD Objects]
```

Each SPD object contains:
- Product name and specifications
- Voltage protection ratings
- Technical parameters (MCOV, surge current, etc.)
- Links to datasheets and product pages

## Browser Compatibility

- **Chrome**: 80+
- **Firefox**: 75+
- **Safari**: 13+
- **Edge**: 80+

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is proprietary software developed for Alltec. All rights reserved.

## Support

For technical support or questions about the SPD Wizard, please contact the development team or refer to the included documentation files.

---

**Built with ⚡ by Alltec Engineering Team**