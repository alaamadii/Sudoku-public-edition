# Sudoku Mobile App (React Native + Expo)

A modern Sudoku game built with React Native, Expo, TypeScript, and Zustand.

This project includes classic Sudoku gameplay, multiple difficulty levels, a daily challenge mode, persistent game state, and logic tests for puzzle generation/solving.
![My Image](photo.png)

## Features

- 9x9 Sudoku board with cell selection and number input
- Difficulty levels:
  - Easy (30 empty cells)
  - Medium (40 empty cells)
  - Hard (50 empty cells)
- Mistake system (game over at 3 mistakes)
- In-game timer and best-time tracking
- Daily challenge mode with deterministic seeded puzzle per day
- Continue active game after app restart (persisted local state)
- coins counter to help when lose
- Settings:
  - Dark mode toggle
  - Highlight errors toggle
  - Highlight same numbers toggle
  - Sound effects toggle
- Stats screen with wins, losses, games played, and win rate
- Restart current puzzle and start a new game flows

## Tech Stack

- React Native (0.83)
- Expo (SDK 55)
- TypeScript
- React Navigation (Native Stack + Bottom Tabs)
- Zustand + AsyncStorage persistence
- Node built-in test runner with tsx for Sudoku logic tests

## Project Structure

```text
sudoku/
  app/
    src/
      components/     # UI blocks (board, cells, number pad)
      screens/        # App screens (home, game, settings, stats, etc.)
      hooks/          # Custom hooks (timer, game logic, theme)
      store/          # Zustand stores (game + settings)
      utils/          # Sudoku generator, solver, validator
      types/          # Shared TypeScript types/constants
```

## Prerequisites

Install the following before running the app:

- Node.js (LTS recommended)
- npm (comes with Node.js)
- Expo Go on Android/iOS (for running on a physical device)
- Optional:
  - Android Studio (Android emulator)
  - Xcode on macOS (iOS simulator)

## Getting Started

1. Clone the repository:

```bash
git clone <your-repo-url>
cd sudoku/app
```

2. Install dependencies:

```bash
npm install
```

3. Start the Expo dev server:

```bash
npm run start
```

4. Run on your preferred platform:

```bash
npm run android
npm run ios
npm run web
```

## Available Scripts

From the `app` folder:

- `npm run start` - Start Expo dev server
- `npm run android` - Open on Android
- `npm run ios` - Open on iOS
- `npm run web` - Open in browser
- `npm run typecheck` - Run TypeScript checks
- `npm run test:logic` - Run Sudoku generator/solver logic tests

## Testing

Logic tests live under:

- `app/src/utils/__tests__/sudokuLogic.test.ts`

Run tests with:

```bash
cd app
npm run test:logic
```

## Notes

- App and settings state are persisted locally using AsyncStorage.
- Daily challenge puzzles are generated using a date-based seed, there is potintial to put play with frined server.

## Future Enhancements

- Leaderboard integration
- Achievements/badges system
- Expanded daily challenge tracking (streaks)
- Polishing sound/theme customization
- play against friends


# Try the game : https://sudokubyalaa.netlify.app
