    body {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        background: #1e3a8a;
        min-height: 100vh;
        padding: 20px;
        position: relative;
        overflow-x: hidden;
    }

    body::before {
        content: '6 7 6 7 6 7 6 7 6 7 6 7 6 7 6 7 6 7 6 7';
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        font-size: 150px;
        font-weight: bold;
        color: rgba(59, 130, 246, 0.1);
        line-height: 1.5;
        word-wrap: break-word;
        z-index: 0;
        pointer-events: none;
        letter-spacing: 50px;
    }

    .container {
        max-width: 800px;
        margin: 0 auto;
        position: relative;
        z-index: 1;
    }

    .header {
        text-align: center;
        color: white;
        margin-bottom: 20px;
    }

    .header h1 {
        font-size: 2.5em;
        margin-bottom: 10px;
        text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
    }

    .header p {
        font-size: 1.1em;
        text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
    }

    .chat-container {
        background: white;
        border-radius: 10px;
        padding: 20px;
        box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }

    .messages {
        height: 500px;
        overflow-y: auto;
        border: 2px solid #bfdbfe;
        padding: 15px;
        margin-bottom: 20px;
        border-radius: 8px;
        background-color: #eff6ff;
    }

    .message {
        margin: 15px 0;
        padding: 12px 15px;
        border-radius: 8px;
        animation: fadeIn 0.3s ease-in;
        white-space: pre-wrap;
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(10px); }
        to { opacity: 1; transform: translateY(0); }
    }

    .user-message {
        background-color: #2563eb;
        color: white;
        margin-left: 50px;
        text-align: right;
    }

    .bot-message {
        background-color: white;
        border: 2px solid #93c5fd;
        margin-right: 50px;
        color: #1e40af;
    }

    .input-area {
        display: flex;
        gap: 10px;
    }

    #userInput {
        flex: 1;
        padding: 12px;
        border: 2px solid #3b82f6;
        border-radius: 8px;
        font-size: 16px;
        transition: border-color 0.3s;
    }

    #userInput:focus {
        outline: none;
        border-color: #2563eb;
    }

    #sendBtn {
        padding: 12px 30px;
        background-color: #2563eb;
        color: white;
        border: none;
        border-radius: 8px;
        cursor: pointer;
        font-size: 16px;
        font-weight: bold;
        transition: background-color 0.3s;
    }

    #sendBtn:hover {
        background-color: #1d4ed8;
    }

    #sendBtn:disabled {
        background-color: #93c5fd;
        cursor: not-allowed;
    }

    .typing-indicator {
        display: none;
        padding: 10px;
        color: #1e40af;
        font-style: italic;
    }

    .typing-indicator.active {
        display: block;
    }

    .suggestions {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        margin-bottom: 15px;
    }

    .suggestion-btn {
        padding: 8px 15px;
        background-color: #dbeafe;
        color: #1e40af;
        border: 2px solid #3b82f6;
        border-radius: 20px;
        cursor: pointer;
        font-size: 14px;
        transition: all 0.3s;
    }

    .suggestion-btn:hover {
        background-color: #3b82f6;
        color: white;
    }

    /* Custom scrollbar for messages */
    .messages::-webkit-scrollbar {
        width: 8px;
    }

    .messages::-webkit-scrollbar-track {
        background: #dbeafe;
        border-radius: 4px;
    }

    .messages::-webkit-scrollbar-thumb {
        background: #3b82f6;
        border-radius: 4px;
    }

    .messages::-webkit-scrollbar-thumb:hover {
        background: #2563eb;
    }
</style>
