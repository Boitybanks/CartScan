# 🛒 CartScan

> **Shop Smart. Scan Every Item.**

CartScan is an Android shopping companion that gives you a live running total as you pick items off the shelf — so you're never surprised by the bill at the till. Link your loyalty cards and watch your discounts and points update in real time.

---

## ✨ Features

- 📷 **Instant barcode scanning** — point, scan, done. Cart updates in under a second
- 💳 **Multi-loyalty card support** — Pick n Pay Smart Shopper, Checkers Xtra Savings, Woolworths WRewards, Clicks ClubCard
- 💰 **Live discount calculation** — see your loyalty price vs shelf price side by side
- ⭐ **Points tracker** — know exactly how many points you're earning this trip
- 📋 **Session history** — review your last 10 shopping trips
- ✈️ **Offline mode** — core scanning works even without internet

---

## 🖥️ Tech Stack

| Layer | Technology |
|---|---|
| Framework | Flutter 3.x (Dart) |
| State Management | Riverpod |
| Local Database | Drift (SQLite) |
| Barcode Scanning | mobile_scanner |
| HTTP Client | Dio |
| Secure Storage | flutter_secure_storage |
| Analytics | Firebase Analytics |

---

## 🚀 Getting Started

### Prerequisites

- Flutter SDK `>=3.0.0`
- Dart SDK `>=3.0.0`
- Android Studio or VS Code with Flutter extension
- Android device or emulator running **Android 9.0 (API 28)+**

### Installation

```bash
# Clone the repo
git clone https://github.com/your-org/cartscan.git
cd cartscan

# Install dependencies
flutter pub get

# Run on connected device
flutter run
```

### Environment Setup

Create a `.env` file in the project root (copy from `.env.example`):

```env
PRODUCT_API_BASE_URL=https://your-product-api.com
FIREBASE_PROJECT_ID=your-firebase-project-id
```

> **Never commit your `.env` file.** It's already in `.gitignore`.

---

## 📁 Project Structure

```
cartscan/
├── lib/
│   ├── main.dart
│   ├── app/                   # App-level config, routing, theme
│   ├── features/
│   │   ├── scanner/           # Barcode scan screen & logic
│   │   ├── cart/              # Cart state, item list, totals
│   │   ├── loyalty/           # Loyalty card setup & rule engine
│   │   ├── history/           # Session history
│   │   └── settings/          # User preferences
│   ├── shared/
│   │   ├── models/            # Data models
│   │   ├── services/          # API, DB, secure storage services
│   │   └── widgets/           # Reusable UI components
├── assets/
│   ├── images/
│   └── loyalty_rules/         # JSON config for loyalty discount rules
├── test/
├── android/
└── pubspec.yaml
```

---

## 🏪 Supported Retailers

| Retailer | Loyalty Card | Discounts | Points |
|---|---|---|---|
| Pick n Pay | Smart Shopper | ✅ | ✅ |
| Checkers / Shoprite | Xtra Savings | ✅ | ➖ |
| Woolworths | WRewards | ✅ | ✅ |
| Clicks | ClubCard | ✅ | ✅ |

---

## 🗺️ Roadmap

- [x] Project spec & architecture
- [ ] Flutter scaffold & navigation
- [ ] Barcode scanner integration
- [ ] Product lookup (API + local cache)
- [ ] Cart state management
- [ ] Loyalty card setup UI
- [ ] Discount rule engine (all 4 retailers)
- [ ] Session summary & history
- [ ] Dark mode & accessibility pass
- [ ] Play Store beta release
- [ ] Retailer partnership integrations

---

## 🤝 Contributing

This is a personal group project. If you're on the team:

1. Branch off `main` using the format `feature/your-feature-name`
2. Keep PRs small and focused — one feature or fix per PR
3. Write widget tests for any new UI components
4. Run `flutter analyze` and `flutter test` before opening a PR
5. Tag a teammate for review — no self-merging into `main`

---

## 🔒 Security & Privacy

- Loyalty card numbers are stored **encrypted on-device only** using `flutter_secure_storage`
- No personally identifiable information is ever sent to CartScan servers
- Analytics are anonymised and aggregated via Firebase

---

## 📄 License

This project is private and not licensed for public distribution at this stage.

---

## 👥 Team

Built with ❤️ by the CartScan crew [ Sibongakonke, Mpilo and Boitumelo] — a side project born out of one too many awkward moments at the till.

---

*CartScan v1.0 — Android — South Africa 🇿🇦*
