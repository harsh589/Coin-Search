<div align="center">

# 🪙 Coin Search

### A sleek, real-time cryptocurrency tracking app built with React & the CoinGecko API

Browse the top 50 coins by market cap, view live prices & 24h changes, and drill into detailed stats for any coins.

<br />

<!-- Badges -->
![React](https://img.shields.io/badge/React-18.2.0-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)
![Repo Size](https://img.shields.io/github/repo-size/harsh589/Coin-Search?style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/harsh589/Coin-Search?style=flat-square)

</div>

---

## 📖 Table of Contents

- [✨ Features](#-features)
- [🖼️ Preview](#️-preview)
- [🛠️ Tech Stack](#️-tech-stack)
- [📂 Project Structure](#-project-structure)
- [🚀 Getting Started](#-getting-started)
- [📜 Available Scripts](#-available-scripts)
- [🔌 API Reference](#-api-reference)
- [🧭 Roadmap](#-roadmap)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [👤 Author](#-author)
- [🙏 Acknowledgements](#-acknowledgements)

---

## ✨ Features

- 📊 **Live Market Data** — Fetches the top 50 cryptocurrencies ranked by market cap in real time.
- 💰 **At-a-Glance Pricing** — Current price, 24h change, trading volume, and market cap in a clean tabular layout.
- 🔍 **Detailed Coin View** — Click any coin to see an in-depth page with rank, price stats, and description.
- 📈 **Multi-Timeframe Changes** — Price change percentages across `1h`, `24h`, `7d`, `14d`, `30d`, and `1yr`.
- 🧾 **Rich Coin Info** — 24h high/low, market cap, circulating supply, and a sanitized "About" section.
- 🛡️ **Safe HTML Rendering** — Coin descriptions are sanitized with **DOMPurify** to prevent XSS.
- 📱 **Responsive Design** — Non-essential columns gracefully hide on smaller screens (`hide-mobile`).
- ⚡ **SPA Navigation** — Fast, seamless routing powered by **React Router**.

---

## 🛠️ Tech Stack

| Category      | Technology |
| ------------- | ---------- |
| **Framework** | [React 18](https://react.dev/) (bootstrapped with [Create React App](https://create-react-app.dev/)) |
| **Routing**   | [React Router DOM v6](https://reactrouter.com/) |
| **HTTP Client** | [Axios](https://axios-http.com/) |
| **Icons**     | [React Icons](https://react-icons.github.io/react-icons/) |
| **Security**  | [DOMPurify](https://github.com/cure53/DOMPurify) |
| **Styling**   | CSS3 |
| **Data Source** | [CoinGecko API](https://www.coingecko.com/en/api) |
| **Testing**   | [React Testing Library](https://testing-library.com/) + [Jest](https://jestjs.io/) |

---

## 📂 Project Structure

```text
Coin-Search/
├── public/                 # Static assets and HTML template
├── src/
│   ├── components/
│   │   ├── Coins.js        # Renders the list of coins + table headings
│   │   ├── CoinItem.js     # Single row: rank, symbol, price, 24h, volume, mkt cap
│   │   ├── Coins.css       # Styling for the coin list
│   │   ├── Navbar.js       # Top navigation bar with logo
│   │   └── Navbar.css      # Navbar styling
│   ├── routes/
│   │   ├── Coin.js         # Detailed single-coin page
│   │   └── Coin.css        # Coin details page styling
│   ├── App.js              # App root: fetches coins & defines routes
│   ├── index.js            # React entry point
│   └── index.css           # Global styles
├── package.json
└── README.md
```

---

## 🚀 Getting Started

Follow these steps to run the project locally.

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v14 or higher recommended)
- npm (comes with Node.js) or [yarn](https://yarnpkg.com/)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/harsh589/Coin-Search.git
   ```

2. **Navigate into the project directory**
   ```bash
   cd Coin-Search
   ```

3. **Install dependencies**
   ```bash
   npm install
   ```

4. **Start the development server**
   ```bash
   npm start
   ```

5. **Open the app**

   Visit [http://localhost:3000](http://localhost:3000) in your browser. 🎉

---

## 📜 Available Scripts

In the project directory, you can run:

| Command | Description |
| ------- | ----------- |
| `npm start` | Runs the app in development mode at `http://localhost:3000`. |
| `npm run build` | Builds the app for production into the `build` folder. |
| `npm test` | Launches the test runner in interactive watch mode. |
| `npm run eject` | Ejects from Create React App (⚠️ one-way operation). |

---

## 🔌 API Reference

This project uses the free **[CoinGecko API](https://www.coingecko.com/en/api)** — no API key required.

**Get top 50 coins by market cap** (used on the home page):
```http
GET https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=50&page=1&sparkline=false
```

**Get details for a single coin** (used on the coin details page):
```http
GET https://api.coingecko.com/api/v3/coins/{coinId}
```

---

## 🧭 Roadmap

Some ideas for future enhancements:

- [ ] 🔎 Add a search bar to filter coins by name/symbol
- [ ] 📄 Add pagination or infinite scroll for more than 50 coins
- [ ] 📉 Integrate price history charts (e.g. Chart.js / Recharts)
- [ ] 🌙 Add a dark/light theme toggle
- [ ] ⭐ Add a favorites/watchlist feature
- [ ] 💱 Support multiple fiat currencies

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Feel free to check the [issues page](https://github.com/harsh589/Coin-Search/issues) if you'd like to help out.

---

## 📄 License

This project is distributed under the **MIT License**. See the `LICENSE` file for more information.

> ℹ️ _No `LICENSE` file exists in the repo yet — consider adding one to make the terms official._

---

## 👤 Author

**harsh589**

- GitHub: [@harsh589](https://github.com/harsh589)

---

## 🙏 Acknowledgements

- [CoinGecko](https://www.coingecko.com/) for the free and generous crypto API
- [Create React App](https://create-react-app.dev/) for the project scaffold
- [React Icons](https://react-icons.github.io/react-icons/) for the icon set

<div align="center">

---

⭐ **If you found this project helpful, consider giving it a star!** ⭐

Made with ❤️ and ⚛️ React

</div>
