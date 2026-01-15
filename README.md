# 📊 Financial Dashboard - Currency & Stock Tracker

A comprehensive web application for tracking currency exchange rates and stock market information. Monitor USD/PLN and EUR/PLN rates, plus detailed financial metrics for multiple companies including daily charts, quarterly performance, and P/E ratios.

## 🎯 Features

### Currency Exchange Tracking
- **USD/PLN and EUR/PLN rates**: Real-time display of exchange rates
- **Change indicators**: Visual indicators showing daily percentage changes
- **Manual updates**: Easy-to-use interface for updating rates
- **Color-coded changes**: Green for positive, red for negative movements

### Stock Market Dashboard
- **Company tracking**: Add and monitor multiple companies
- **Daily price charts**: Interactive 30-day price trend visualization using Chart.js
- **Quarterly metrics**:
  - Revenue (last quarter) with Q/Q change
  - Net Income with Q/Q change
  - Cash per Share with Q/Q change
- **Valuation ratios**:
  - Trailing P/E ratio
  - Forward P/E ratio
- **Full CRUD operations**: Add, edit, view, and remove companies

### Data Persistence
- **LocalStorage**: All data is saved locally in your browser
- **Persistent updates**: Changes remain after page refresh
- **Default examples**: Includes sample data for Apple Inc. and CD Projekt

## 🚀 How to Run

### Option 1: Direct Browser Access
Simply open `index.html` in any modern web browser. No installation required.

### Option 2: Local Web Server

Using Python 3:
```bash
python -m http.server 8000
```

Using Python 2:
```bash
python -m SimpleHTTPServer 8000
```

Using Node.js:
```bash
npx http-server
```

Then navigate to `http://localhost:8000` in your browser.

## 📖 How to Use

### Currency Management

1. **View rates**: Currency cards display current exchange rates
2. **Update rates**: Click "Update Rate" button on any currency card
3. **Edit values**: Enter new rate and percentage change
4. **Save changes**: Click "Save" to update (automatically stored)

### Stock Management

1. **Add company**: Click "+ Add Company" button
2. **Enter details**:
   - Company name and ticker symbol
   - Last quarter revenue ($M)
   - Revenue Q/Q change (%)
   - Net Income ($M)
   - Net Income Q/Q change (%)
   - Cash per Share ($)
   - Cash per Share Q/Q change (%)
   - Trailing P/E ratio
   - Forward P/E ratio
   - Daily chart data (30 comma-separated price points)
3. **Edit company**: Click "Edit Data" on any stock card
4. **Remove company**: Click the "×" button in top-right corner

### Chart Data Format

When adding or editing a company, enter daily prices as comma-separated values:
```
150.2,151.5,149.8,152.3,154.1,153.7,155.2,156.8,...
```

Enter approximately 30 price points for a complete month view. If left blank, random data will be generated.

## 🎨 Visual Design

- **Modern UI**: Clean, professional financial dashboard aesthetic
- **Gradient backgrounds**: Purple gradient backdrop
- **Responsive cards**: Hover effects and smooth transitions
- **Color indicators**:
  - Green (▲) for positive changes
  - Red (▼) for negative changes
- **Interactive charts**: Hover over charts to see exact prices
- **Modal dialogs**: Clean forms for editing data

## 💡 Technical Details

### Technologies Used
- **Pure HTML/CSS/JavaScript**: No framework dependencies
- **Chart.js**: Professional charting library for price visualization
- **LocalStorage API**: Browser-based data persistence
- **Responsive Grid Layout**: Adapts to different screen sizes
- **CSS Animations**: Smooth transitions and hover effects

### Browser Compatibility
- Works in all modern browsers (Chrome, Firefox, Safari, Edge)
- Requires JavaScript enabled
- Requires LocalStorage support

### Data Structure

**Currency Object:**
```javascript
{
  pair: 'USD/PLN',
  rate: 4.0245,
  change: -0.35
}
```

**Stock Object:**
```javascript
{
  id: 1234567890,
  name: 'Apple Inc.',
  ticker: 'AAPL',
  revenue: 89537,
  revenueChange: 2.1,
  netIncome: 22956,
  netIncomeChange: 10.8,
  cashPerShare: 3.85,
  cashChange: -2.5,
  trailingPE: 29.5,
  forwardPE: 27.2,
  chartData: [172.5, 173.2, ...]
}
```

## 📊 Default Data

The application comes pre-loaded with example data:

### Currency Rates
- **USD/PLN**: 4.0245 (-0.35%)
- **EUR/PLN**: 4.3122 (+0.12%)

### Stock Examples
- **Apple Inc. (AAPL)**: Complete financial metrics and 30-day chart
- **CD Projekt (CDR)**: Polish gaming company example

## 🔧 Customization

### Adding More Currency Pairs
Edit the `initializeDefaultData()` function in index.html to add more currency pairs:

```javascript
currencies = [
  { pair: 'USD/PLN', rate: 4.0245, change: -0.35 },
  { pair: 'EUR/PLN', rate: 4.3122, change: 0.12 },
  { pair: 'GBP/PLN', rate: 5.1234, change: 0.45 }  // Add new pairs
];
```

### Changing Chart Colors
Modify the Chart.js configuration in the `createChart()` function:

```javascript
borderColor: '#667eea',  // Line color
backgroundColor: 'rgba(102, 126, 234, 0.1)',  // Fill color
```

### Styling Modifications
All styles are contained in the `<style>` section. Key CSS variables:
- Primary color: `#667eea`
- Positive change: `#28a745`
- Negative change: `#dc3545`

## 🌟 Use Cases

- **Personal finance**: Track your investment portfolio
- **Forex trading**: Monitor currency pair movements
- **Stock research**: Compare company financials side-by-side
- **Financial education**: Learn about P/E ratios and quarterly metrics
- **Demo purposes**: Showcase financial data visualization

## 📱 Mobile Responsive

The dashboard automatically adapts to mobile devices:
- Single-column layout on small screens
- Touch-friendly buttons and inputs
- Scrollable modals for data entry
- Readable text at all sizes

## 🔒 Privacy

- **No external API calls**: All data stays on your device
- **No tracking**: No analytics or third-party scripts (except Chart.js CDN)
- **Local-only storage**: Data never leaves your browser
- **Offline capable**: Works without internet (after initial load)

## 🎓 Educational Value

Learn about key financial metrics:
- **Trailing P/E**: Price-to-Earnings ratio based on past 12 months
- **Forward P/E**: P/E ratio based on estimated future earnings
- **Q/Q Change**: Quarter-over-Quarter growth percentage
- **Revenue**: Total income from business operations
- **Net Income**: Profit after all expenses
- **Cash per Share**: Company's cash divided by shares outstanding

## 🚀 Future Enhancement Ideas

- Integration with real-time financial APIs
- Export data to CSV/Excel
- Historical data tracking
- Alerts for price changes
- Multiple portfolio support
- Dark mode toggle
- Chart timeframe selection (7d, 30d, 90d)
- Financial news integration
- Performance comparison tools

## 📄 License

This project is open source and available for personal and educational use.

## 🤝 Contributing

Feel free to fork and enhance this dashboard. Some areas for improvement:
- API integration for live data
- Additional financial metrics
- Advanced charting options
- Data import/export features
- Multi-currency support

---

**Stay informed about your investments!** 📈💰
