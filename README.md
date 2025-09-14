# � Crypto Trade Calculator

A **modern, feature-rich web application** that helps users track cryptocurrency trades and calculate tax liabilities using the **FIFO (First In, First Out)** method. With **real-time prices**, **dynamic coin support**, and **beautiful UI**, it's your complete crypto trading companion.

🔗 **Live App:** [Crypto_Trade_Calculator](https://crypto-trade-calculator.surge.sh)

> ⚡ Now featuring **thousands of cryptocurrencies** with dynamic loading and enhanced UI!

---

## 🚀 Features

### 💼 Core Trading Features
- ✅ **Add/Edit/Delete Crypto Trades** (Buy/Sell) with intuitive forms
- 🎯 **Dynamic Cryptocurrency Support** - Access to **thousands of coins** from CoinGecko
- 📈 **Live Price Integration** with one-click price fetching
- 💰 **Smart Price Display** - Live market prices for popular cryptocurrencies
- 🧮 **Current Holdings Tracker** with real-time valuation

### 📊 Advanced Calculations
- 📄 **Professional FIFO Tax Calculation** with detailed breakdown:
  - Total Gain/Loss tracking
  - Cost Basis calculation
  - Proceeds analysis
  - Individual trade profit/loss
- 🎯 **Investment Projection Calculator** - Visualize potential profits/losses
- 📋 **Comprehensive Trade History** with sortable data

### 🎨 Modern UI/UX
- 🌙 **Dark/Light Mode Toggle** with smooth animations
- � **Fully Responsive Design** - Perfect on all devices
- ✨ **Beautiful Gradients & Animations** with modern card layouts
- 🎭 **Interactive Elements** with hover effects and loading states
- 🏷️ **API Status Indicators** (Free Tier / Premium API Active)

### 📂 Export & Reporting
- 📊 **Professional CSV Export** (for tax software integration)
- 📄 **Detailed Text Summary Reports** with comprehensive analysis
- 💾 **Auto-save functionality** with localStorage persistence
- 🔄 **Data import/export** capabilities

### ⚡ Performance Features
- 🚀 **Optimized API Calls** with intelligent rate limiting
- 🎯 **Popular Coins Priority** for faster loading
- 🔄 **Background Data Loading** with loading indicators
- 💾 **Efficient State Management** for smooth user experience

---

## 🛠 Tech Stack

| Technology       | Purpose                         | Version |
|------------------|---------------------------------|---------|
| **React + Vite** | Frontend Framework + Dev Tools  | Latest  |
| **TypeScript**   | Static Type Checking & Safety   | 5.x     |
| **Tailwind CSS** | Responsive UI & Modern Styling  | 3.x     |
| **Lucide React** | Beautiful Icon Library          | Latest  |
| **CoinGecko API**| Live Crypto Prices & Coin Data  | v3      |
| **Vercel**       | Hosting & Serverless Deployment | -       |
| **LocalStorage** | Client-side Data Persistence    | Native  |

### 🎯 Key Technical Highlights
- **Component-based Architecture** with reusable UI elements
- **Type-safe Development** with comprehensive TypeScript interfaces
- **Responsive Design** with mobile-first approach
- **Performance Optimized** with lazy loading and efficient re-renders
- **Modern ES6+** features with async/await patterns

---

## ⚙️ How It Works

### 🎯 Core Workflow
1. **Select from Thousands of Cryptos** - Dynamic loading of all available cryptocurrencies from CoinGecko
2. **Add Trades Easily** - Intuitive form with live price fetching and validation
3. **Automatic FIFO Calculation** - Real-time computation of gains/losses using tax-compliant methods
4. **Visual Analytics** - Beautiful cards showing profits, losses, and portfolio health
5. **Investment Projections** - Calculate potential future profits with the projection calculator
6. **Professional Reports** - Export comprehensive data for tax filing or analysis

### 🔄 Data Flow
```
User Input → Dynamic Coin Loading → Live Price Fetching → FIFO Calculation → 
Real-time Updates → Visual Dashboard → Export Reports
```

### 🧮 FIFO Tax Logic
- **Buy orders** are queued chronologically (oldest first)
- **Sell orders** automatically match against the oldest available buy lots
- **Remaining quantities** are tracked for partial sales
- **Gain/Loss calculation** is computed as: `(Sell Price - Buy Price) × Quantity`
- **Cost basis** and **proceeds** are maintained for tax reporting accuracy

---

## 🧑‍💻 Setup Instructions

### 📋 Prerequisites
- **Node.js** (v16.0.0 or higher)
- **npm** or **yarn** package manager
- Modern web browser (Chrome, Firefox, Safari, Edge)

### 1. 📥 Clone the Repository

```bash
git clone https://github.com/nakuljain2011/Crypto-Tax-Calculator.git
cd Crypto-Tax-Calculator
```

### 2. 📦 Install Dependencies

```bash
npm install
# or
yarn install
```

### 3. 🔑 Configure API Key (Optional but Recommended)

For enhanced features and better rate limits, get a free API key from [CoinGecko](https://www.coingecko.com/en/api/pricing):

1. **Sign up** for a free account at [CoinGecko API](https://www.coingecko.com/en/api/pricing)
2. **Get your API key** from the dashboard
3. **Create environment file**:
   ```bash
   # Create .env file in project root
   touch .env
   ```
4. **Add your API key**:
   ```env
   VITE_COINGECKO_API_KEY=your_api_key_here
   ```

#### 🆚 API Key Benefits

| Feature | Without API Key | With API Key |
|---------|----------------|--------------|
| **Rate Limit** | 30 calls/minute | 10,000 calls/month |
| **Coin Support** | Popular coins only | All available coins |
| **Reliability** | Basic | Enhanced |
| **Performance** | Standard | Optimized |

### 4. 🚀 Run Development Server

```bash
npm run dev
# or
yarn dev
```

The app will be available at: `http://localhost:5173`

### 5. 🏗️ Build for Production

```bash
npm run build
# or
yarn build
```

### 6. 📊 Preview Production Build

```bash
npm run preview
# or
yarn preview
```

---

## � Deployment

### 🌐 Vercel Deployment (Recommended)

This project is optimized for **Vercel** deployment with zero configuration:

1. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Ready for deployment"
   git push origin main
   ```

2. **Deploy on Vercel**:
   - Visit [vercel.com](https://vercel.com)
   - Import your GitHub repository
   - Configure build settings:
     - **Build Command**: `npm run build`
     - **Output Directory**: `dist`
     - **Install Command**: `npm install`
   - Add environment variables (if using API key)
   - Deploy! ✨

3. **Environment Variables on Vercel**:
   - Go to Project Settings → Environment Variables
   - Add: `VITE_COINGECKO_API_KEY` = `your_api_key_here`

#### 🛠️ Vercel Deployment Troubleshooting

**If deployment fails with TypeScript errors:**

1. **Ensure TypeScript files are properly configured**
2. **Test build locally first**: `npm run build`
3. **Check that all files are committed to Git**
4. **Verify Node.js version** (use Node.js 18+ for best compatibility)

**Common fixes:**
- Clear Vercel build cache and redeploy
- Check that `tsconfig.app.json` includes all source files
- Ensure no TypeScript syntax errors in the code

### 🏗️ Alternative Deployment Options

| Platform | Support | Notes |
|----------|---------|--------|
| **Netlify** | ✅ Full | Add build command: `npm run build` |
| **GitHub Pages** | ⚠️ Limited | Static hosting, no server-side features |
| **Firebase Hosting** | ✅ Full | Requires Firebase CLI setup |
| **AWS S3 + CloudFront** | ✅ Full | Manual setup required |

---

## 📖 Usage Guide

### 🎯 Getting Started
1. **Add Your First Trade**: Click "Add New Trade" and fill in the details
2. **Use Live Prices**: Click the "Live" button to fetch current market prices
3. **Track Your Portfolio**: View your holdings in the "Current Holdings" section
4. **Calculate Projections**: Use the Investment Projection Calculator for future scenarios
5. **Export Reports**: Download CSV or TXT reports for your records

### 💡 Pro Tips
- **Enable Dark Mode** for better viewing in low light
- **Use the API key** for access to all cryptocurrencies
- **Regular backups**: Export your data regularly as a backup
- **Price accuracy**: Use live prices for the most accurate calculations
- **Multiple currencies**: The app displays prices in INR (Indian Rupees)

### 🔧 Troubleshooting

| Issue | Solution |
|-------|----------|
| **No prices loading** | Check internet connection, verify API key |
| **Coin not found** | Ensure you have an API key for full coin access |
| **Data not saving** | Check if browser allows localStorage |
| **Export not working** | Update to latest browser version |

### 🚨 Deployment Issues

#### Vercel TypeScript Build Errors
If you encounter TypeScript configuration errors during Vercel deployment:

**Error**: `No inputs were found in config file '/vercel/path0/tsconfig.app.json'`

**Solutions**:
1. **Update tsconfig.app.json** - Ensure proper include patterns:
   ```json
   {
     "include": [
       "src/**/*",
       "src/**/*.ts", 
       "src/**/*.tsx"
     ],
     "exclude": ["node_modules", "dist"]
   }
   ```

2. **Check file structure** - Ensure all TypeScript files are in the `src` directory

3. **Verify Vite config** - Make sure `vite.config.ts` has proper build settings:
   ```typescript
   export default defineConfig({
     plugins: [react()],
     build: {
       outDir: 'dist',
       sourcemap: false,
       minify: 'esbuild',
     },
     base: './',
   })
   ```

4. **Test build locally** before deploying:
   ```bash
   npm run build
   npm run preview
   ```

#### Environment Variables
- Add `VITE_COINGECKO_API_KEY` in Vercel project settings
- Redeploy after adding environment variables

#### Build Command Issues
If Vercel can't find the build command:
- Build Command: `npm run build`
- Output Directory: `dist`
- Install Command: `npm install`

---

## 🏗️ Project Structure

```
crypto-tax-calculator/
├── public/                 # Static assets
├── src/
│   ├── assets/            # Images, icons
│   ├── CryptoTaxCalculator.tsx  # Main component
│   ├── main.tsx           # Entry point
│   ├── index.css          # Global styles
│   └── vite-env.d.ts      # TypeScript declarations
├── .env.example           # Environment variables template
├── .gitignore            # Git ignore rules
├── index.html            # HTML template
├── package.json          # Dependencies and scripts
├── tailwind.config.js    # Tailwind CSS configuration
├── tsconfig.json         # TypeScript configuration
└── vite.config.ts        # Vite configuration
```

---

## 🧪 Development

### 🔧 Available Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Run ESLint
npm run type-check   # Check TypeScript types
```

### 🎨 Customization

The project uses **Tailwind CSS** for styling. Key customization points:

- **Colors**: Modify `tailwind.config.js` for brand colors
- **Animations**: Custom animations in `src/index.css`
- **Gradients**: Crypto-specific gradients in `getCryptoGradient()` function
- **API Integration**: Modify API endpoints in the fetch functions

### 🐛 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

---

## 📚 Technical Learnings & Challenges

### 🧠 Key Learnings
- **Advanced React Patterns**: Implemented complex state management with hooks
- **TypeScript Mastery**: Built type-safe interfaces for financial calculations
- **API Integration**: Efficient handling of external APIs with error boundaries
- **Performance Optimization**: Optimized for large datasets and real-time updates
- **UI/UX Design**: Created intuitive interfaces for complex financial data
- **Build Optimization**: Configured Vite for optimal production builds

### 🎯 Technical Challenges Solved
- **FIFO Algorithm Implementation**: Complex queue management for tax calculations
- **Dynamic Data Loading**: Efficiently loading thousands of cryptocurrencies
- **Rate Limiting**: Smart API call management to avoid hitting limits
- **State Synchronization**: Keeping UI in sync with complex financial calculations
- **Cross-browser Compatibility**: Ensuring consistent experience across platforms
- **Mobile Responsiveness**: Optimizing complex layouts for mobile devices

### 🏆 Architecture Decisions
- **Component Composition**: Modular design for maintainability
- **Type Safety**: Comprehensive TypeScript interfaces for data integrity
- **Performance First**: Lazy loading and efficient re-renders
- **User Experience**: Intuitive design with helpful loading states and error handling

---

## ✨ Future Enhancements

### 🚀 Planned Features
- 🔐 **User Authentication** - Cloud storage for trades across devices
- 📊 **Advanced Analytics** - Portfolio performance charts and insights
- � **PDF Reports** - Professional PDF generation for tax filing
- 🌍 **Multi-currency Support** - USD, EUR, and other fiat currencies
- 🏛️ **Tax Regime Selection** - Support for different countries' tax rules
- 📱 **Mobile App** - Native mobile applications
- 🔄 **Exchange Integration** - Import trades directly from exchanges
- 📈 **Advanced Charting** - Technical analysis tools
- 🤖 **AI Insights** - Smart recommendations and analysis
- 🔔 **Price Alerts** - Notifications for price movements

### 💡 Enhancement Ideas
- **Batch Import** - CSV/Excel trade import functionality
- **Portfolio Rebalancing** - Automated portfolio optimization suggestions
- **DeFi Integration** - Support for DeFi protocols and yield farming
- **NFT Tracking** - Non-fungible token portfolio management
- **Staking Rewards** - Track staking rewards and income
- **Mining Income** - Mining reward calculations and tracking

---

## 🙏 Acknowledgements

### 🛠️ Technologies & Services
- **[CoinGecko API](https://www.coingecko.com/)** - Comprehensive cryptocurrency data
- **[Lucide Icons](https://lucide.dev/)** - Beautiful, consistent icon library
- **[Tailwind CSS](https://tailwindcss.com/)** - Utility-first CSS framework
- **[Vercel](https://vercel.com/)** - Seamless deployment platform
- **[Vite](https://vitejs.dev/)** - Lightning-fast build tool

### 🌟 Inspiration
- Open-source finance tools community
- Modern web design trends
- User feedback and suggestions
- Cryptocurrency trading community needs

### 💝 Special Thanks
- Contributors and beta testers
- The React and TypeScript communities
- Crypto enthusiasts who provided valuable feedback

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 🤝 Support

### 🆘 Getting Help
- 🐛 **Issues**: [GitHub Issues](https://github.com/nakuljain2011/Crypto-Tax-Calculator/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/nakuljain2011/Crypto-Tax-Calculator/discussions)
- 📧 **Email**: For private inquiries

### ⭐ Show Your Support
If you found this project helpful:
- ⭐ **Star the repository**
- 🍴 **Fork and contribute**
- 📢 **Share with others**
- 💝 **Consider sponsoring**

---

<div align="center">

**Built with ❤️ for the crypto community**

[⬆️ Back to Top](#-crypto-trade-calculator)

</div>

