# GeoAventura Mundial

![License](https://img.shields.io/badge/license-MIT-green)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white)
![Platform](https://img.shields.io/badge/platform-Web-orange)
![Next.js](https://img.shields.io/badge/Next.js-15-000000?logo=nextdotjs&logoColor=white)

> A fun, interactive web game to learn world geography through flags and countries.

## Overview

GeoAventura Mundial is an educational game that tests your knowledge of world
geography. Players must identify countries based on their flags, choosing from
multiple answers. The app includes more than 190 countries and offers a
gamified learning experience with light/dark themes and AI integration powered
by Google Gemini 2.0 Flash.

![webpreview](https://github.com/user-attachments/assets/eb6988ff-a884-42b5-8408-3291041dab96)

## Features

- Interactive flag-quiz game with immediate feedback on each answer
- Complete country database: 190+ countries with names in Spanish and English
- Customizable quizzes: choose the number of questions (5-190)
- Score tracking: correct and incorrect answers, final results review
- Modern responsive UI built with Tailwind CSS and Radix UI
- Light and dark mode with persisted theme preference
- AI integration via Google Gemini 2.0 Flash (Genkit)
- High performance: built with Next.js 15 (Turbopack) and React 18

## Tech Stack

- **Next.js 15** — React framework (App Router, Turbopack)
- **React 18** + **TypeScript 5**
- **Tailwind CSS** + **Radix UI** + **Lucide React** (icons)
- **Genkit** + **@genkit-ai/googleai** (Google Gemini 2.0 Flash)
- React Hook Form, Recharts, next-themes
- Tooling: ESLint, Prettier, Husky

## Requirements

- Node.js 18+
- npm, yarn, pnpm, or bun
- A Google AI API key (for the Genkit/Gemini features)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/JoanMike/GeoAventura_Mundial_Game.git
   cd GeoAventura_Mundial_Game
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

## Configuration

Create a `.env.local` file in the project root and add your Google AI API key:

```bash
GOOGLE_AI_API_KEY=your_api_key_here
```

## Usage

Start the development server (runs on port 9002 with Turbopack):

```bash
npm run dev
```

Then open [http://localhost:9002](http://localhost:9002) in your browser.

Available scripts:

- `npm run dev` — start the dev server with Turbopack (port 9002)
- `npm run build` — build the app for production
- `npm run start` — start the production server
- `npm run lint` — run ESLint
- `npm run typecheck` — run the TypeScript type checker
- `npm run format` — format the code with Prettier
- `npm run genkit:dev` — start the Genkit dev server
- `npm run genkit:watch` — start Genkit in watch mode

### How to play

1. Select the number of questions you want to answer (minimum 5) and click
   "Comenzar Juego".
2. A country flag is shown — pick the correct country name among 4 options.
3. At the end, review your total score and every answer, and play again.

## Project Structure

```text
src/
├── ai/                 # AI configuration (Genkit)
│   ├── genkit.ts       # Main Genkit configuration
│   └── dev.ts          # AI development entry point
├── app/                # Next.js App Router
│   ├── layout.tsx      # Root layout
│   ├── page.tsx        # Main game page
│   └── globals.css     # Global styles
├── components/         # React components
│   ├── game/           # Game-specific components
│   │   ├── GameSetup.tsx    # Game setup screen
│   │   ├── GamePlay.tsx     # Gameplay interface
│   │   └── GameResults.tsx  # Results screen
│   ├── ui/             # Reusable UI components
│   └── theme-*.tsx     # Theme provider and toggle
├── hooks/              # Custom React hooks
└── lib/                # Utilities and business logic
    ├── countries.ts    # Country database
    ├── gameLogic.ts    # Game logic
    └── utils.ts        # General utilities
```

## License

Distributed under the **MIT License**. See [LICENSE](LICENSE) for the full
license text.

Copyright (c) 2025 Jose Miguel Maldonado Garcia

## Author

**Jose Miguel Maldonado Garcia** — [@JoanMike](https://github.com/JoanMike)
