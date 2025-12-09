# NetAnaliza Amazon Content Manager

**Google Apps Script tool for Amazon listing optimization - Direct SP-API integration**

## 🎯 About

This tool is specifically designed for **NetAnaliza** to provide Amazon listing optimization services to clients.

### Key Features:

- ✅ **Direct SP-API connection** (no Cloud Functions required)
- ✅ **Multi-seller support** - switch marketplace and credentials per operation
- ✅ **Standalone** - only needs SP-API credentials
- ✅ **Import, edit, export** Amazon products
- ✅ **Full support** for A+ Content, Images, Pricing, Inventory
- ✅ **Everything in Google Sheets**

## 🔗 Links

- **Based on:** [LUKOAmazonContentManager](https://github.com/LUKOAI/LUKOAmazonContentManager)
- **Difference:** Direct SP-API (no Cloud Functions needed)
- **Target:** Client services - listing optimization for multiple Amazon sellers

## 🆚 NetAnaliza vs LUKO

| Feature | LUKO | NetAnaliza (this project) |
|---------|------|---------------------------|
| Architecture | Apps Script + Cloud Functions | Apps Script + Direct SP-API |
| Infrastructure | Requires Cloud Function setup | Standalone - credentials only |
| Seller Management | Single seller | Multi-seller support |
| Marketplace Switch | Static config | Dynamic per operation |
| Target Audience | Internal LUKO use | Client services |
| Complexity | Higher (2 components) | Lower (1 component) |

## 🚀 Features

### Import
- Import products by ASIN (single/batch)
- Search products by keyword
- Import pricing (Pricing API)
- Import inventory (FBA Inventory API)
- Import A+ Content
- Import product dimensions
- API connection test

### Export
- Export products (Partial/Full Update)
- Export A+ Content (Basic & Premium)
- Field Selector (choose specific fields)
- Bulk operations
- Export images
- Export prices and promotions

### Management
- Create coupons
- Manage promotions
- Brand Content Management
- GPSR Compliance
- Product documents

## 📦 Installation

### Requirements:
1. Google Account
2. Amazon SP-API Credentials (Client ID, Secret, Refresh Token)
3. Marketplace configuration

### Steps:

1. **Copy files to Google Apps Script:**
   - Open Google Sheets
   - Extensions → Apps Script
   - Copy all files from `apps-script/` folder
   - Save

2. **Configure in Google Sheets:**
   - Open Config sheet
   - Enter SP-API Credentials
   - Select default Marketplace

3. **Generate sheets:**
   - Menu → Tools → Generate Full Spreadsheet

## 🔧 Configuration

### Config Sheet

| Parameter | Example | Description |
|----------|---------|-------------|
| `LWA Client ID` | `amzn1.application-oa2-client...` | SP-API Client ID |
| `LWA Client Secret` | `amzn1.oa2-cs.v1...` | SP-API Client Secret |
| `Refresh Token` | `Atzr\|...` | OAuth Refresh Token |
| `Marketplace` | `DE`, `FR`, `UK`, etc. | Default marketplace |

## 📚 Documentation

- **Full documentation:** [NOWE_FUNKCJE.md](NOWE_FUNKCJE.md)
- **Deployment instructions:** [DEPLOY_INSTRUCTIONS.md](DEPLOY_INSTRUCTIONS.md)

## 🔄 Workflow

1. **Import products:**
   - Menu → Import → Import by ASIN(s)
   - Enter ASINs (comma separated)
   - Products imported to "ImportedProducts" sheet

2. **Edit in sheet:**
   - Edit Title, Bullets, Description, Images
   - Check products to export

3. **Export to Amazon:**
   - Menu → Export → Export Products (Advanced)
   - Choose: Partial/Full Update
   - Select fields to export (optional)
   - Direct export via SP-API

4. **Verification:**
   - Check Status column
   - Review Logs sheet

## 🛠️ Development

### Project Structure:

