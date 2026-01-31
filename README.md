# 📚 Library Management Mobile App

A comprehensive React Native mobile application for library management, built with Expo and featuring role-based access control, book browsing, and reservation systems.

## 🚀 Features

### User Features
- **📱 Cross-platform Support**: iOS, Android, and Web
- **🔐 Secure Authentication**: Clerk-powered authentication with email/password
- **📖 Book Discovery**: Browse available books with detailed information
- **⭐ Book Details**: View comprehensive book information including author, pages, language, and reading time estimates
- **📋 Book Reservations**: Request and track book borrowings
- **👤 User Profile**: Manage personal information and view borrowing history
- **🎨 Modern UI**: Beautiful interface with NativeWind (Tailwind CSS) styling

### Admin Features
- **➕ Book Management**: Add new books to the library catalog
- **✏️ Book Editing**: Modify existing book information
- **📊 Request Management**: Review and approve/deny borrowing requests
- **👥 User Management**: Oversee user activities and permissions

### Technical Features
- **🗄️ Database Integration**: Neon PostgreSQL database
- **📱 Responsive Design**: Optimized for all screen sizes
- **🔄 Real-time Updates**: Live data synchronization
- **🎯 Type Safety**: Full TypeScript implementation
- **🧪 Testing Ready**: Jest testing framework configured

## 🛠️ Tech Stack

- **Framework**: [Expo](https://expo.dev) (~52.0.26)
- **Language**: TypeScript
- **Navigation**: Expo Router with file-based routing
- **Authentication**: [Clerk](https://clerk.com) for user management
- **Database**: [Neon PostgreSQL](https://neon.tech) with serverless SQL
- **Styling**: [NativeWind](https://nativewind.dev) (Tailwind CSS for React Native)
- **UI Components**: React Native with custom components
- **Icons**: Expo Vector Icons & React Native Vector Icons
- **State Management**: React hooks and context
- **Testing**: Jest with Expo testing preset

## 📋 Prerequisites

Before running this project, make sure you have:

- **Node.js** (v18 or later)
- **npm** or **yarn**
- **Expo CLI** (`npm install -g @expo/cli`)
- **iOS Simulator** (for iOS development on macOS)
- **Android Studio** (for Android development)
- **Expo Go app** (for testing on physical devices)

## 🚀 Installation & Setup

1. **Clone the repository**
   ```bash
   git clone [repository-url]
   cd MobileRepoGroupe
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   Create a `.env` file in the root directory with:
   ```env
   DATABASE_URL=your_neon_database_url
   CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   ```

4. **Start the development server**
   ```bash
   npm start
   # or
   npx expo start
   ```

5. **Run on specific platforms**
   ```bash
   # iOS Simulator
   npm run ios
   
   # Android Emulator
   npm run android
   
   # Web Browser
   npm run web
   ```

## 📱 Development

### Available Scripts

- `npm start` - Start the Expo development server
- `npm run android` - Run on Android emulator/device
- `npm run ios` - Run on iOS simulator/device
- `npm run web` - Run in web browser
- `npm test` - Run Jest tests
- `npm run lint` - Run ESLint
- `npm run reset-project` - Reset to blank project

### Project Structure

```
MobileRepoGroupe/
├── app/                    # Main application code (Expo Router)
│   ├── (api)/             # API routes
│   │   ├── book+api.ts    # Book management endpoints
│   │   ├── user+api.ts    # User management endpoints
│   │   └── booking/       # Booking-related endpoints
│   ├── (auth)/            # Authentication screens
│   │   ├── sign-in.tsx    # Login screen
│   │   └── sign-up.tsx    # Registration screen
│   ├── (tabs)/            # User tab navigation
│   │   ├── home.tsx       # Main book browsing
│   │   ├── profile.tsx    # User profile
│   │   └── bookDetail.tsx # Book details view
│   ├── (tabsAdmin)/       # Admin tab navigation
│   │   ├── addBook.tsx    # Add new books
│   │   ├── ModifyBook.tsx # Edit existing books
│   │   └── home.tsx       # Admin dashboard
│   ├── _layout.tsx        # Root layout
│   └── index.tsx          # Entry point
├── components/            # Reusable UI components
│   ├── BookCard.tsx       # Book display component
│   ├── CustomButton.tsx   # Styled button component
│   ├── InputField.tsx     # Form input component
│   ├── PendingCard.tsx    # Pending request component
│   └── RequestDetail.tsx  # Request details component
├── constants/             # App constants and themes
├── types/                 # TypeScript type definitions
├── lib/                   # Utility libraries
├── assets/                # Images, fonts, and icons
└── data/                  # Mock/dummy data
```

## 🔑 Authentication

The app uses Clerk for authentication with:
- Email/password authentication
- Secure token storage (Expo SecureStore)
- Role-based access control (User/Admin)
- Automatic token refresh and management

## 🗄️ Database Schema

The application uses Neon PostgreSQL with the following main entities:
- **Users**: User profiles and authentication data
- **Books**: Library catalog with book information
- **Bookings**: Reservation and borrowing records
- **Categories**: Book categorization (if applicable)

## 🎨 Styling

The app uses NativeWind (Tailwind CSS) for styling with:
- Custom color palette (primary, secondary, accent colors)
- Responsive design utilities
- Custom font family support (Roboto family)
- Consistent spacing and typography

## 📱 Features in Detail

### For Library Users
1. **Browse Books**: View available books with covers, titles, authors
2. **Search & Filter**: Find books by various criteria
3. **Book Details**: Complete information including reading time estimates
4. **Make Reservations**: Request to borrow books
5. **Track Status**: Monitor reservation and borrowing status
6. **Profile Management**: Update personal information

### For Administrators
1. **Catalog Management**: Add, edit, and remove books
2. **Request Processing**: Approve or deny borrowing requests
3. **User Oversight**: View user activities and manage accounts
4. **Analytics Dashboard**: Overview of library statistics

## 🧪 Testing

Run the test suite:
```bash
npm test
```

The project includes Jest configuration for:
- Unit testing components
- API endpoint testing
- Integration testing
- Snapshot testing

## 🚀 Deployment

### Production Build
```bash
# Create production build
expo build

# For iOS
expo build:ios

# For Android
expo build:android
```

### Distribution
- **App Store**: Submit iOS builds to Apple App Store
- **Google Play**: Submit Android builds to Google Play Store
- **Expo Updates**: Over-the-air updates for published apps

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:
- 📧 Email: [your-email@example.com]
- 🐛 Issues: [GitHub Issues](link-to-issues)
- 📖 Documentation: [Project Wiki](link-to-wiki)

## 🙏 Acknowledgments

- [Expo](https://expo.dev) for the amazing development platform
- [Clerk](https://clerk.com) for authentication services
- [Neon](https://neon.tech) for serverless PostgreSQL
- [NativeWind](https://nativewind.dev) for styling solution

---

Made with ❤️ for efficient library management
