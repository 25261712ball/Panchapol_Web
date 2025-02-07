<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>บอกรักแฟน 💚</title>
    <style>
        body {
            text-align: center;
            font-family: 'Arial', sans-serif;
            background-color: white;
            color: black;
            margin: 0;
            padding: 50px;
            overflow: hidden;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
            display: inline-block;
            position: relative;
        }
        h1 {
            color: black;
        }
        .button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
        }
        .yes {
            background-color: #28a745;
            color: white;
        }
        .no {
            background-color: #ccc;
            color: black;
        }
        .hidden {
            display: none;
        }
        .back-button {
            position: absolute;
            top: 10px;
            left: 10px;
            cursor: pointer;
            width: 50px;
        }
    </style>
</head>
<body>
    <div class="container" id="question-container">
        <h1>รักเค้าไหม? 💚</h1>
        <button class="button yes" onclick="showLove()">รัก</button>
        <button class="button no" onclick="showNotSure()">ไม่รัก</button>
    </div>
    <div class="container hidden" id="love-container">
        <h1>รักเหมือนกัน อิอิ 💚</h1>
        <video width="320" height="240" controls autoplay>
            <source src="test.mp4" type="video/mp4">
        </video>
    </div>
    <div class="container hidden" id="notsure-container">
        <h1>แน่ใจเหรอ? 🤨</h1>
        <img src="Dof.jpg" >
        <button class="button no" onclick="resetQuestion()">ไม่</button>
        <button class="button no" onclick="resetQuestion()">ไม่</button>
    </div>
    
    <script>
        function showLove() {
            document.getElementById("question-container").classList.add("hidden");
            document.getElementById("love-container").classList.remove("hidden");
            document.querySelector(".back-button").classList.remove("hidden");
        }
        
        function showNotSure() {
            document.getElementById("question-container").classList.add("hidden");
            document.getElementById("notsure-container").classList.remove("hidden");
            document.querySelector(".back-button").classList.remove("hidden");
        }
        
        function resetQuestion() {
            document.getElementById("question-container").classList.remove("hidden");
            document.getElementById("love-container").classList.add("hidden");
            document.getElementById("notsure-container").classList.add("hidden");
            document.querySelector(".back-button").classList.add("hidden");
        }
    </script>
</body>
</html>
