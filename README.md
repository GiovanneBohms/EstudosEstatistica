## Para verificar os gráficos teste em GeoGebra
```
https://www.geogebra.org/calculator
```

## 📈 Regressão Linear Simples


### 1️⃣ Dados de Entrada
<img src="https://github.com/user-attachments/assets/259acc83-b91e-4e7e-b420-13de1a2c6d95" width="400"/>

```
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 4, 6]
```

### 2️⃣ Somatórios
- Soma de x: ∑x = 1 + 2 + 3 + 4 + 5 = **15**
- Soma de y: ∑y = 2 + 3 + 5 + 4 + 6 = **20**
- Soma de x²: ∑x² = 1² + 2² + 3² + 4² + 5² = **55**
- Soma de xy: ∑xy = 1×2 + 2×3 + 3×5 + 4×4 + 5×6 = **69**
- Número de pontos: n = **5**

### 3️⃣ Coeficiente Angular (**b**)
Fórmula:
```text
b = (n * ∑xy - ∑x * ∑y) / (n * ∑x² - (∑x)²)
```
Substituindo:
```text
b = (5×69 - 15×20) / (5×55 - 15²) = (345 - 300) / (275 - 225) = 45 / 50 = 0.9
```

### 4️⃣ Intercepto (**a**)
Fórmula:
```text
a = (∑y - b * ∑x) / n
```
Substituindo:
```text
a = (20 - 0.9×15) / 5 = (20 - 13.5) / 5 = 1.3
```

### 5️⃣ Equação da Reta de Regressão
```
y = 1.3 + 0.9x
```

### 6️⃣ Interpretação Visual
- Reta **ascendente** porque **b = 0.9 > 0**
- Para cada +1 em x, y aumenta em média **0.9**
- A reta cruza o eixo y no ponto (0, **1.3**)



## 📚 Desvio Padrão, Variância e Distribuição Normal

Este resumo explica de forma detalhada e passo a passo os conceitos de **variância**, **desvio padrão** e a **distribuição normal**, utilizando exemplos numéricos simples.

---

### 1️⃣ Dados de Entrada

Vamos trabalhar com o seguinte conjunto de dados, que representa as notas de 5 estudantes:

```
Dados: 6, 8, 10, 12, 14
```

---

### 2️⃣ Cálculos Intermediários

#### 🧮 Passo 1: Calcular a média (𝑥̄)

A média é dada pela soma de todos os valores dividida pela quantidade de dados.

- ∑x = 6 + 8 + 10 + 12 + 14 = **50**
- n = 5

```text
Média (x̄) = ∑x / n = 50 / 5 = 10
```

#### 🧮 Passo 2: Calcular os desvios em relação à média

Agora, vamos subtrair a média de cada valor e depois elevar o resultado ao quadrado:

| Valor (x) | x - x̄ | (x - x̄)² |
|-----------|--------|-----------|
| 6         | -4     | 16        |
| 8         | -2     | 4         |
| 10        | 0      | 0         |
| 12        | 2      | 4         |
| 14        | 4      | 16        |

- ∑(x - x̄)² = 16 + 4 + 0 + 4 + 16 = **40**

---

### 3️⃣ Aplicação da Fórmula

#### 🧮 Fórmula da **variância amostral** (s²):

> A variância é a média dos quadrados dos desvios em relação à média.

```text
s² = ∑(x - x̄)² / (n - 1)
```

```makefile
Substituindo:
s² = 40 / (5 - 1) = 40 / 4 = 10
```

#### 🧮 Fórmula do **desvio padrão amostral** (s):

> O desvio padrão é a raiz quadrada da variância.

```text
s = √s² = √10 ≈ 3,16
```

---

### 4️⃣ Resultado Final

```bash
✅ Variância amostral (s²) = 10
✅ Desvio padrão amostral (s) ≈ 3,16
```

---

### 5️⃣ Interpretação

- A **média** das notas é 10.
- A **variância** de 10 indica o grau de dispersão dos dados ao redor da média.
- O **desvio padrão** de aproximadamente **3,16** mostra que, em média, as notas estão cerca de 3 pontos afastadas da média.
- Como o desvio padrão é **baixo em relação à média**, os dados estão **moderadamente concentrados**.

---

## 📊 Distribuição Normal e Curva Normal

A **distribuição normal** (ou curva de Gauss) é uma função de densidade simétrica em forma de sino.

---

### 1️⃣ Propriedades da Curva Normal

- Média = Mediana = Moda
- Simétrica em torno da média
- Área total sob a curva = 1 (ou 100%)
- Regida pela fórmula:

```text
f(x) = (1 / (σ√(2π))) * e^(-(x - μ)² / (2σ²))
```

```makefile
Substituindo:
f(x) = (1 / (3.16√(2π))) * e^(-(x - 10)^2 / (2 * 3.16^2))
```
Onde:

- μ = 10, é a média
- σ = 3.16, é o desvio padrão
- e é a base do logaritmo natural
- x é o valor da variável

---

### 2️⃣ Regra Empírica (Regra 68-95-99.7)

Em uma distribuição normal:

- **68%** dos dados estão entre **μ ± 1σ**
- **95%** dos dados estão entre **μ ± 2σ**
- **99,7%** dos dados estão entre **μ ± 3σ**

```bash
Exemplo com μ = 10 e σ = 3,16:
68% dos dados entre: 10 ± 3,16 → [6,84 a 13,16]
95% dos dados entre: 10 ± 6,32 → [3,68 a 16,32]
```

---

### 3️⃣ Interpretação da Distribuição Normal

- A distribuição normal é amplamente usada porque **muitos fenômenos naturais** (altura, pressão, QI) seguem esse padrão.
- Se os dados têm distribuição normal, **previsões probabilísticas** são mais confiáveis.
- O **desvio padrão** define a **largura** da curva: quanto maior o desvio, mais "espalhada" ela é.

---

## ✅ Conclusão

- **Variância** e **desvio padrão** são fundamentais para entender a **dispersão dos dados**.
- A **distribuição normal** permite analisar e prever a **probabilidade de ocorrência** de eventos.
- Esses conceitos são essenciais em estatística, ciência de dados e engenharia.
