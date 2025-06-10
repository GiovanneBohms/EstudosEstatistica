
# 📈 Regressão Linear Simples
<img src="https://github.com/user-attachments/assets/259acc83-b91e-4e7e-b420-13de1a2c6d95" width="400"/>


## 1️⃣ Dados de Entrada
```JS
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 4, 6]
```

## 2️⃣ Somatórios
- Soma de x: ∑x = 1 + 2 + 3 + 4 + 5 = **15**
- Soma de y: ∑y = 2 + 3 + 5 + 4 + 6 = **20**
- Soma de x²: ∑x² = 1² + 2² + 3² + 4² + 5² = **55**
- Soma de xy: ∑xy = 1×2 + 2×3 + 3×5 + 4×4 + 5×6 = **69**
- Número de pontos: n = **5**

## 3️⃣ Coeficiente Angular (**b**)
Fórmula:
```text
b = (n * ∑xy - ∑x * ∑y) / (n * ∑x² - (∑x)²)
```
Substituindo:
```text
b = (5×69 - 15×20) / (5×55 - 15²) = (345 - 300) / (275 - 225) = 45 / 50 = **0.9**
```

## 4️⃣ Intercepto (**a**)
Fórmula:
```text
a = (∑y - b * ∑x) / n
```
Substituindo:
```text
a = (20 - 0.9×15) / 5 = (20 - 13.5) / 5 = **1.3**
```

## 5️⃣ Equação da Reta de Regressão
```
y = 1.3 + 0.9x
```

## 6️⃣ Interpretação Visual
- Reta **ascendente** porque **b = 0.9 > 0**
- Para cada +1 em x, y aumenta em média **0.9**
- A reta cruza o eixo y no ponto (0, **1.3**)
