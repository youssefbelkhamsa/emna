<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Questionnaire</title>
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background: linear-gradient(to bottom right, #6a11cb, #2575fc);
            margin: 0;
            padding: 0;
            color: #333;
        }
        .container {
            max-width: 700px;
            margin: 30px auto;
            background: #fff;
            border-radius: 12px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
            overflow: hidden;
        }
        .header {
            background: #4a90e2;
            color: #fff;
            text-align: center;
            padding: 20px;
        }
        .header h1 {
            font-size: 24px;
            margin: 0;
        }
        .header p {
            font-size: 14px;
            margin: 10px 0 0;
        }
        .content {
            padding: 20px;
        }
        .question {
            margin-bottom: 20px;
        }
        .question label {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 10px;
            display: block;
        }
        .options {
            list-style: none;
            padding: 0;
            margin: 10px 0;
        }
        .options li {
            margin-bottom: 12px;
        }
        .options input[type="radio"],
        .options input[type="checkbox"] {
            margin-right: 10px;
        }
        .slider-container {
            margin: 15px 0;
        }
        .slider-container input[type="range"] {
            width: 100%;
        }
        .slider-labels {
            display: flex;
            justify-content: space-between;
            font-size: 14px;
            margin-top: 10px;
        }
        .footer {
            text-align: center;
            padding: 20px;
            background: #f1f1f1;
            border-top: 1px solid #ddd;
        }
        .footer button {
            background: #4a90e2;
            color: #fff;
            border: none;
            padding: 12px 25px;
            font-size: 16px;
            font-weight: bold;
            border-radius: 8px;
            cursor: pointer;
            transition: background 0.3s;
        }
        .footer button:hover {
            background: #357ab9;
        }
        .add-option {
            font-size: 14px;
            color: #4a90e2;
            cursor: pointer;
            text-decoration: none;
            margin-top: 8px;
            display: inline-block;
        }
        .add-option:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Questionnaire sur les drogues addictives</h1>
            <p>Vos réponses nous aident à comprendre les comportements liés à la consommation de drogues.</p>
        </div>
        <div class="content">
            <!-- Question 1 -->
            <div class="question">
                <label>Quelle est votre tranche d'âge ?</label>
                <ul class="options">
                    <li><input type="radio" name="age" value="moins_de_18"> Moins de 18 ans</li>
                    <li><input type="radio" name="age" value="18_24"> 18-24 ans</li>
                    <li><input type="radio" name="age" value="25_34"> 25-34 ans</li>
                    <li><input type="radio" name="age" value="35_44"> 35-44 ans</li>
                    <li><input type="radio" name="age" value="45_plus"> 45 ans et plus</li>
                </ul>
            </div>
            <!-- Question 2 -->
            <div class="question">
                <label>À quel âge avez-vous commencé à consommer des drogues ?</label>
                <ul class="options">
                    <li><input type="radio" name="start_age" value="moins_de_15"> Moins de 15 ans</li>
                    <li><input type="radio" name="start_age" value="15_18"> 15-18 ans</li>
                    <li><input type="radio" name="start_age" value="19_24"> 19-24 ans</li>
                    <li><input type="radio" name="start_age" value="25_30"> 25-30 ans</li>
                    <li><input type="radio" name="start_age" value="plus_de_30"> Plus de 30 ans</li>
                </ul>
                <a href="#" class="add-option">Ajouter une option ou ajouter "Autre"</a>
            </div>
            <!-- Question 3 -->
            <div class="question">
                <label>Quelles drogues avez-vous consommées ? (cochez tout ce qui s'applique)</label>
                <ul class="options">
                    <li><input type="checkbox" name="drugs" value="cannabis"> Cannabis</li>
                    <li><input type="checkbox" name="drugs" value="cocaine"> Cocaïne</li>
                    <li><input type="checkbox" name="drugs" value="heroine"> Héroïne</li>
                    <li><input type="checkbox" name="drugs" value="meth"> Méthamphétamines</li>
                    <li><input type="checkbox" name="drugs" value="autres"> Autres</li>
                </ul>
            </div>
            <!-- Question 4 -->
            <div class="question">
                <label>Quelles sont les raisons de votre consommation ? (cochez tout ce qui s'applique)</label>
                <ul class="options">
                    <li><input type="checkbox" name="reasons" value="curiosite"> Curiosité</li>
                    <li><input type="checkbox" name="reasons" value="pression_pairs"> Pression des pairs</li>
                    <li><input type="checkbox" name="reasons" value="stress"> Stress</li>
                    <li><input type="checkbox" name="reasons" value="evasion"> Évasion</li>
                    <li><input type="checkbox" name="reasons" value="autres"> Autres</li>
                </ul>
                <a href="#" class="add-option">Ajouter une option ou ajouter "Autre"</a>
            </div>
            <!-- Question 5 -->
            <div class="question">
                <label>Avez-vous déjà été en traitement pour une dépendance ?</label>
                <ul class="options">
                    <li><input type="radio" name="treatment" value="oui"> Oui</li>
                    <li><input type="radio" name="treatment" value="non"> Non</li>
                </ul>
            </div>
            <!-- Question 6 -->
            <div class="question slider-container">
                <label>Sur une échelle de 1 à 10, dans quelle mesure pensez-vous que la consommation de drogues affecte votre santé ?</label>
                <input type="range" min="1" max="10" step="1" name="health_impact" value="5">
                <div class="slider-labels">
                    <span>1</span>
                    <span>10</span>
                </div>
            </div>
        </div>
        <div class="footer">
            <button>Soumettre</button>
        </div>
    </div>
</body>
</html>
