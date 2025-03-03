<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine Của Mập và Tiên Nữ ❤️</title>
    <style>
        :root {
            --primary-color: #ff3366;
            --secondary-color: #fff0f5;
        }

        body {
            font-family: 'Pacifico', cursive;
            background: linear-gradient(to right, #fff0f5, #ffe4e1);
            margin: 0;
            overflow-x: hidden;
        }

        .header {
            height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        .heart-fall {
            position: absolute;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .heart {
            position: absolute;
            color: var(--primary-color);
            animation: fall 3s linear infinite;
        }

        @keyframes fall {
            to { transform: translateY(100vh) rotate(360deg); }
        }

        .couple-photo {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            border: 5px solid white;
            box-shadow: 0 0 20px rgba(255,51,102,0.3);
            transition: transform 0.3s;
        }

        .couple-photo:hover {
            transform: scale(1.05);
        }

        .timeline {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            padding: 2rem;
        }

        .memory-card {
            background: white;
            padding: 1.5rem;
            border-radius: 15px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            transition: transform 0.3s;
            cursor: pointer;
        }

        .memory-card:hover {
            transform: translateY(-5px);
        }

        .love-letter {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: white;
            padding: 1rem;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            cursor: pointer;
            transition: transform 0.3s;
        }

        .love-letter:hover {
            transform: rotate(5deg);
        }

        @media (max-width: 768px) {
            .couple-photo {
                width: 150px;
                height: 150px;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
</head>
<body>
    <div class="header">
        <div class="heart-fall" id="hearts-container"></div>
        <h1 style="color: var(--primary-color); margin-top: 1rem;">[Mập] ❤️ [Tiên Nữ Xinh Đẹp Nhất Thế Gian]</h1>
        <p>Ngày yêu nhau: 18/06/2022</p>
        <img src="your-couple-photo.jpg" alt="Chuyến đầu tiên về Vũng Tàu" class="couple-photo">
        <img src="your-couple-photo1.jpg" alt="Phượt Đà Lạt bằng Lead thần thánh" class="couple-photo">
        <img src="your-couple-photo2.jpg" alt="Cùng nhau tốt nghiệp" class="couple-photo">
        <img src="your-couple-photo3.jpg" alt="Cùng ngồi trên chiếc xe của chúng mình" class="couple-photo">
        <img src="your-couple-photo4.jpg" alt="Say sóng cùng nhau ở ngoài biển khơi" class="couple-photo">
    </div>
    <div class="love-letter" onclick="openLetter()">
        <img src="heart-icon.png" alt="Ngõ lời yêu thương" width="50">
    </div>
    <script>
        function createHearts() {
            const container = document.getElementById('hearts-container');
            for (let i = 0; i < 50; i++) {
                const heart = document.createElement('div');
                heart.className = 'heart';
                heart.innerHTML = '❤️';
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.animationDelay = Math.random() * -3 + 's';
                container.appendChild(heart);
            }
        }

        function openLetter() {
            const content = `
                <div style="padding: 20px; text-align: center;">
                    <h2>Gửi Tiên Nữ yêu dấu của đời anh,</h2>
                    <p>Anh muốn nói rằng... [Anh yêu em nhiều lắm, anh chỉ hi vọng một điều dù đường đời có khó khăn thế nào mình vẫn mãi có nhau em nhé! Yêu em nhiều!]</p>
                    <button onclick="this.parentElement.style.display='none'">❤️ Đóng thư</button>
                </div>
            `;
            const letter = document.querySelector('.love-letter');
            letter.innerHTML = content;
        }

        window.onload = createHearts;
    </script>
</body>
</html>
