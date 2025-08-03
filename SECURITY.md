 /* বেসিক স্টাইল */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Hind Siliguri', 'Arial', sans-serif;
}

body {
    background-color: #f5f5f5;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    color: #333;
}

.game-header {
    text-align: center;
    margin-bottom: 15px;
}

.game-header h1 {
    color: #e74c3c;
    font-size: 2.5rem;
    margin-bottom: 10px;
}

.game-settings {
    display: flex;
    justify-content: center;
    gap: 10px;
    margin-bottom: 15px;
}

.game-settings button {
    padding: 8px 15px;
    background-color: #3498db;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 14px;
}

.game-container {
    width: 100%;
    max-width: 800px;
    margin: 20px auto;
    padding: 20px;
    background-color: white;
    border-radius: 15px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
}

.game-board {
    position: relative;
    width: 100%;
    aspect-ratio: 1/1;
    background-color: #f8f8f8;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.1);
}

.board {
    position: absolute;
    width: 100%;
    height: 100%;
    background-color: #f0d9b5;
    background-image: linear-gradient(45deg, #f0d9b5 25%, #e6cfa1 25%, #e6cfa1 50%, #f0d9b5 50%, #f0d9b5 75%, #e6cfa1 75%, #e6cfa1 100%);
    background-size: 20px 20px;
}

.center-home {
    position: absolute;
    width: 30%;
    height: 30%;
    top: 35%;
    left: 35%;
    background-color: white;
    border: 5px solid #333;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2rem;
    color: gold;
    z-index: 1;
}

.player-base {
    position: absolute;
    width: 25%;
    height: 25%;
    border: 5px solid #333;
    z-index: 2;
}

.red-base {
    top: 0;
    left: 0;
    background-color: rgba(231, 76, 60, 0.3);
    border-color: #e74c3c;
}

.green-base {
    top: 0;
    right: 0;
    background-color: rgba(46, 204, 113, 0.3);
    border-color: #2ecc71;
}

.yellow-base {
    bottom: 0;
    left: 0;
    background-color: rgba(241, 196, 15, 0.3);
    border-color: #f1c40f;
}

.blue-base {
    bottom: 0;
    right: 0;
    background-color: rgba(52, 152, 219, 0.3);
    border-color: #3498db;
}

.path-cell {
    position: absolute;
    width: 5%;
    height: 5%;
    background-color: white;
    border: 1px solid #ddd;
    border-radius: 50%;
    z-index: 3;
}

.safe-cell {
    background-color: #fff;
    border: 2px solid #333;
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);
}

.home-cell {
    background-color: #fff;
    border: 2px solid #27ae60;
}

.token {
    position: absolute;
    width: 6%;
    height: 6%;
    border-radius: 50%;
    cursor: pointer;
    transition: all 0.3s ease;
    z-index: 10;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: bold;
    font-size: 1.2rem;
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);
    transform: scale(1);
}

.token:hover {
    transform: scale(1.1);
    z-index: 11;
}

.token.highlight {
    animation: pulse 1s infinite;
    box-shadow: 0 0 15px 5px rgba(255, 255, 0, 0.7);
}

@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.1); }
    100% { transform: scale(1); }
}

.red-token {
    background-color: #e74c3c;
    color: white;
}

.green-token {
    background-color: #2ecc71;
    color: white;
}

.yellow-token {
    background-color: #f1c40f;
    color: #333;
}

.blue-token {
    background-color: #3498db;
    color: white;
}

.game-controls {
    margin-top: 20px;
    text-align: center;
    padding: 15px;
    background-color: #f8f8f8;
    border-radius: 10px;
}

.dice-container {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
    margin-bottom: 15px;
}

.dice {
    width: 70px;
    height: 70px;
    background-color: white;
    border-radius: 15px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2.5rem;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
    cursor: pointer;
    user-select: none;
}

.roll-btn {
    padding: 12px 25px;
    background-color: #e74c3c;
    color: white;
    border: none;
    border-radius: 8px;
    font-size: 1.1rem;
    cursor: pointer;
    transition: all 0.3s;
    box-shadow: 0 3px 0 #c0392b;
}

.roll-btn:hover {
    background-color: #c0392b;
    transform: translateY(2px);
    box-shadow: 0 1px 0 #c0392b;
}

.player-turn {
    font-size: 1.3rem;
    font-weight: bold;
    margin-bottom: 10px;
    color: #e74c3c;
}

.game-message {
    font-size: 1.1rem;
    color: #333;
    min-height: 30px;
    margin-bottom: 15px;
    font-weight: 500;
}

.ai-controls {
    margin-top: 15px;
}

.ai-controls label {
    margin-right: 10px;
    font-size: 1rem;
}

.ai-controls select {
    padding: 8px 12px;
    border-radius: 5px;
    border: 1px solid #ddd;
    font-size: 1rem;
}

/* মোবাইল রেস্পন্সিভ */
@media (max-width: 600px) {
    .game-container {
        padding: 10px;
    }
    
    .dice {
        width: 50px;
        height: 50px;
        font-size: 1.8rem;
    }
    
    .roll-btn {
        padding: 10px 20px;
        font-size: 1rem;
    }
    
    .player-turn {
        font-size: 1.1rem;
    }
    
    .game-message {
        font-size: 1rem;
    }
}
