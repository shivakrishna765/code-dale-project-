# code-dale-project-
// App.js
import React from 'react';
import { motion } from 'framer-motion';
import './App.css'; // For custom styling (e.g., custom mouse cursor)

function App() {
  return (
    <div className="relative bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500 h-screen">
      {/* Custom Cursor */}
      <div className="absolute top-0 left-0 w-full h-full pointer-events-none">
        <div className="custom-cursor"></div>
      </div>

      {/* Main Section */}
      <div className="flex items-center justify-center h-full text-center">
        <motion.div
          className="text-white font-bold text-5xl md:text-7xl leading-tight"
          initial={{ opacity: 0 }}
          animate={{ opacity: 1 }}
          transition={{ duration: 1 }}
        >
          <h1>Design with Relume</h1>
          <p className="mt-4 text-xl md:text-2xl">Create beautiful websites faster than ever</p>

          <motion.button
            className="mt-8 py-3 px-6 bg-gradient-to-r from-blue-400 to-purple-400 text-white rounded-full text-lg hover:scale-105 transform transition-all"
            whileHover={{ scale: 1.05 }}
          >
            Get Started
          </motion.button>
        </motion.div>
      </div>

      {/* SVG Background Animation */}
      <motion.svg
        className="absolute top-0 left-0 z-[-1]"
        viewBox="0 0 1440 320"
        initial={{ y: "100%" }}
        animate={{ y: 0 }}
        transition={{ duration: 2 }}
      >
        <path
          fill="#fff"
          fillOpacity="1"
          d="M0,288L48,261.3C96,235,192,181,288,144C384,107,480,75,576,85.3C672,96,768,160,864,181.3C960,203,1056,181,1152,144C1248,107,1344,43,1392,11.3L1440,0L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
        ></path>
      </motion.svg>
    </div>
  );
}

export default App;


//css
/* App.css */
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

.custom-cursor {
  position: absolute;
  width: 20px;
  height: 20px;
  background-color: white;
  border-radius: 50%;
  pointer-events: none;
  transition: all 0.1s ease-in-out;
}

.custom-cursor.active {
  background-color: #ff4081;
  transform: scale(1.5);
}

html {
  cursor: none; /* Hide default cursor */
}
//js 
// tailwind.config.js
module.exports = {
  content: [
    "./src/**/*.{html,js,jsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
//cursor function 
import React, { useEffect } from 'react';
import { motion } from 'framer-motion';
import './App.css'; // Custom CSS for cursor and other styling

// Custom Cursor Hook
const useCustomCursor = () => {
  useEffect(() => {
    const cursor = document.querySelector('.custom-cursor');
    const updateCursor = (e) => {
      cursor.style.top = `${e.clientY - 10}px`;
      cursor.style.left = `${e.clientX - 10}px`;
    };
    window.addEventListener('mousemove', updateCursor);

    return () => {
      window.removeEventListener('mousemove', updateCursor);
    };
  }, []);
};

function App() {
  useCustomCursor(); // Initialize custom cursor

  return (
    <div className="relative bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500 h-screen overflow-hidden">
      {/* Custom Cursor */}
      <div className="absolute top-0 left-0 w-full h-full pointer-events-none">
        <div className="custom-cursor"></div>
      </div>

      {/* Main Section */}
      <div className="flex items-center justify-center h-full text-center">
        <motion.div
          className="text-white font-bold text-5xl md:text-7xl leading-tight"
          initial={{ opacity: 0 }}
          animate={{ opacity: 1 }}
          transition={{ duration: 1 }}
        >
          <h1>Design with Relume</h1>
          <p className="mt-4 text-xl md:text-2xl">Create beautiful websites faster than ever</p>

          <motion.button
            className="mt-8 py-3 px-6 bg-gradient-to-r from-blue-400 to-purple-400 text-white rounded-full text-lg hover:scale-105 transform transition-all"
            whileHover={{ scale: 1.05 }}
          >
            Get Started
          </motion.button>
        </motion.div>
      </div>

      {/* SVG Background Animation */}
      <motion.svg
        className="absolute top-0 left-0 z-[-1]"
        viewBox="0 0 1440 320"
        initial={{ y: "100%" }}
        animate={{ y: 0 }}
        transition={{ duration: 2 }}
      >
        <path
          fill="#fff"
          fillOpacity="1"
          d="M0,288L48,261.3C96,235,192,181,288,144C384,107,480,75,576,85.3C672,96,768,160,864,181.3C960,203,1056,181,1152,144C1248,107,1344,43,1392,11.3L1440,0L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"
        ></path>
      </motion.svg>
    </div>
  );
}

export default App;
//App.css
/* App.css */
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

.custom-cursor {
  position: absolute;
  width: 20px;
  height: 20px;
  background-color: white;
  border-radius: 50%;
  pointer-events: none;
  transition: all 0.1s ease-in-out;
}

.custom-cursor.active {
  background-color: #ff4081;
  transform: scale(1.5);
}

html {
  cursor: none; /* Hide default cursor */
}
//tailwind.js 
// tailwind.config.js
module.exports = {
  content: [
    "./src/**/*.{html,js,jsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}




