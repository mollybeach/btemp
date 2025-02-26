# BRKT READ ME

# Project Overview

## What is BRKT?
BRKT is an online platform that facilitates competitive gaming, prediction markets, and betting competitions. It integrates blockchain technology to provide a transparent, trustless betting experience.

(BRKT WEBSITE)[https://www.brkt.gg]

## How It Works

### Users Participate in Competitions
- Users can join competitions by placing bets using cryptocurrency.
- Custom competitions allow users to create and manage their own events.

### Blockchain Integration
- The platform uses Ethereum & Aptos blockchains for transparency.
- Ethers.js interacts with smart contracts for bet placements.
- Gas fees are managed via gas limits in competitions.

### Prediction Markets
- Users make periodic predictions on various topics (e.g., Bitcoin price, elections).
- Aggregated prediction data is stored to track accuracy over time.

### Raffles & Leaderboards
- Raffles allow users to buy tickets and win prizes.
- The leaderboard tracks top users based on betting success.

### Smart Contract Features
- Betting is trustless using smart contracts.
- Prize pools are distributed automatically based on results.

### Web3 User Interaction
- Users connect wallets (e.g., MetaMask).
- Betting and payments occur in crypto (ETH, USDC, etc.).

# Tech Stack
- **Frontend**: Next.js, React, TypeScript, Tailwind CSS
- **Backend**: Express.js, Firebase Firestore (NoSQL)
- **Blockchain**: Ethers.js, Aptos SDK
- **Networking**: GraphQL, Axios

# Key Features
- ✔ Blockchain-Powered Competitions
- ✔ Decentralized Betting & Predictions
- ✔ Smart Contract-Based Prize Pool Distribution
- ✔ Customizable Competitions & Events
- ✔ Periodic & Aggregated Prediction Tracking


# Setup Instructions

## Install Dependencies
```bash
yarn install --legacy-peer-deps
```

## Run Locally
```bash
yarn run dev
```

## Deploy to Firebase
```bash
firebase login
firebase deploy
```
## Tech Stack

### Frontend
- **React**: A JavaScript library for building user interfaces.
- **Next.js**: A React framework for server-side rendering and static site generation.
- **TypeScript**: A typed superset of JavaScript that compiles to plain JavaScript.
- **Tailwind CSS**: A utility-first CSS framework for rapid UI development.
- **Framer Motion**: A library for creating animations in React.

#### Backend
- **Express**: A minimal and flexible Node.js web application framework.
- **Firebase**: A platform developed by Google for creating mobile and web applications.

#### Networking
- **Axios**: A promise-based HTTP client for the browser and Node.js.
- **GraphQL**: A query language for your API, and a server-side runtime for executing queries.

#### Blockchain
- **Ethers**: A library for interacting with the Ethereum blockchain and its ecosystem.
- **Aptos**: A library for interacting with the Aptos blockchain.

#### UI Libraries
- **@mui/material**: A popular React UI framework.
- **@emotion/react** & **@emotion/styled**: Libraries for writing CSS styles with JavaScript.
- **@nextui-org/react**: A modern and beautiful React UI library.
- **@radix-ui/react-components**: A set of unstyled, accessible UI primitives for React.

#### Development Tools
- **ESLint**: A tool for identifying and fixing problems in JavaScript code.
- **PostCSS**: A tool for transforming CSS with JavaScript plugins.
- **Autoprefixer**: A PostCSS plugin to parse CSS and add vendor prefixes.

#### Additional Libraries
- **Zustand**: A small, fast, and scalable state-management solution.
- **React Query**: A library for fetching, caching, and updating asynchronous data in React.
- **React Beautiful DnD**: A library for beautiful and accessible drag and drop for lists.
- **React Router**: A collection of navigational components for React applications.

Join the excitement and participate in various competitions and events to earn rewards and engage with the community.

# Pages

These are the main route handlers for the application.

| Path                                   | File                                      | Description                                      |
|----------------------------------------|-------------------------------------------|--------------------------------------------------|
| /                                      | app/layout.tsx                           | Layout file for the main app structure.          |
| /competitions                          | app/competitions/page.tsx                | Displays all competitions.                        |
| /CompetitionBracket/:id                | app/CompetitionBracket/[competitionId]/page.tsx | Bracket view of a specific competition.          |
| /CreateCompetition                     | app/CreateCompetition/page.tsx           | Page for creating a new competition.             |
| /leaderboard                           | app/leaderboard/page.tsx                 | Displays rankings or leaderboard.                |
| /profile                               | app/profile/page.tsx                     | User profile page.                               |
| /profile/bets                          | app/profile/ProfileBets.tsx              | User's betting history.                          |
| /profile/details                       | app/profile/ProfileDetails.tsx           | Profile details of the user.                     |
| /profile/avatar-upload                 | app/profile/AvatarUpload.tsx             | Profile avatar upload.                           |
| /profile/referral-code                | app/profile/ReferralCodeGen.tsx          | Generates a referral code for the user.         |
| /event/:id                             | app/event/[id]/page.tsx                  | Detailed event view.                            |
| /events                                | app/events/page.tsx                      | Events listing page.                             |
| /raffle/:id                            | app/Raffle/[id]/page.tsx                | Specific raffle page.                            |
| /rewards                               | app/Rewards/page.tsx                     | Displays user rewards.                           |

# API Routes

Backend endpoints responsible for handling data and API interactions.

| API Endpoint                          | File                                      | Description                                      |
|---------------------------------------|-------------------------------------------|--------------------------------------------------|
| /api/bets/:walletAddress              | app/api/bets/[walletAddress]/route.ts    | Retrieves bets associated with a wallet.        |
| /api/bitget/1/:walletAddress          | app/api/bitget/1/[walletAddress]/route.ts| Fetches bitget transactions for wallet (type 1).|
| /api/bitget/3/:walletAddress          | app/api/bitget/3/[walletAddress]/route.ts| Fetches bitget transactions for wallet (type 3).|
| /api/bitget/5/:walletAddress          | app/api/bitget/5/[walletAddress]/route.ts| Fetches bitget transactions for wallet (type 5).|
| /api/utility                          | app/api/utility.ts                        | Utility functions for API interactions.         |
| /api/profile-redirect                 | app/api/profile-redirect.ts               | Redirect handler for user profiles.             |

# Components

Reusable UI components used across the project.

| Component Name                        | File                                      | Description                                      |
|---------------------------------------|-------------------------------------------|--------------------------------------------------|
| BracketPreview                        | BracketPreview.tsx                        | Displays a preview of the tournament bracket.   |
| Card                                  | Card.tsx                                  | General-purpose card UI component.               |
| CompetitionCard                       | CompetitionCard.tsx                       | Displays details of a competition.               |
| CompetitionPage                       | CompetitionPage.tsx                       | Page layout for a competition.                   |
| CompetitionSlider                     | CompetitionSlider.tsx                     | Displays a slider for competitions.              |
| CreateBracket                         | CreateBracket.tsx                         | UI for creating brackets.                        |
| CreateRaffle                          | CreateRaffle.tsx                          | UI for creating a raffle event.                 |
| DollarInputBox                        | DollarInputBox.tsx                        | Input box for entering dollar amounts.           |
| EntryPage                             | EntryPage.tsx                             | UI for event entry.                             |
| Event                                 | Event.tsx                                 | Handles event-specific interactions.             |
| EventCard                             | EventCard.tsx                             | Displays an event card.                          |
| EventsComponent                       | EventsComponent.tsx                       | Main component for handling events.              |
| EventsPage                            | EventsPage.tsx                            | Page displaying events.                          |
| Footer                                | Footer.tsx                                | Footer component.                                |
| GridViewComponent                     | GridViewComponent.tsx                     | Grid display component.                           |
| IPTracker                             | IPTracker.tsx                             | Tracks user IP addresses.                        |
| Leaderboard                           | Leaderboard.tsx                           | Leaderboard component.                           |
| LottiePlayer                          | LottiePlayer.tsx                          | Displays Lottie animations.                      |
| MarketInfoModal                       | MarketInfoModal.tsx                       | Market information modal.                        |
| Modal                                 | Modal.tsx                                 | Generic modal component.                         |
| ModalContent                          | ModalContent.tsx                          | Content wrapper for modals.                     |
| Navbar                                | Navbar.tsx                                | Navigation bar component.                        |
| Quantitypicker                        | Quantitypicker.tsx                        | Quantity selection component.                    |
| RaffleComponent                       | RaffleComponent.tsx                       | Handles raffle UI.                              |
| RichTextEditor                        | RichTextEditor.tsx                        | WYSIWYG text editor.                            |
| TableComponentlp                      | TableComponentlp.tsx                      | Table component for leaderboard pages.          |
| TableSection                          | TableSection.tsx                          | Generic table section.                          |
| Web3Provider                          | Web3Provider.tsx                          | Web3 provider for blockchain integration.       |
| WheelComponent                        | WheelComponent.tsx                        | Displays a spinning wheel for raffles.         |

# State Management (Context)

Global state management for the application.

| Context Name                          | File                                      | Description                                      |
|---------------------------------------|-------------------------------------------|--------------------------------------------------|
| Wallet Context                        | contexts/WalletContext.tsx                | Manages wallet connection state.                 |

# Utilities

Helper functions for data processing.

| Utility Name                          | File                                      | Description                                      |
|---------------------------------------|-------------------------------------------|--------------------------------------------------|
| addNotification                       | utils/addNotification.ts                  | Handles notifications.                           |
| openGraphImageResponse                | utils/openGraphImageResponse.tsx          | Generates Open Graph image responses.            |
| ActivityTracker                       | CompetitionBracket/[competitionId]/utils/ActivityTracker.ts | Tracks user activity.                           |
| betPriceHistoryData                  | CompetitionBracket/[competitionId]/utils/betPriceHistoryData.ts | Stores betting history.                          |
| EstimatedPayout                       | CompetitionBracket/[competitionId]/utils/EstimatedPayout.tsx | Calculates estimated payout.                     |


# Database Schema

The data structure provided suggests a Firebase Firestore NoSQL schema, where collections and documents store various data points. Below is the schema translated into relational database tables (for SQL-based databases) while maintaining Firestore's document-oriented structure.

## Tables and Schema

### 1. activities (User Activities)
| Column Name      | Data Type     | Description                             |
|------------------|---------------|-----------------------------------------|
| activity_id      | VARCHAR(255)  | Unique ID for the activity              |
| result           | FLOAT         | Outcome of the activity                 |
| avatar_url       | TEXT          | User profile image URL                  |
| username         | VARCHAR(255)  | Username of the user                    |
| timestamp        | TIMESTAMP     | Time of the activity                    |

### 2. aggregatedPeriodicPredictions
| Column Name      | Data Type     | Description                             |
|------------------|---------------|-----------------------------------------|
| id               | VARCHAR(255)  | Unique identifier                       |
| aggregatedStats   | JSON          | Aggregated statistics for predictions    |

### 3. aggregatedPredictions (Prediction Rounds)
| Column Name      | Data Type     | Description                             |
|------------------|---------------|-----------------------------------------|
| prediction_id    | VARCHAR(255)  | Unique ID for prediction                |
| round_0          | JSON          | Data for round 0                        |
| round_1          | JSON          | Data for round 1 (optional)            |
| round_2          | JSON          | Data for round 2 (optional)            |
| round_3          | JSON          | Data for round 3 (optional)            |

### 4. catSocietyWhitelist
| Column Name      | Data Type     | Description                             |
|------------------|---------------|-----------------------------------------|
| id               | VARCHAR(255)  | Unique ID for user                      |
| guaranteed       | BOOLEAN       | Whether the user is guaranteed access   |

### 5. competitions (Main Competitions)
| Column Name                | Data Type     | Description                             |
|----------------------------|---------------|-----------------------------------------|
| competition_id             | VARCHAR(255)  | Unique identifier for the competition   |
| game_type                  | VARCHAR(100)  | Type of game (e.g., sports, stocks)    |
| competition_title          | VARCHAR(255)  | Title of the competition                 |
| team_names                 | JSON          | List of participating teams              |
| total_points_per_round     | INT           | Points per round                         |
| team_count                 | INT           | Number of teams                          |
| starting_epoch             | INT           | Start timestamp (epoch format)          |
| gas_limit                  | BIGINT        | Gas limit for blockchain transactions    |
| competition_background      | TEXT          | Description of the competition           |
| expiration_epoch           | INT           | Expiration timestamp                     |
| image_url                  | TEXT          | Image representing the competition       |
| bracket_id                 | VARCHAR(255)  | ID of the competition bracket            |
| registration_fee_info       | JSON          | Details about registration fees           |
| has_finished               | BOOLEAN       | Indicates if the competition is finished |
| prize_pool                 | FLOAT         | Total prize pool                         |
| bettors                    | JSON          | Users betting on the competition         |
| bettors_count              | INT           | Number of bettors                        |

### 6. customCompetitions (User-Created Competitions)
| Column Name                | Data Type     | Description                             |
|----------------------------|---------------|-----------------------------------------|
| competition_id             | VARCHAR(255)  | Unique identifier for the competition   |
| game_type                  | VARCHAR(100)  | Type of game                            |
| has_finished               | BOOLEAN       | Status of competition completion        |
| team_names                 | JSON          | Teams involved                          |
| starting_epoch             | INT           | Start time (epoch)                     |
| expiration_epoch           | INT           | Expiration time                         |
| bracket_id                 | VARCHAR(255)  | Bracket ID for the competition          |
| rules                      | TEXT          | Rules of the competition                |
| image_url                  | TEXT          | Competition image URL                   |
| bettors                    | JSON          | List of bettors                         |
| bettors_count              | INT           | Number of participants                  |
| prize_pool                 | FLOAT         | Prize money                             |

### 7. raffles (Raffle System)
| Column Name                | Data Type     | Description                             |
|----------------------------|---------------|-----------------------------------------|
| raffle_id                  | UUID          | Unique raffle ID                        |
| title                      | VARCHAR(255)  | Title of the raffle                     |
| details                    | TEXT          | Description of the raffle               |
| rules                      | TEXT          | Rules of the raffle                     |
| creator                    | JSON          | Creator details                         |
| price_per_ticket           | FLOAT         | Ticket price                            |
| tickets_sold               | INT           | Number of tickets sold                  |
| image_url                  | TEXT          | Image for the raffle                    |
| start_date                 | TIMESTAMP     | Start time of the raffle                |
| end_date                   | TIMESTAMP     | End time of the raffle                  |
| total_likes                | INT           | Number of likes on the raffle           |

### 8. userSpendingSummaries (User Spending Data)
| Column Name                | Data Type     | Description                             |
|----------------------------|---------------|-----------------------------------------|
| user_id                    | VARCHAR(255)  | Unique user identifier                  |
| total_usd_spent            | FLOAT         | Total money spent by user               |

### 9. ethPriceSnapshots (ETH Price Tracking)
| Column Name                | Data Type     | Description                             |
|----------------------------|---------------|-----------------------------------------|
| timestamp                  | TIMESTAMP     | Time of snapshot                        |
| eth_price_usd              | FLOAT         | Price of ETH in USD                    |

### 10. leaderboard (Competition Rankings)
| Column Name                | Data Type     | Description                             |
|----------------------------|---------------|-----------------------------------------|
| leaderboard_7_days         | JSON          | Leaderboard for the last 7 days        |
| leaderboard_30_days        | JSON          | Leaderboard for the last 30 days       |
| last_updated               | TIMESTAMP     | Last updated time                       |

### 11. notifications
| Column Name                | Data Type     | Description                             |
|----------------------------|---------------|-----------------------------------------|
| notification_id            | VARCHAR(255)  | Unique ID for the notification          |
| image_url                  | TEXT          | Image associated with the notification   |
| bracket_id                 | VARCHAR(255)  | Bracket ID of the competition           |
| title                      | VARCHAR(255)  | Title of the notification               |
| message                    | TEXT          | Notification message                     |
| timestamp                  | TIMESTAMP     | Time of notification                    |

### 12. referrals
| Column Name                | Data Type     | Description                             |
|----------------------------|---------------|-----------------------------------------|
| referral_id                | VARCHAR(255)  | Unique referral code                    |
| creator                    | VARCHAR(255)  | Creator of the referral code            |
| used_by                   | VARCHAR(255)  | User who used the referral              |
| status                     | VARCHAR(100)  | Status of the referral                  |
| rewarded                   | BOOLEAN       | Whether the user was rewarded           |

# Conclusion
The BRKT platform is a blockchain-based prediction and betting marketplace. It provides users with:
- Competitive games & events
- Crypto-powered rewards
- Smart contract automation
- Transparent & decentralized betting

This makes it a unique Web3 gaming & prediction platform combining Ethereum, Aptos, and Firebase for a seamless experience.

## Project Structure

```
BRKTGG/
├── .git/
├── .next/
│   ├── server/
│   │   ├── app/
│   │   │   ├── CompetitionBracket/
│   │   │   │   └── [competitionId]/
│   │   │   │   │   ├── page_client-reference-manifest.js
│   │   │   │   │   └── page.js
│   │   │   ├── competitions/
│   │   │   │   ├── page_client-reference-manifest.js
│   │   │   │   └── page.js
│   │   │   └── CreateCompetition/
│   │   │   │   ├── page_client-reference-manifest.js
│   │   │   │   └── page.js
│   │   ├── vendor-chunks/
│   │   └── webpack-runtime.js
│   ├── static/
│   ├── types/
│   │   ├── app/
│   │   │   ├── CompetitionBracket/
│   │   │   │   └── [competitionId]/
│   │   │   │   │   ├── layout.ts
│   │   │   │   │   └── page.ts
│   │   │   ├── competitions/
│   │   │   │   └── page.ts
│   │   │   ├── CreateCompetition/
│   │   │   │   └── page.ts
│   │   │   └── layout.ts
│   │   ├── cache-life.d.ts
│   │   └── package.json
│   ├── app-build-manifest.json
│   ├── build-manifest.json
│   ├── package.json
│   ├── react-loadable-manifest.json
│   └── trace
├── ABI/
│   ├── CompetitionFactory.json
│   ├── ConditionalTokens.json
│   ├── ConditionalTokens.txt
│   ├── ERC20.json
│   ├── ERC20MockDecimals.json
│   ├── FixedProductMarketMaker.json
│   ├── FixedProductMarketMaker.txt
│   ├── FPMMDeterministicFactory.json
│   ├── PaidPredictableABI.json
│   └── router.json
├── components/
│   ├── ui/
│   │   ├── SheetSide.tsx
│   │   ├── toast.tsx
│   │   ├── toaster.tsx
│   │   └── use-toast.ts
│   ├── utils/
│   │   ├── .DS_Store
│   │   ├── addNotification.ts
│   │   ├── openGraphImageResponse.tsx
│   │   └── utils.ts
│   ├── .DS_Store
│   ├── BracketPreview.tsx
│   ├── Card.tsx
│   ├── CompetitionCard.tsx
│   ├── CompetitionPage.tsx
│   ├── CompetitionSlider.tsx
│   ├── CreateBracket.tsx
│   ├── CreateRaffle.tsx
│   ├── DollarInputBox.tsx
│   ├── EntryPage.tsx
│   ├── Event.tsx
│   ├── EventCard.tsx
│   ├── EventsComponent.tsx
│   ├── EventsPage.tsx
│   ├── Footer.tsx
│   ├── GridViewComponent.tsx
│   ├── IPTracker.tsx
│   ├── Leaderboard.tsx
│   ├── LottiePlayer.tsx
│   ├── MarketInfoModal.tsx
│   ├── Modal.tsx
│   ├── ModalContent.tsx
│   ├── Navbar.tsx
│   ├── Quantitypicker.tsx
│   ├── RaffleComponent.tsx
│   ├── RichTextEditor.tsx
│   ├── TableComponentlp.tsx
│   ├── TableSection.tsx
│   ├── utils.ts
│   ├── Web3Provider.tsx
│   └── WheelComponent.tsx
├── contexts/
│   └── WalletContext.tsx
├── functions/
│   ├── lib/
│   │   └── serviceAccountKey.json
│   ├── src/
│   │   └── index.ts
│   ├── .DS_Store
│   ├── .eslintrc.js
│   ├── .gitignore
│   ├── eslint.config.mjs
│   ├── firestore-debug.log
│   ├── package-lock.json
│   ├── package.json
│   ├── serviceAccountKey.json
│   ├── tsconfig.dev.json
│   ├── tsconfig.json
│   ├── ui-debug.log
│   └── yarn.lock
├── node_modules/
├── public/
│   ├── CatSociety/
│   │   ├── assets/
│   │   │   ├── bg.png
│   │   │   ├── BOX.png
│   │   │   ├── button.png
│   │   │   ├── card_back_red.png
│   │   │   ├── JokerButton.png
│   │   │   ├── middle.png
│   │   │   ├── playingCards.png
│   │   │   ├── playingCards.xml
│   │   │   └── titleScreen.png
│   └── win.mp3
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   ├── bets/
│   │   │   │   └── [walletAddress]/
│   │   │   │   │   └── route.ts
│   │   │   ├── bitget/
│   │   │   │   ├── 1/
│   │   │   │   │   └── [walletAddress]/
│   │   │   │   │   │   └── route.ts
│   │   │   │   ├── 3/
│   │   │   │   │   └── [walletAddress]/
│   │   │   │   │   │   └── route.ts
│   │   │   │   ├── 5/
│   │   │   │   │   └── [walletAddress]/
│   │   │   │   │   │   └── route.ts
│   │   │   │   └── utility.ts
│   │   │   ├── profile-redirect.ts
│   │   │   └── utility.ts
│   │   ├── CatSociety/
│   │   │   ├── EligibilityChecker/
│   │   │   │   ├── EligibilityChecker.tsx
│   │   │   │   ├── filteredSharedAddresses.tsx
│   │   │   │   └── page.tsx
│   │   │   ├── game/
│   │   │   │   ├── scenes/
│   │   │   │   │   ├── Boot.ts
│   │   │   │   │   ├── Game.ts
│   │   │   │   │   ├── GameOver.ts
│   │   │   │   │   ├── MainMenu.ts
│   │   │   │   │   └── Preloader.ts
│   │   │   │   ├── EventBus.ts
│   │   │   │   ├── main.ts
│   │   │   │   └── PhaserGame.tsx
│   │   │   ├── BlackJackApp.tsx
│   │   │   ├── CatApp.tsx
│   │   │   ├── modal.tsx
│   │   │   ├── moons.tsx
│   │   │   ├── page.tsx
│   │   │   ├── partnerData.tsx
│   │   │   └── theme.json
│   │   ├── CompetitionBracket/
│   │   │   ├── [competitionId]/
│   │   │   │   ├── utils/
│   │   │   │   │   ├── ActivityTracker.ts
│   │   │   │   │   ├── addNotification.ts
│   │   │   │   │   ├── betPriceHistoryData.ts
│   │   │   │   │   ├── EstimatedPayout.tsx
│   │   │   │   │   └── SwipeIndicator.tsx
│   │   │   │   ├── Activity.tsx
│   │   │   │   ├── BaseMarketButton.tsx
│   │   │   │   ├── BetPriceHistoryGraph.tsx
│   │   │   │   ├── BracketBetButton.tsx
│   │   │   │   ├── BracketSelection.tsx
│   │   │   │   ├── Chat.tsx
│   │   │   │   ├── ConditionalBetPanel.tsx
│   │   │   │   ├── CustomSeed.tsx
│   │   │   │   ├── Header.tsx
│   │   │   │   ├── layout.tsx
│   │   │   │   ├── MarketInteractionBox.tsx
│   │   │   │   ├── MarketResolutionPanel.tsx
│   │   │   │   ├── Modal.tsx
│   │   │   │   ├── ModalContent.tsx
│   │   │   │   ├── page.tsx
│   │   │   │   ├── SmallCard.tsx
│   │   │   │   ├── TabbedViewsComponent.tsx
│   │   │   │   ├── types.ts
│   │   │   │   ├── WalletButton.tsx
│   │   │   │   ├── WalletInfoBox.tsx
│   │   │   │   └── WalletSelectionModal.tsx
│   │   │   └── .DS_Store
│   │   ├── competitions/
│   │   │   └── page.tsx
│   │   ├── CreateCompetition/
│   │   │   └── page.tsx
│   │   ├── data/
│   │   │   ├── DataComponent.tsx
│   │   │   └── page.tsx
│   │   ├── event/
│   │   │   └── [id]/
│   │   │   │   ├── layout.tsx
│   │   │   │   └── page.tsx
│   │   ├── events/
│   │   │   └── page.tsx
│   │   ├── leaderboard/
│   │   │   └── page.tsx
│   │   ├── profile/
│   │   │   ├── AvatarUpload.tsx
│   │   │   ├── page.tsx
│   │   │   ├── ProfileBets.tsx
│   │   │   ├── ProfileComponent.tsx
│   │   │   ├── ProfileDetails.tsx
│   │   │   ├── ProfileUser.tsx
│   │   │   └── ReferralCodeGen.tsx
│   │   ├── Raffle/
│   │   │   └── [id]/
│   │   │   │   ├── utils/
│   │   │   │   │   └── addWinnerNotification.ts
│   │   │   │   └── page.tsx
│   │   ├── Rewards/
│   │   │   └── page.tsx
│   │   ├── .DS_Store
│   │   ├── config.ts
│   │   ├── globals.css
│   │   ├── layout.tsx
│   │   ├── opengraph-image.png
│   │   └── vanta.d.ts
│   ├── components/
│   │   └── ui/
│   │   │   ├── alert-dialog.tsx
│   │   │   ├── button.tsx
│   │   │   ├── card.tsx
│   │   │   ├── carousel.tsx
│   │   │   ├── dialog.tsx
│   │   │   ├── dropdown-menu.tsx
│   │   │   ├── input.tsx
│   │   │   ├── popover.tsx
│   │   │   ├── select.tsx
│   │   │   ├── sheet.tsx
│   │   │   ├── skeleton.tsx
│   │   │   ├── slider.tsx
│   │   │   ├── tabs.tsx
│   │   │   ├── textarea.tsx
│   │   │   └── tooltip.tsx
│   ├── hooks/
│   │   ├── useGoogleAnalytics.ts
│   │   └── useWhitelist.ts
│   ├── lib/
│   │   ├── config.ts
│   │   ├── constants.ts
│   │   └── utils.ts
│   └── .DS_Store
├── types/
│   ├── dummyData.ts
│   └── MarketDataTypes.tsx
├── .DS_Store
├── .env
├── .eslintrc.json
├── .firebaserc
├── .gitignore
├── components.json
├── firebase.json
├── firebaseConfig.ts
├── firestore-debug.log
├── next-env.d.ts
├── next.config.mjs
├── package.json
├── postcss.config.js
├── README.md
├── tailwind.config.ts
├── tsconfig.json
├── ui-debug.log
├── vercel.json
└── yarn.lock
```
