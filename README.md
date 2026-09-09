# Belajar-seruu-dengan-Web-seruu
Dengan web ini kita dapat semakin giat untuk belajar pelajaran di sekolah kitaa
<!DOCTYPE html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>StudySpace 📚</title>
    

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }

        body {
            background: #f6f3ff;
            color: #29253d;
        }

        /* SIDEBAR */
        .sidebar {
            position: fixed;
            width: 230px;
            height: 100vh;
            background: #302b4f;
            color: white;
            padding: 30px 20px;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 40px;
            text-align: center;
        }

        .nav a {
            display: block;
            text-decoration: none;
            color: #dcd8ef;
            padding: 14px;
            margin: 8px 0;
            border-radius: 12px;
            transition: 0.2s;
        }

        .nav a:hover,
        .nav a.active {
            background: #8174d8;
            color: white;
        }

        /* MAIN */
        .main {
            margin-left: 230px;
            padding: 35px;
        }

        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
        }

        .header h1 {
            font-size: 30px;
        }

        .profile {
            background: white;
            padding: 10px 18px;
            border-radius: 20px;
            box-shadow: 0 4px 15px #ddd8ed;
        }

        /* WELCOME CARD */
        .welcome {
            background: linear-gradient(135deg, #8174d8, #a996e8);
            color: white;
            padding: 30px;
            border-radius: 22px;
            margin-bottom: 25px;
        }

        .welcome h2 {
            font-size: 27px;
            margin-bottom: 10px;
        }

        .welcome p {
            opacity: 0.9;
        }

        /* GRID */
        .grid {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 25px;
        }

        .card {
            background: white;
            padding: 25px;
            border-radius: 20px;
            box-shadow: 0 5px 20px #e1ddef;
            margin-bottom: 25px;
        }

        .card h2 {
            margin-bottom: 20px;
        }

        /* SUBJECTS */
        .subjects {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
        }

        .subject {
            padding: 20px;
            border-radius: 17px;
            background: #f2effc;
            transition: 0.2s;
            cursor: pointer;
        }

        .subject:hover {
            transform: translateY(-4px);
            box-shadow: 0 8px 18px #ddd8ed;
        }

        .subject span {
            font-size: 30px;
        }

        .subject h3 {
            margin-top: 10px;
        }

        .subject p {
            color: #77718d;
            margin-top: 5px;
        }

        /* PROGRESS */
        .progress-box {
            margin-top: 15px;
        }

        .progress-bar {
            height: 12px;
            background: #ebe8f5;
            border-radius: 20px;
            overflow: hidden;
        }

        .progress {
            width: 72%;
            height: 100%;
            background: #8174d8;
            border-radius: 20px;
        }

        .progress-text {
            display: flex;
            justify-content: space-between;
            margin-bottom: 7px;
            font-size: 14px;
        }

        /* TODO */
        .todo {
            display: flex;
            align-items: center;
            padding: 12px;
            margin-bottom: 10px;
            background: #f7f5fc;
            border-radius: 12px;
        }

        .todo input {
            margin-right: 12px;
            width: 18px;
            height: 18px;
            accent-color: #8174d8;
        }

        /* TIMER */
        .timer {
            text-align: center;
        }

        .time {
            font-size: 55px;
            font-weight: bold;
            color: #8174d8;
            margin: 15px 0;
        }

        button {
            border: none;
            background: #8174d8;
            color: white;
            padding: 11px 20px;
            border-radius: 12px;
            cursor: pointer;
            font-size: 15px;
            margin: 4px;
        }

        button:hover {
            background: #6d61c0;
        }

        /* QUOTE */
        .quote {
            text-align: center;
            font-style: italic;
            color: #625c78;
            line-height: 1.6;
        }

        /* RESPONSIVE */
        @media (max-width: 850px) {
            .sidebar {
                width: 70px;
                padding: 20px 10px;
            }

            .logo {
                font-size: 0;
            }

            .logo::after {
                content: "📚";
                font-size: 25px;
            }

            .nav a {
                font-size: 0;
                text-align: center;
            }

            .nav a::first-letter {
                font-size: 20px;
            }

            .main {
                margin-left: 70px;
            }

            .grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 550px) {
            .main {
                padding: 20px;
            }

            .subjects {
                grid-template-columns: 1fr;
            }

            .header h1 {
                font-size: 23px;
            }
        }
    </style>
</head>

<body>

    <!-- SIDEBAR -->
    <aside class="sidebar">
        <div class="logo">📚 StudySpace</div>

        <nav class="nav">
            <a href="#" class="active">🏠 Home</a>
            <a href="#">📖 Subjects</a>
            <a href="#">📝 Tasks</a>
            <a href="#">⏱️ Focus</a>
            <a href="#">📊 Progress</a>
            <a href="#">⚙️ Settings</a>
        </nav>
    </aside>


    <!-- MAIN CONTENT -->
    <main class="main">

        <header class="header">
            <h1>Good afternoon! 🌷</h1>
            <div class="profile">✨ Student</div>
        </header>


        <!-- WELCOME -->
        <section class="welcome">
            <h2>Ready to study?</h2>
            <p>Small progress is still progress. Keep going! 💜</p>
        </section>


        <div class="grid">

            <!-- LEFT COLUMN -->
            <div>

                <!-- SUBJECTS -->
                <section class="card">
                    <h2>📚 My Subjects</h2>

                    <div class="subjects">

                        <div class="subject">
                            <span>➗</span>
                            <h3>Mathematics</h3>
                            <p>12 lessons</p>
                        </div>

                        <div class="subject">
                            <span>🔬</span>
                            <h3>Science</h3>
                            <p>8 lessons</p>
                        </div>

                        <div class="subject">
                            <span>🌎</span>
                            <h3>Geography</h3>
                            <p>6 lessons</p>
                        </div>

                        <div class="subject">
                            <span>📚</span>
                            <h3>English</h3>
                            <p>10 lessons</p>
                        </div>

                    </div>
                </section>


                <!-- PROGRESS -->
                <section class="card">
                    <h2>📊 Weekly Progress</h2>

                    <div class="progress-box">
                        <div class="progress-text">
                            <span>Study Goal</span>
                            <span>72%</span>
                        </div>

                        <div class="progress-bar">
                            <div class="progress"></div>
                        </div>
                    </div>
                </section>

            </div>


            <!-- RIGHT COLUMN -->
            <div>

                <!-- TIMER -->
                <section class="card timer">
                    <h2>⏱️ Focus Timer</h2>

                    <div class="time" id="time">
                        25:00
                    </div>

                    <button onclick="startTimer()">Start</button>
                    <button onclick="pauseTimer()">Pause</button>
                    <button onclick="resetTimer()">Reset</button>
                </section>


                <!-- TODO -->
                <section class="card">
                    <h2>📝 Today's Tasks</h2>

                    <label class="todo">
                        <input type="checkbox">
                        Finish math homework
                    </label>

                    <label class="todo">
                        <input type="checkbox">
                        Read science chapter
                    </label>

                    <label class="todo">
                        <input type="checkbox">
                        Review vocabulary
                    </label>

                    <label class="todo">
                        <input type="checkbox">
                        Prepare for tomorrow
                    </label>
                </section>


                <!-- QUOTE -->
                <section class="card quote">
                    🌱 "You don't have to be perfect.
                    You just have to keep learning."
                </section>

            </div>

        </div>

    </main>


    <!-- TIMER JAVASCRIPT -->
    <script>

        let seconds = 25 * 60;
        let timer = null;

        function updateTimer() {
            let minutes = Math.floor(seconds / 60);
            let remainingSeconds = seconds % 60;

            document.getElementById("time").textContent =
                String(minutes).padStart(2, "0") +
                ":" +
                String(remainingSeconds).padStart(2, "0");
        }

        function startTimer() {

            if (timer !== null) return;

            timer = setInterval(() => {

                if (seconds > 0) {
                    seconds--;
                    updateTimer();
                } else {
                    clearInterval(timer);
                    timer = null;
                    alert("🎉 Focus session complete! Great job!");
                }

            }, 1000);
        }

        function pauseTimer() {
            clearInterval(timer);
            timer = null;
        }

        function resetTimer() {
            clearInterval(timer);
            timer = null;
            seconds = 25 * 60;
            updateTimer();
        }

    </script>

</body>
</html>
