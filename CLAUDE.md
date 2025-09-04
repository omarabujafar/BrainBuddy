# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

BrainBuddy is a React Native application built with Expo and structured as a monorepo using npm workspaces. The project uses Expo Router for file-based navigation and TypeScript for type safety.

## Architecture

- **Monorepo Structure**: Uses npm workspaces with `apps/*` and `packages/*` (packages directory currently empty)
- **Mobile App**: Located in `apps/mobile/` - Expo React Native app with router-based navigation
- **Navigation**: Uses Expo Router with file-based routing in `app/` directory
- **UI Framework**: React Native with Expo SDK v53
- **State Management**: TanStack React Query for data fetching
- **Styling**: Built-in React Native StyleSheet with theme support (light/dark)

## Common Development Commands

### Mobile App Development (run from `apps/mobile/`)
```bash
cd apps/mobile
npm start              # Start Expo development server
npm run android        # Start on Android device/emulator  
npm run ios           # Start on iOS device/simulator
npm run web           # Start web version
npm test              # Run Jest tests in watch mode
```

### Root Level Commands
```bash
npm install           # Install dependencies for all workspaces
```

## Key Files and Directories

- `apps/mobile/app/` - Expo Router screens and layouts
- `apps/mobile/app/(tabs)/` - Tab-based navigation screens
- `apps/mobile/components/` - Reusable React components
- `apps/mobile/constants/Colors.ts` - Theme colors configuration
- `apps/mobile/assets/` - Images, fonts, and other static assets
- `app.json` - Expo configuration
- `babel.config.js` - Babel preset configuration for Expo
- `metro.config.js` - Metro bundler configuration

## Testing

- Uses Jest with `jest-expo` preset
- Test files located in `components/__tests__/`
- Run tests with `npm test` from the mobile app directory

## Platform Support

- iOS (bundle ID: com.yourname.brainbuddy)
- Android (package: com.yourname.brainbuddy)  
- Web (Metro bundler with static output)

## Development Notes

- TypeScript configuration extends `expo/tsconfig.base`
- Uses automatic UI style switching (light/dark)
- Splash screen and app icons configured in `app.json`
- Navigation uses typed routes (experimental feature enabled)