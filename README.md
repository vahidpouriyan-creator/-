[eli gavsandogh.html](https://github.com/user-attachments/files/25436131/eli.gavsandogh.html)
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>گاوصندوق کلاسیک | طلایی و مشکی</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Cinzel', 'Courier New', serif;
        }
        body {
            background: linear-gradient(145deg, #0a0a0a 0%, #1a1a1a 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 16px;
        }
        .safe-container {
            max-width: 550px;
            width: 100%;
        }
        .safe {
            background: #0c0c0c;
            border-radius: 25px;
            padding: 35px 25px 30px 25px;
            box-shadow: 
                0 25px 40px rgba(0,0,0,0.9),
                0 0 0 2px #3a2a0a,
                inset 0 0 20px rgba(255,215,0,0.2),
                inset 0 -5px 15px rgba(0,0,0,0.9);
            border: 1px solid #b8860b;
            position: relative;
            background: #0f0f0f;
        }
        /* تزئینات طلایی گوشه‌ها */
        .safe::before {
            content: "";
            position: absolute;
            top: 15px;
            left: 15px;
            width: 40px;
            height: 40px;
            border-top: 3px solid #b8860b;
            border-left: 3px solid #b8860b;
            opacity: 0.6;
        }
        .safe::after {
            content: "";
            position: absolute;
            bottom: 15px;
            right: 15px;
            width: 40px;
            height: 40px;
            border-bottom: 3px solid #b8860b;
            border-right: 3px solid #b8860b;
            opacity: 0.6;
        }
        /* دسته گاوصندوق طلایی */
        .handle {
            position: absolute;
            top: 35px;
            left: 35px;
            width: 60px;
            height: 60px;
            background: #b8860b;
            border-radius: 50%;
            border: 3px solid #5a3e0a;
            box-shadow: 
                0 8px 0 #3a2a0a,
                0 10px 15px rgba(0,0,0,0.8),
                inset 0 -5px 8px #f0c674;
            cursor: pointer;
            transition: all 0.1s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #000;
            font-size: 18px;
            font-weight: bold;
            z-index: 10;
            background: radial-gradient(circle at 30% 30%, #f5d742, #b8860b);
            text-shadow: 0 1px 2px #fff3b0;
        }
        .handle:active {
            transform: rotate(20deg);
            box-shadow: 0 3px 0 #3a2a0a, 0 8px 12px rgba(0,0,0,0.8);
        }
        .handle::after {
            content: "⚜️";
            font-size: 28px;
        }
        /* صفحه نمایش مشکی با نور طلایی */
        .display {
            background: #050505;
            border: 4px solid #b8860b;
            border-radius: 12px;
            padding: 18px 12px;
            margin: 0 0 30px 0;
            box-shadow: 
                inset 0 0 30px #000,
                0 0 20px rgba(184,134,11,0.3);
            color: #f5d742;
            font-size: 40px;
            font-weight: bold;
            text-align: center;
            letter-spacing: 8px;
            direction: ltr;
            font-family: 'Courier New', monospace;
            text-shadow: 0 0 12px #ffd700, 0 0 25px #b8860b;
            position: relative;
            overflow: hidden;
            background: #080808;
        }
        .display::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, transparent, #ffd700, #b8860b, #ffd700, transparent);
            animation: goldScan 3s linear infinite;
            opacity: 0.7;
        }
        @keyframes goldScan {
            0% { top: 0; }
            50% { top: 100%; }
            100% { top: 0; }
        }
        /* صفحه برنده شدن طلایی */
        .win-screen {
            background: #0a0600;
            border: 4px solid #b8860b;
            border-radius: 20px;
            padding: 30px 20px;
            margin-bottom: 30px;
            box-shadow: 
                0 0 40px #b8860b,
                inset 0 0 30px #3a2a0a;
            color: #ffd700;
            text-align: center;
            transform: scale(1);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            animation: goldGlow 2s infinite alternate;
            position: relative;
            overflow: hidden;
        }
        .win-screen::before {
            content: "⚜️⚜️⚜️";
            position: absolute;
            top: -10px;
            left: 0;
            width: 100%;
            color: rgba(184,134,11,0.1);
            font-size: 60px;
            transform: rotate(-5deg);
            pointer-events: none;
        }
        @keyframes goldGlow {
            from { box-shadow: 0 0 30px #b8860b, inset 0 0 20px #5a3e0a; }
            to { box-shadow: 0 0 70px #ffd700, inset 0 0 40px #b8860b; }
        }
        .win-screen h1 {
            font-size: 42px;
            margin-bottom: 20px;
            font-weight: bold;
            text-shadow: 0 0 15px #ffd700, 0 0 30px #b8860b;
            letter-spacing: 3px;
            font-family: 'Cinzel', serif;
            border-bottom: 2px solid #b8860b;
            display: inline-block;
            padding-bottom: 10px;
        }
        .win-screen p {
            font-size: 28px;
            margin: 25px 0 15px 0;
            color: #f5d742;
            border-top: 2px dashed #b8860b;
            border-bottom: 2px dashed #b8860b;
            padding: 20px 0;
            font-family: 'Courier New', monospace;
            background: rgba(0,0,0,0.5);
        }
        .win-screen .designer {
            font-size: 24px;
            color: #ffd700;
            margin-top: 25px;
            font-style: italic;
            background: rgba(184,134,11,0.15);
            padding: 12px 25px;
            border-radius: 50px;
            display: inline-block;
            border: 1px solid #b8860b;
            box-shadow: 0 0 15px rgba(184,134,11,0.3);
        }
        /* دکمه‌های عددی طلایی روی مشکی */
        .buttons-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 18px;
            margin: 25px 0;
            direction: ltr;
        }
        .num-btn {
            background: #1a1a1a;
            border: none;
            border-radius: 18px;
            padding: 22px 0;
            font-size: 40px;
            font-weight: bold;
            color: #b8860b;
            box-shadow: 
                0 8px 0 #0a0a0a,
                0 10px 15px rgba(0,0,0,0.8),
                inset 0 2px 10px rgba(255,215,0,0.3);
            cursor: pointer;
            transition: all 0.07s ease;
            font-family: 'Courier New', monospace;
            border: 1px solid #b8860b;
            text-shadow: 0 0 8px #ffd700;
            background: radial-gradient(circle at 20% 20%, #2a2a2a, #0a0a0a);
        }
        .num-btn:active {
            transform: translateY(7px);
            box-shadow: 0 2px 0 #0a0a0a, 0 8px 12px rgba(0,0,0,0.8);
            color: #ffd700;
        }
        .num-btn:hover {
            background: #2a2a2a;
            color: #ffd700;
            box-shadow: 0 8px 0 #0a0a0a, 0 10px 20px rgba(184,134,11,0.3);
        }
        /* دکمه‌های کنترلی طلایی */
        .action-buttons {
            display: flex;
            gap: 20px;
            margin-top: 20px;
        }
        .action-btn {
            flex: 1;
            background: #1a1a1a;
            border: none;
            border-radius: 15px;
            padding: 20px 0;
            font-size: 26px;
            font-weight: bold;
            color: #b8860b;
            box-shadow: 
                0 7px 0 #0a0a0a,
                inset 0 1px 8px rgba(255,215,0,0.2);
            cursor: pointer;
            transition: all 0.07s ease;
            font-family: 'Cinzel', serif;
            border: 1px solid #b8860b;
            letter-spacing: 2px;
            text-transform: uppercase;
            background: radial-gradient(circle at 30% 30%, #2a2a2a, #0f0f0f);
        }
        .action-btn.clear {
            color: #cd7f32; /* برنزی */
            border-color: #cd7f32;
        }
        .action-btn.enter {
            color: #ffd700;
            border-color: #ffd700;
        }
        .action-btn:active {
            transform: translateY(5px);
            box-shadow: 0 2px 0 #0a0a0a;
        }
        .action-btn.clear:active {
            color: #ffaa33;
        }
        .action-btn.enter:active {
            color: #fff0a0;
        }
        /* بخش نمایش کدهای مجاز طلایی */
        .codes-info {
            background: #0a0a0a;
            border-radius: 40px;
            padding: 15px 12px;
            margin: 25px 0 5px 0;
            border: 2px solid #b8860b;
            color: #ffd700;
            text-align: center;
            font-size: 24px;
            font-weight: bold;
            box-shadow: inset 0 0 20px rgba(184,134,11,0.2);
        }
        .codes-info span {
            display: inline-block;
            background: #050505;
            padding: 8px 18px;
            margin: 0 8px;
            border-radius: 40px;
            color: #ffd700;
            border: 2px solid #b8860b;
            font-family: 'Courier New', monospace;
            direction: ltr;
            font-size: 26px;
            box-shadow: 0 0 15px rgba(184,134,11,0.3);
        }
        .footer-note {
            text-align: center;
            color: #b8860b;
            margin-top: 20px;
            font-size: 16px;
            font-family: 'Cinzel', serif;
            border-top: 2px solid #3a2a0a;
            padding-top: 15px;
            opacity: 0.9;
        }
        .footer-note strong {
            color: #ffd700;
            font-size: 18px;
            text-shadow: 0 0 8px #b8860b;
        }
        .hidden {
            display: none;
        }
        /* خطوط تزئینی طلایی */
        .gold-line {
            height: 2px;
            background: linear-gradient(90deg, transparent, #b8860b, #ffd700, #b8860b, transparent);
            margin: 20px 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <div class="safe-container">
        <div class="safe">
            <!-- دسته گاوصندوق طلایی -->
            <div class="handle" id="handleClick" title="دسته طلایی"></div>
            
            <!-- صفحه نمایش مشکی با نور طلایی -->
            <div class="display" id="display">____</div>
            
            <!-- بخش برنده شدن طلایی -->
            <div id="winScreen" class="win-screen hidden">
                <h1>🔓 گاوصندوق باز شد</h1>
                <p>🎉 شما برنده بازی گام‌های کشف شده‌ای 🎉</p>
                <div class="designer">طراح بازی: الینا پوریان</div>
                <div style="margin-top: 25px; font-size: 30px;">⚜️ ⚜️ ⚜️</div>
            </div>
            
            <!-- دکمه‌های اعداد طلایی -->
            <div class="buttons-grid" id="numPad">
                <button class="num-btn" data-num="1">۱</button>
                <button class="num-btn" data-num="2">۲</button>
                <button class="num-btn" data-num="3">۳</button>
                <button class="num-btn" data-num="4">۴</button>
                <button class="num-btn" data-num="5">۵</button>
                <button class="num-btn" data-num="6">۶</button>
                <button class="num-btn" data-num="7">۷</button>
                <button class="num-btn" data-num="8">۸</button>
                <button class="num-btn" data-num="9">۹</button>
                <button class="num-btn" data-num="0" style="grid-column: span 3;">۰</button>
            </div>
            
            <!-- دکمه‌های اکشن طلایی -->
            <div class="action-buttons">
                <button class="action-btn clear" id="clearBtn">🚫 پاک</button>
                <button class="action-btn enter" id="enterBtn">⚡ باز کن</button>
            </div>
            
            <!-- خط تزئین طلایی -->
            <div class="gold-line"></div>
            
            <!-- نمایش کدهای مجاز -->
            <div class="codes-info">
                <span>۱۲۰</span> <span>۴۴</span> <span>۲۳</span> <span>۹۵</span>
            </div>
        </div>
        <div class="footer-note">
            <strong>✨ گاوصندوق کلاسیک طلایی ✨</strong><br>
            با هرکدام از کدها باز می‌شود
        </div>
    </div>

    <script>
        (function() {
            // آرایه کدهای صحیح (چهار کد مجزا)
            const CORRECT_CODES = ["120", "44", "23", "95"];
            
            // متغیر ذخیره ورودی فعلی
            let enteredCode = "";
            
            // المنت‌ها
            const displayEl = document.getElementById("display");
            const winScreenEl = document.getElementById("winScreen");
            const numPad = document.getElementById("numPad");
            const clearBtn = document.getElementById("clearBtn");
            const enterBtn = document.getElementById("enterBtn");
            const handle = document.getElementById("handleClick");

            // به روز رسانی صفحه نمایش
            function updateDisplay() {
                if (enteredCode.length === 0) {
                    displayEl.textContent = "____";
                    return;
                }
                displayEl.textContent = enteredCode;
            }

            // پاک کردن صفحه و بازگشت به حالت عادی
            function resetToNormal() {
                enteredCode = "";
                updateDisplay();
                if (!winScreenEl.classList.contains("hidden")) {
                    winScreenEl.classList.add("hidden");
                }
            }

            // بررسی کد وارد شده
            function checkCode() {
                if (CORRECT_CODES.includes(enteredCode)) {
                    winScreenEl.classList.remove("hidden");
                    enteredCode = "";
                    updateDisplay();
                    return true;
                }
                return false;
            }

            // رویداد عدد‌ها
            numPad.addEventListener("click", (e) => {
                const btn = e.target.closest(".num-btn");
                if (!btn) return;
                
                if (!winScreenEl.classList.contains("hidden")) {
                    resetToNormal();
                }
                
                const num = btn.getAttribute("data-num");
                if (num !== null) {
                    if (enteredCode.length < 5) {
                        enteredCode += num;
                        updateDisplay();
                        
                        if (enteredCode.length >= 2) {
                            checkCode();
                        }
                    }
                }
            });

            // دکمه پاک کردن
            clearBtn.addEventListener("click", () => {
                resetToNormal();
                handle.style.transform = "rotate(10deg)";
                setTimeout(() => handle.style.transform = "", 150);
            });

            // دکمه enter
            enterBtn.addEventListener("click", () => {
                if (!winScreenEl.classList.contains("hidden")) {
                    handle.style.transform = "rotate(20deg)";
                    setTimeout(() => handle.style.transform = "", 200);
                    return;
                }
                
                if (enteredCode.length === 0) {
                    displayEl.textContent = "خالی";
                    setTimeout(() => updateDisplay(), 500);
                    return;
                }
                
                if (!checkCode()) {
                    displayEl.textContent = "❌";
                    setTimeout(() => {
                        if (winScreenEl.classList.contains("hidden")) {
                            enteredCode = "";
                            updateDisplay();
                        }
                    }, 700);
                }
                
                handle.style.transform = "rotate(25deg)";
                setTimeout(() => handle.style.transform = "", 300);
            });

            // دسته طلایی
            handle.addEventListener("click", () => {
                handle.style.transform = "rotate(35deg) scale(0.95)";
                setTimeout(() => handle.style.transform = "", 250);
                
                if (winScreenEl.classList.contains("hidden")) {
                    displayEl.textContent = "⚜️";
                    setTimeout(() => updateDisplay(), 500);
                }
            });

            // کیبورد
            document.addEventListener("keydown", (e) => {
                const key = e.key;
                
                if (key >= "0" && key <= "9") {
                    e.preventDefault();
                    if (!winScreenEl.classList.contains("hidden")) {
                        resetToNormal();
                    }
                    if (enteredCode.length < 5) {
                        enteredCode += key;
                        updateDisplay();
                        
                        if (enteredCode.length >= 2) {
                            checkCode();
                        }
                    }
                } 
                else if (key === "Enter") {
                    e.preventDefault();
                    enterBtn.click();
                } 
                else if (key === "Backspace" || key === "Escape" || key === "Delete") {
                    e.preventDefault();
                    clearBtn.click();
                }
            });

            resetToNormal();
        })();
    </script>
</body>
</html>
