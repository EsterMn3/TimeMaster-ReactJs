# Time Master

**Time Master** is a fun and engaging timer-based challenge game. The player is tasked with starting and stopping a timer, aiming to achieve the highest score based on how close they get to the target time. Each challenge offers progressively harder target times. You can set your name, which is displayed throughout the game. This app uses React for component-based architecture, leveraging `useState`, `useRef`, `forwardRef`, and `createPortal` for state and DOM management.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)
![React Portal](https://img.shields.io/badge/React%20Portal-61DAFB?style=for-the-badge&logo=react&logoColor=black)

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h1 align="center">Time Master</h1>

  <p align="center">
    <a href="https://timemaster-reactjs-ester.netlify.app/">View Demo</a>
  </p>
</div>

## Features

- Enter and display player name.
- Time challenges with varying difficulty levels.
- Score calculation based on timing precision.
- Modal window displays results when the timer is stopped or expires.
- Reset and restart challenges easily.

## Components

1. **Player Component**:

   - Allows the user to input their name, which is then displayed during the game.
   - Uses `useRef` to directly reference the input field and clear it after submission.

2. **TimerChallenge Component**:

   - Manages countdown timers for each challenge.
   - Uses `useState` to track the remaining time and `useRef` to control the modal.
   - Includes start and stop buttons for the timer.

3. **ResultModal Component**:

   - Displays the result in a modal after a challenge ends.
   - Uses `forwardRef` to expose methods (like `open`) to the parent component (`TimerChallenge`) via `useImperativeHandle`.
   - Utilizes `createPortal` to render the modal outside the main component tree, improving accessibility and structure.

4. **App Component**:
   - Combines the `Player` and `TimerChallenge` components to create the game's main interface.

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/timemaster.git
   cd timemaster
   ```

2. **Install Dependencies: Ensure you have Node.js installed, then run:**
   npm install

3. **Run the Application: Start the app in development mode:**
   npm start

## How to Play

1. Enter your name in the input field and click **"Set Name."**
2. Choose a timer challenge (e.g., **Easy, Not easy**, etc.).
3. Press **"Start"** to begin the timer. Stop it as close to the target time as possible.
4. When you stop the timer (or when time runs out), a modal will display your score and remaining time.
5. Reset the timer and try again!

## Folder Structure

```bash
/src
  /components
    Player.jsx
    TimerChallenge.jsx
    ResultModal.jsx
  App.js
  index.js
  index.css
```

## Technologies Used

- **React** (Hooks: `useState`, `useRef`, `useImperativeHandle`)
- `forwardRef` to enable ref forwarding in components.
- `createPortal` to render the modal outside of the normal DOM hierarchy.
- **HTML5**
- **CSS3**

## Future Improvements

- Add more difficulty levels or bonus rounds.
- Implement high score tracking across multiple rounds.
- Introduce multiplayer functionality.
