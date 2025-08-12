# SPD Database Management Guide

This guide explains how to use Excel to manage your SPD product database and keep the SPD Wizard web application updated.

## 📊 **Excel Database Structure**

The CSV template includes these columns:

| Column | Description | Example |
|--------|-------------|---------|
| **Type** | SPD category | Type 1, Type 2 |
| **System_Voltage_Configuration** | Complete voltage/phase specification | "120V Single Phase", "277/480 3 phase wye" |
| **Protection_Modes** | Comma-separated protection modes (optional) | "Line to Line, Line to Neutral, Line to Ground" |
| **MCOV** | Maximum continuous operating voltage | "150V", "320/600" |
| **Max_Surge_Current_Rating** | Maximum surge current capacity | "160kA", "400kA" |
| **VP_Line_to_Line** | Voltage protection Line to Line | "600", "N/A" |
| **VP_Line_to_Neutral** | Voltage protection Line to Neutral | "700V" |
| **VP_Line_to_Ground** | Voltage protection Line to Ground | "700V" |
| **VP_Neutral_to_Ground** | Voltage protection Neutral to Ground | "700V" |
| **EMI_RFI_Filters** | EMI/RFI filtering capability | Yes, No |
| **Enclosure_Protection_Level** | NEMA enclosure rating | "NEMA 12/4", "NEMA 4X" |
| **SPD_Name_Product_Number** | Product name/model number | "ADSi-080-120T" |
| **SPD_Type** | UL classification | "Type I", "Type II" |
| **Description** | Product description (optional) | "Professional surge protection device" |
| **Product_Link** | Link to product page | https://shopalltec.com/adsi-080/ |
| **Data_Sheet** | Link to datasheet PDF | https://store.../datasheet.pdf |

## 🔄 **Workflow: Excel to Web App**

### Step 1: Open Excel Template
1. Open `SPD_Database_Template.csv` in Microsoft Excel
2. The file will load with sample data and proper column headers

### Step 2: Add Your SPD Products
1. **Add new rows** for each SPD product in your catalog
2. **Fill in all columns** with accurate product information
3. **Use consistent values** for Application and Phase_Type (see valid values below)
4. **Update URLs** to point to your actual website pages

### Step 3: Save and Convert
1. **Save as CSV** format (keep the .csv extension)
2. Open `csv-to-js-converter.html` in your web browser
3. **Upload your CSV file** using drag-and-drop or file selection
4. **Click "Convert to JavaScript"** to generate the code
5. **Copy the generated JavaScript** code

### Step 4: Update Web Application
1. Open `script.js` in a text editor
2. **Find the `spdDatabase` object** (around line 2)
3. **Replace the entire object** with your copied JavaScript code
4. **Save the file** and test your SPD Wizard

## ✅ **Valid Values Reference**

### Type Categories
- `Type 1` - Service entrance level SPDs
- `Type 2` - Panel level SPDs

### System Voltage Configuration (exact strings)
- `120V Single Phase`
- `120/240 split phase`
- `120/208 3 phase wye`
- `127/220 3 phase wye`
- `240 single phase`
- `220/380 3 phase wye`
- `240 3 phase delta`
- `240/415 3 phase wye`
- `240 High leg 3 phase`
- `277/480 3 phase wye`
- `480 3 phase delta`
- `347/600 3 phase wye`
- `600 3 phase delta`

### MCOV Values
- `150`, `180`, `320`, `150/320`, `420`, `550`, `600`, `680`, `690`

### Max Surge Current Rating
- `36kA`, `40kA`, `50kA`, `100kA`, `160kA`, `200kA`, `300kA`, `320kA`, `400kA`, `480kA`

### Voltage Protection Values (0V to 3400V in 100V increments)
- Use `N/A` for non-applicable protection modes
- Values: `0`, `100`, `200`, `300`, `400`, `500`, `600`, `700V`, etc.

### Protection Modes (comma-separated, optional)
- `Line to Line` - Protection between line conductors
- `Line to Neutral` - Protection between line and neutral
- `Line to Ground` - Protection between line and ground
- `Neutral to Ground` - Protection between neutral and ground

### SPD Type (UL Classification)
- `Type I` - Service entrance level protection
- `Type II` - Panel level protection

### EMI/RFI Filters
- `Yes` - Includes EMI/RFI filtering capability
- `No` - No EMI/RFI filtering

### Enclosure Protection Levels
- `NEMA 12/4` - Industrial, watertight
- `NEMA 12` - Industrial, dust protection
- `Polycarbonate NEMA 4X` - Corrosion resistant polycarbonate
- `NEMA 4X` - Corrosion resistant, watertight

### Voltage Values
Enter **numbers only**: 120, 208, 240, 277, 480, 600, etc.

## 🎯 **Best Practices**

### Data Quality
- **Double-check technical specifications** - MCOV, surge ratings, etc.
- **Use consistent formatting** for prices ($XX format)
- **Write clear descriptions** that highlight key benefits
- **List features separated by commas** for proper parsing

### URL Management
- **Use absolute URLs** (https://yourcompany.com/...)
- **Test all links** before publishing
- **Use placeholder URLs** (#datasheet-MODEL) if pages don't exist yet
- **Keep URLs consistent** across similar products

### Organization Tips
- **Group products by application** for easier management
- **Use descriptive model numbers** that indicate voltage/application
- **Sort by voltage within each application** for logical ordering
- **Add comments** in Excel to track product status or notes

## 🔧 **Maintenance Schedule**

### Regular Updates
- **Monthly**: Review pricing and availability
- **Quarterly**: Add new products and discontinue old ones
- **Annually**: Review all technical specifications and descriptions

### Version Control
- **Keep dated backups** of your CSV files
- **Document major changes** in Excel comments
- **Test the web app** after each update

## 🚨 **Troubleshooting**

### Common Issues
1. **CSV won't convert**: Check for missing commas or quotes in descriptions
2. **Products not showing**: Verify Application and Phase_Type values match exactly
3. **Features not displaying**: Ensure features are comma-separated without extra spaces
4. **Links not working**: Check URLs are complete and properly formatted

### Data Validation
- **Use Excel data validation** to restrict Application and Phase_Type values
- **Format price columns** consistently
- **Check for empty required fields** before converting

## 📈 **Future Enhancements**

This Excel-based system can be extended with:
- **Automated price updates** from your ERP system
- **Inventory integration** to show availability
- **Compliance tracking** for certifications and standards
- **Multi-language support** for international markets

---

**Need Help?** This system is designed to be maintained by non-technical staff while keeping the web application automatically updated. 