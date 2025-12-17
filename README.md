# Use-Popcorn

Use-Popcorn is an internal frontend React application built to practice and demonstrate core React concepts such as state management, hooks, side effects, API fetching, and browser storage.

This project focuses on real-world React patterns rather than production-ready architecture and is intended for internal learning and development purposes.

---

## 1. Tech Stack

- React.js
- JavaScript (ES6+)
- Create React App
- Node.js and npm
- OMDb API (external movie data source)
- Browser LocalStorage

---

## 2. Installation

### 2.1 Prerequisites

- Node.js (v14 or higher recommended)
- npm

### 2.2 Setup

1. Clone the repository

```bash
git clone https://github.com/cozocozy/use-popcorn.git
cd use-popcorn

Install dependencies

npm install


Run the development server

npm start


Open the application in your browser

http://localhost:3000

3. Project Structure
use-popcorn/
├── public/                 Static public assets
├── src/
│   ├── components/         Reusable UI components
│   ├── App.js              Main application logic
│   ├── index.js            Application entry point
│   └── index.css           Global styles
├── package.json
└── README.md

4. Features and Implementation

4.1 Movie Fetching using OMDb API
Movie data is fetched dynamically from the OMDb API
Fetching is triggered when the search query changes
Side effects are handled using useEffect
Asynchronous logic is implemented using async and await

Concepts used:
useEffect
API fetching
Side-effect management

4.2 Loading State Handling
A loading indicator is displayed while data is being fetched
Prevents empty or flickering UI
Improves user experience during API requests
Implementation detail:
An isLoading state is set before and after fetch execution

4.3 error Handling
Handles API and network errors gracefully
Prevents application crashes
Error messages are conditionally rendered

4.4 Watchlist Management
Users can manage a personal movie watchlist.
Add to watchlist:
Movies can be added from search results
Duplicate movies are prevented
Delete from watchlist:
Movies can be removed from the watchlist
State is updated immutably using array filtering

4.5 LocalStorage Persistence
Watchlist data is stored in LocalStorage
Data persists after page refresh
Initial state is loaded from LocalStorage on first render
Hooks used:
useState
useEffect

4.6 Star Rating System
Users can rate movies using a star-based rating interface
Ratings are stored per movie
Ratings are displayed inside the watchlist
Concepts used:
Controlled components
Component state
Props for parent-child communication

4.7 useRef Implementation
useRef is used for direct DOM interaction and non-rendering values.
Use cases:
Automatically focusing the search input
Preserving mutable values without triggering re-render

4.8 State Management
Multiple React states are used to manage application data and UI flow, including:
Search query
Movie list
Loading status
Selected movie
Watchlist
User rating
Hooks used:
useState
useEffect
useRef

5. Usage
5.1 Development Mode
npm start
Runs the application in development mode
Hot reload is enabled

5.2 Production Build
npm run build
Creates optimized static files in the build directory

6. Development Guidelines
Use functional components
Keep components small and reusable
Separate logic from presentation
Avoid unnecessary re-renders
Keep state updates immutable

7. Internal Notes

This project is intended for internal learning purposes
Documentation should be updated alongside feature changes
Code clarity is prioritized over optimization

8. Possible Improvements
Refactor logic into custom hooks
Improve error and empty state handling
Add unit testing
Improve component-level documentation
Migrate the project to TypeScript

9. Credits
This project was inspired by a React learning course.
It was built as part of a personal learning journey, with modifications,
custom implementations, and feature extensions beyond the original material.

```
