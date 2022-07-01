# Primeira-simula-o-no-html
Minha primeira experiência com páginas em html

index.html 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-widt, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Document</title>
</head>
<body>
    <div class="wrapper">
        <div class="checkbox-wrapper">
            <input type="checkbox" id="toggle">
            <label class="checkbox" for="toggle">
                <div class="trace"></div>
                <div class="trace"></div>
                <div class="trace"></div>
            </label>
        </div>
    </div>               
</body>
</html>

// Em uma outra abra identificada na linguagem css//

style.css
// Esse * que se inicia é indicado para apresentação simples como só simulação de imagens mesmo //

* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

.wrapper {
    background-color: rgb(221, 163, 171);
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.checkbox {
    width: 100px;
    height: 100px;
    display: flex;
    justify-content: center;
    position: relative;
    cursor: pointer;
}

.checkbox .trace {
    width: 90px;
    height: 8px;
    background-color: white;
    position: absolute;
    border-radius: 4px;
    transition: 0.5s ease-in-out;
}

.checkbox .trace:nth-child(1) {
    top: 26px;
    transform: rotate(0);
}

.checkbox .trace:nth-child(2) {
    top: 46px;
    transform: rotate(0);
}

.checkbox .trace:nth-child(3) {
    top: 66px;
    transform: rotate(0);
}

#toggle {
    display: none;
}

#toggle:checked + .checkbox .trace:nth-child(1) {
    transform: rotate(45deg);
    top: 47px;
}

#toggle:checked + .checkbox .trace:nth-child(2) {
    transform: translate(-100px);
    width: 30px;
    visibility: hidden;
    opacity: 0;
}

#toggle:checked + .checkbox .trace:nth-child(3) {
    transform: rotate(-45deg);
    top: 48px;
}
