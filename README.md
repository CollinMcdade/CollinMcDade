<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rainbow Profile Welcome</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@700&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background-color: #1a202c; /* Dark background for contrast */
            overflow: hidden; /* Prevent scrollbars */
        }

        .rainbow-container {
            font-size: 4rem; /* Large text */
            font-weight: 700;
            white-space: nowrap; /* Keep text on one line */
            overflow: hidden; /* Hide overflowing text */
            border-right: .15em solid orange; /* Typing cursor effect */
            animation:
                typing 3.5s steps(22, end) forwards, /* Type out text */
                blink-caret .75s step-end infinite; /* Blinking cursor */
            width: 0; /* Start with zero width */
            border-radius: 0.5rem; /* Rounded corners for the container */
            padding: 0.5rem 1rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .rainbow-text {
            display: inline-block; /* Allows individual character styling */
            background: linear-gradient(to right,
                #ff0000, /* Red */
                #ff7f00, /* Orange */
                #ffff00, /* Yellow */
                #00ff00, /* Green */
                #0000ff, /* Blue */
                #4b0082, /* Indigo */
                #9400d3  /* Violet */
            );
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-size: 200% auto; /* For the gradient animation */
            animation: rainbow-shift 6s linear infinite; /* Shift colors */
        }

        /* Typing animation */
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }

        /* Blinking cursor animation */
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: orange }
        }

        /* Rainbow color shift animation */
        @keyframes rainbow-shift {
            to { background-position: 200% center; }
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .rainbow-container {
                font-size: 2.5rem; /* Smaller font for mobile */
                padding: 0.3rem 0.8rem;
            }
        }

        @media (max-width: 480px) {
            .rainbow-container {
                font-size: 1.8rem; /* Even smaller font for small mobiles */
                padding: 0.2rem 0.5rem;
            }
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <div class="rainbow-container rounded-lg shadow-lg">
        <span class="rainbow-text">Welcome to my profile!</span>
    </div>
</body>
</html>
