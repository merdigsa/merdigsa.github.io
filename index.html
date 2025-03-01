<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Включение звука</title>
    <style>
        body {
            font-family: 'Roboto', Arial, sans-serif;
            background-color: #2c3e50;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        
        .container {
            text-align: center;
        }
        
        .btn {
            background-color: #e74c3c;
            color: white;
            border: none;
            padding: 20px 40px;
            font-size: 24px;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
            margin: 20px 0;
            outline: none;
        }
        
        .btn:hover {
            background-color: #c0392b;
            transform: scale(1.05);
        }
        
        .btn:active {
            transform: scale(0.95);
        }
        
        h1 {
            margin-bottom: 40px;
            font-size: 32px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .status {
            margin-top: 30px;
            font-size: 18px;
            opacity: 0.8;
        }
        
        .hidden {
            display: none;
        }
        
        #audioElement {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Включение звука</h1>
        <button id="volumeBtn" class="btn">ВКЛЮЧИТЬ ЗВУК НА ПОЛНУЮ</button>
        <div id="status" class="status">Нажмите на кнопку для активации</div>
        <!-- Здесь указываете путь к вашему звуковому файлу -->
        <audio id="audioElement" src="videoplayback (1).m4a" loop></audio>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const volumeBtn = document.getElementById('volumeBtn');
            const statusEl = document.getElementById('status');
            const audioElement = document.getElementById('audioElement');
            let audioContext = null;
            
            // Функция для воспроизведения звука на максимальной громкости
            function playSound() {
                // Проверяем, поддерживается ли Web Audio API
                if (window.AudioContext || window.webkitAudioContext) {
                    try {
                        // Создаем аудио контекст
                        if (!audioContext) {
                            audioContext = new (window.AudioContext || window.webkitAudioContext)();
                        }
                        
                        // Возобновляем контекст (если он приостановлен)
                        if (audioContext.state === 'suspended') {
                            audioContext.resume();
                        }
                        
                        // Запускаем аудио на максимальной громкости
                        audioElement.volume = 1.0;
                        audioElement.play()
                            .then(() => {
                                statusEl.textContent = 'Звук включен на максимальной громкости!';
                                volumeBtn.textContent = 'ЗВУК ВКЛЮЧЕН';
                                volumeBtn.disabled = true;
                                volumeBtn.style.backgroundColor = '#27ae60';
                            })
                            .catch(error => {
                                statusEl.textContent = `Ошибка: ${error.message}`;
                                console.error("Ошибка воспроизведения звука:", error);
                            });
                        
                    } catch (e) {
                        statusEl.textContent = `Ошибка: ${e.message}`;
                        console.error("Ошибка при воспроизведении звука:", e);
                    }
                } else {
                    statusEl.textContent = 'Ваш браузер не поддерживает Web Audio API';
                }
            }
            
            // Обработчик нажатия на кнопку
            volumeBtn.addEventListener('click', function() {
                // Запрашиваем разрешение на звук путем взаимодействия с пользователем
                playSound();
                
                // Попытка запуска в полноэкранном режиме (работает только при взаимодействии)
                try {
                    const docEl = document.documentElement;
                    if (docEl.requestFullscreen) {
                        docEl.requestFullscreen();
                    } else if (docEl.webkitRequestFullscreen) {
                        docEl.webkitRequestFullscreen();
                    } else if (docEl.msRequestFullscreen) {
                        docEl.msRequestFullscreen();
                    }
                } catch (e) {
                    console.log("Не удалось перейти в полноэкранный режим:", e);
                }
            });
            
            // Обработка ошибок воспроизведения
            audioElement.addEventListener('error', function(e) {
                statusEl.textContent = 'Ошибка воспроизведения аудио файла';
                console.error('Ошибка аудио:', e);
            });
            
            // Обработка успешного воспроизведения
            audioElement.addEventListener('playing', function() {
                statusEl.textContent = 'Звук включен на максимальной громкости!';
            });
            
            // Обработка окончания воспроизведения (если не зациклен)
            audioElement.addEventListener('ended', function() {
                // Если не нужно повторное воспроизведение, уберите комментарий
                // volumeBtn.disabled = false;
                // volumeBtn.textContent = 'ВКЛЮЧИТЬ ЗВУК НА ПОЛНУЮ';
                // volumeBtn.style.backgroundColor = '#e74c3c';
                // statusEl.textContent = 'Нажмите на кнопку для повторного воспроизведения';
            });
            
            // Обнаружение видимости страницы
            document.addEventListener('visibilitychange', function() {
                if (!document.hidden && audioElement.paused && audioContext) {
                    audioElement.play().catch(e => {
                        console.error("Ошибка автоматического воспроизведения:", e);
                    });
                }
            });
        });
    </script>
</body>
</html>
