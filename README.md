<!doctype html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interfaz Similar</title>
    <style>
        :root {
            --primary-color: #4CAF50;
            --secondary-color: #007BFF;
            --premium-color: #FFD700;
            --text-color: #333;
            --background-color: #f0f0f0;
            --white-color: #fff;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: var(--background-color);
            margin: 0;
            padding: 0;
        }

        .header {
            background-color: var(--primary-color);
            color: var(--white-color);
            text-align: center;
            padding: 20px 0;
            position: relative;
        }

        .icon-button {
            position: absolute;
            width: 40px;
            height: 40px;
            background-color: var(--white-color);
            border: none;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
        }

        .icon-button.profile-button {
            top: 10px;
            left: 10px;
        }

        .icon-button.notification-icon {
            top: 10px;
            right: 10px;
        }

        .icon-button .icon {
            font-size: 24px;
            color: var(--primary-color);
        }

        .search-bar {
            width: 100%;
            max-width: 600px;
            margin: 20px auto;
            position: relative;
        }

        .search-input {
            width: 100%;
            padding: 10px 50px 10px 20px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 20px;
            box-sizing: border-box;
        }

        .search-button {
            position: absolute;
            top: 50%;
            right: 10px;
            transform: translateY(-50%);
            background-color: var(--secondary-color);
            color: var(--white-color);
            border: none;
            padding: 10px 20px;
            border-radius: 20px;
            font-weight: bold;
            cursor: pointer;
        }

        .premium-button {
            background-color: var(--premium-color);
            color: black;
            border: none;
            padding: 15px 30px;
            border-radius: 20px;
            font-weight: bold;
            cursor: pointer;
            margin-top: 20px;
        }

        .container {
            padding: 20px;
            max-width: 600px;
            margin: 0 auto;
            background-color: var(--white-color);
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .date-selector {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .date-selector .date {
            display: flex;
            gap: 5px;
        }

        .date-selector .date div {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            background-color: #eaeaea;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
        }

        .date-selector .date .active {
            background-color: var(--secondary-color);
            color: var(--white-color);
        }

        .macros {
            display: flex;
            justify-content: space-around;
            margin-top: 10px;
        }

        .macros div {
            text-align: center;
        }

        .macros div p {
            margin: 0;
        }

        .progress-bars {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 20px;
        }

        .progress-bar {
            width: 100%;
            height: 10px;
            background-color: #e0e0e0;
            border-radius: 5px;
            overflow: hidden;
            position: relative;
            margin-left: 10px;
        }

        .progress-bar div {
            height: 100%;
            background-color: var(--secondary-color);
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            transition: width 0.3s;
        }

        .food-section {
            margin-top: 20px;
        }

        .meal {
            margin-bottom: 20px;
        }

        .meal h3 {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .meal h3 .more-options {
            font-size: 1.5em;
            cursor: pointer;
        }

        .meal .add-food {
            display: flex;
            justify-content: center;
            align-items: center;
            border: 1px dashed #ccc;
            border-radius: 5px;
            padding: 10px;
            cursor: pointer;
        }

        .meal .add-food span {
            font-size: 2em;
        }

        .footer {
            display: flex;
            justify-content: space-around;
            background-color: var(--secondary-color);
            padding: 10px 0;
            margin-top: 20px;
        }

        .footer div {
            color: white;
            text-align: center;
        }

        .footer div:hover {
            background-color: #0056b3;
            cursor: pointer;
            padding: 10px 0;
            border-radius: 5px;
        }

        .footer-icon {
            font-size: 1.5em;
        }

        .footer-text {
            font-size: 0.9em;
        }

        .circular-progress {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background-color: #e0e0e0;
            position: relative;
            margin: 20px auto;
        }

        .circular-progress::after {
            content: "0 / 2233 kcal";
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 1.2em;
            text-align: center;
        }

        .progress-ring {
            stroke-dasharray: 440;
            stroke-dashoffset: 440;
            transition: stroke-dashoffset 0.3s;                     
       }
       
        }

        .water-intake {
            margin-top: 20px;
            text-align: center;
        }

        .water-intake h3 {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .water-intake .cups {
            display: flex;
            justify-content: center;
            gap: 5px;
            margin-top: 10px;
        }

        .water-intake .cup {
            width: 30px;
            height: 60px;
            border: 1px solid #ccc;
            border-radius: 5px;
            position: relative;
            background-color: #e0e0e0;
            cursor: pointer;
        }

        .water-intake .cup .filled {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            background-color: var(--primary-color);
            height: 0;
            transition: height 0.3s;
        }
        
        .floating-button {
    position: fixed;
    bottom: 50%;
    right: 20px;
    transform: translateY(50%);
    width: 60px;
    height: 60px;
    background-color: var(--secondary-color);
    color: var(--white-color);
    border: none;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 24px;
    cursor: pointer;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
    z-index: 1000;
}

.shortcut-bar {
    position: fixed;
    bottom: 50%;
    right: 100px;
    transform: translateY(50%);
    background-color: var(--secondary-color);
    color: var(--white-color);
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 10px;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
    z-index: 1000;
    transition: opacity 0.3s, visibility 0.3s;
}

.shortcut-bar.hidden {
    opacity: 0;
    visibility: hidden;
}

.shortcut-bar div {
    display: flex;
    align-items: center;
    gap: 10px;
    cursor: pointer;
}

.shortcut-bar div:hover {
    background-color: #0056b3;
    padding: 5px;
    border-radius: 5px;
}

.floating-button {
    position: fixed;
    bottom: 50%;
    right: 20px;
    transform: translateY(50%);
    width: 60px;
    height: 60px;
    background-color: var(--secondary-color);
    color: var(--white-color);
    border: none;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 24px;
    cursor: pointer;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
    z-index: 1000;
    user-select: none;
}
    </style>
</head>
<body>
    <header class="header">
        <button class="icon-button profile-button" aria-label="Perfil"><span class="icon">👤</span></button>
        <h1>myfitnesspal</h1>
        <button class="icon-button notification-icon" aria-label="Notificaciones">🔔</button>
    </header>

    <div style="text-align: center;">
        <button class="premium-button">PASAR A PREMIUM <span>👑</span></button>
    </div>
    <div class="search-bar">
        <input type="text" class="search-input" placeholder="Busca un alimento...">
        <button class="search-button">Buscar</button>
    </div>

    <div class="container">
        <div class="date-selector">
            <div class="date">
                <div>13</div>
                <div>14</div>
                <div>15</div>
                <div>16</div>
                <div class="active">17</div>
                <div>18</div>
                <div>19</div>
            </div>
            <div>
                <span>May 17</span>
            </div>
        </div>

        <div class="circular-progress">
            <svg width="150" height="150">
                <circle cx="75" cy="75" r="70" fill="none" stroke="#e0e0e0" stroke-width="10"/>
                <circle cx="75" cy="75" r="70" fill="none" stroke="#4CAF50" stroke-width="10" class="progress-ring"/>
            </svg>
        </div>

        <div class="macros">
            <div>
                <p>Proteínas</p>
                <div class="progress-bar">
                    <div></div>
                </div>
                <p>0 / 113 g</p>
            </div>
            <div>
                <p>Carbs</p>
                <div class="progress-bar">
                    <div></div>
                </div>
                <p>0 / 250 g</p>
            </div>
            <div>
                <p>Grasas</p>
                <div class="progress-bar">
                    <div></div>
                </div>
                <p>0 / 87 g</p>
            </div>
        </div>

        <div class="food-section">
            <div class="meal">
                <h3>Desayuno <span class="more-options">⋮</span></h3>
                <div class="add-food">
                                    <span>+</span>
            </div>
        </div>
        <div class="meal">
            <h3>Media Mañana <span class="more-options">⋮</span></h3>
            <div class="add-food">
                <span>+</span>
            </div>
        </div>
        <div class="meal">
            <h3>Almuerzo <span class="more-options">⋮</span></h3>
            <div class="add-food">
                <span>+</span>
            </div>
        </div>
        <div class="meal">
            <h3>Media Tarde <span class="more-options">⋮</span></h3>
            <div class="add-food">
                <span>+</span>
            </div>
        </div>
        <div class="meal">
            <h3>Cena <span class="more-options">⋮</span></h3>
            <div class="add-food">
                <span>+</span>
            </div>
        </div>
        
        <!-- Sección de consumo de agua -->
            <div class="meal">
                <h3>Agua <span class="more-options">⋮</span></h3>
                <div class="water-intake">
                    <div class="cups">
                        <div class="cup" onclick="fillCup(this)"><div class="filled"></div></div>
                        <div class="cup" onclick="fillCup(this)"><div class="filled"></div></div>
                        <div class="cup" onclick="fillCup(this)"><div class="filled"></div></div>
                        <div class="cup" onclick="fillCup(this)"><div class="filled"></div></div>
                        <div class="cup" onclick="fillCup(this)"><div class="filled"></div></div>
                        <div class="cup" onclick="fillCup(this)"><div class="filled"></div></div>
                        <div class="cup" onclick="fillCup(this)"><div class="filled"></div></div>
                        <div class="cup" onclick="fillCup(this)"><div class="filled"></div></div>
                        <div class="cup" onclick="fillCup(this)"><div class="filled"></div></div>
                        <div class="cup" onclick="fillCup(this)"><div class="filled"></div></div>
                    </div>
    </div>
</div>

<div class="footer">
    <div>
        <div class="footer-icon">🏠</div>
        <div class="footer-text">Plan</div>
    </div>
    <div>
        <div class="footer-icon">📖</div>
        <div class="footer-text">Base Datos</div>
    </div>
    <div>
        <div class="footer-icon">👨‍🍳</div>
        <div class="footer-text">Recetas</div>
    </div>
    <div>
        <div class="footer-icon">👥</div>
        <div class="footer-text">Teams</div>
    </div>
    <div>
        <div class="footer-icon">📈</div>
        <div class="footer-text">Progreso</div>
    </div>
</div>

<button class="floating-button" aria-label="Atajos">+</button>
<div class="shortcut-bar hidden">
    <div>
        <div class="footer-icon">⚙️</div>
        <div class="footer-text">Configurar Nutrición</div>
    </div>
    <div>
        <div class="footer-icon">📈</div>
        <div class="footer-text">Registra tu Progreso</div>
    </div>
    <div>
        <div class="footer-icon">⏰</div>
        <div class="footer-text">Configuración de Recordatorios</div>
    </div>
    <div>
        <div class="footer-icon">🛒</div>
        <div class="footer-text">Lista de Compras</div>
    </div>
    <div>
        <div class="footer-icon">👨‍🍳</div>
        <div class="footer-text">Crear Receta</div>
    </div>
    <div>
        <div class="footer-icon">🔥</div>
        <div class="footer-text">Configurar Calorías</div>
    </div>
    <div>
        <div class="footer-icon">🍴</div>
        <div class="footer-text">Configurar Macros</div>
    </div>
    <div>
        <div class="footer-icon">💧</div>
        <div class="footer-text">Configurar Agua</div>
    </div>
    <div>
        <div class="footer-icon">🍽️</div>
        <div class="footer-text">Número de Comidas</div>
    </div>
    <div>
        <div class="footer-icon">🔄</div>
        <div class="footer-text">Sincronizar Plan</div>
    </div>
</div>

<script>
  
    function fillCup(cup) {
            const filled = cup.querySelector('.filled');
            if (filled.style.height === '100%') {
                filled.style.height = '0';
            } else {
                filled.style.height = '100%';
            }
            }
  
    document.addEventListener('DOMContentLoaded', () => {
        const proteinProgress = document.querySelectorAll('.progress-bar div')[0];
        const carbsProgress = document.querySelectorAll('.progress-bar div')[1];
        const fatProgress = document.querySelectorAll('.progress-bar div')[2];

        // Example values, these should be updated dynamically
        let proteinConsumed = 0;
        let proteinGoal = 113;
        let carbsConsumed = 0;
        let carbsGoal = 250;
        let fatConsumed = 0;
        let fatGoal = 87;

        proteinProgress.style.width = `${(proteinConsumed / proteinGoal) * 100}%`;
        carbsProgress.style.width = `${(carbsConsumed / carbsGoal) * 100}%`;
        fatProgress.style.width = `${(fatConsumed / fatGoal) * 100}%`;

        const progressRing = document.querySelector('.progress-ring');
        let totalCaloriesConsumed = 0;
        let totalCaloriesGoal = 2233;
        const radius = progressRing.r.baseVal.value;
        const circumference = radius * 2 * Math.PI;

        progressRing.style.strokeDasharray = `${circumference} ${circumference}`;
        progressRing.style.strokeDashoffset = circumference;

        function setProgress(percent) {
            const offset = circumference - (percent / 100) * circumference;
            progressRing.style.strokeDashoffset = offset;
        }

        setProgress((totalCaloriesConsumed / totalCaloriesGoal) * 100);
    });
    
    const floatingButton = document.querySelector('.floating-button');
    const shortcutBar = document.querySelector('.shortcut-bar');

    floatingButton.addEventListener('click', () => {
        shortcutBar.classList.toggle('hidden');
    });

    floatingButton.addEventListener('mousedown', function(event) {
        event.preventDefault(); // Para prevenir comportamiento predeterminado del botón

        let shiftX = event.clientX - floatingButton.getBoundingClientRect().left;
        let shiftY = event.clientY - floatingButton.getBoundingClientRect().top;

        function moveAt(pageX, pageY) {
            floatingButton.style.left = pageX - shiftX + 'px';
            floatingButton.style.top = pageY - shiftY + 'px';
        }

        function onMouseMove(event) {
            moveAt(event.pageX, event.pageY);
        }

        document.addEventListener('mousemove', onMouseMove);

        floatingButton.addEventListener('mouseup', function() {
            document.removeEventListener('mousemove', onMouseMove);
            floatingButton.onmouseup = null;
        });

        floatingButton.ondragstart = function() {
            return false;
        };
    });

</script>

</body>
</html>
