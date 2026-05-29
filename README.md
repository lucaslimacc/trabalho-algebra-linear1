# 🧮 Determinante e Inversa de Matriz em Python

<div align="center">

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucaslimacc/trabalho-algebra-linear1/blob/main/Atividade_Geo_Ana.ipynb)
![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-1.x-013243?logo=numpy&logoColor=white)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)

**Trabalho prático de Álgebra Linear e Geometria Analítica**  
Centro Universitário de Brasília — CEUB · 2026

[🌐 Ver site do projeto](https://lucaslimacc.github.io/trabalho-algebra-linear1/) · [📓 Abrir no Colab](https://colab.research.google.com/github/lucaslimacc/trabalho-algebra-linear1/blob/main/Atividade_Geo_Ana.ipynb)

</div>

---

## 📋 Sobre o Projeto

Este repositório contém a implementação em Python do cálculo do **determinante** e da **matriz inversa** de uma matriz quadrada 4×4. O trabalho foi desenvolvido como atividade prática da disciplina de Álgebra Linear e Geometria Analítica do CEUB, sob orientação do Prof. Ednardo P. Spaniol.

A matriz utilizada é inspirada na **métrica de Schwarzschild** da Relatividade Geral, expressa em coordenadas esféricas, o que torna o trabalho um ponto de contato entre a álgebra linear clássica e a física teórica.

---

## 🗂️ Estrutura do Repositório

```
📦 trabalho-algebra-linear1
 ┣ 📓 Atividade_Geo_Ana.ipynb   ← Notebook principal (entrega da atividade)
 ┣ 🌐 index.html                ← Página do GitHub Pages
 ┗ 📄 README.md                 ← Este arquivo
```

---

## 📐 A Matriz

A matriz trabalhada é definida como:

$$
A = \begin{pmatrix}
\gamma_{00} & 0 & 0 & 0 \\
0 & \gamma_{11}\sin\theta\cos\phi & r\cos\theta\cos\phi & -r\sin\theta\sin\phi \\
0 & \gamma_{11}\sin\theta\sin\phi & r\cos\theta\sin\phi &  r\sin\theta\cos\phi \\
0 & \gamma_{11}\cos\theta & -r\sin\theta & 0
\end{pmatrix}
$$

Onde os componentes γ são dados por:

$$
\gamma_{00} = \frac{r}{\sqrt{1 - \frac{2m}{r}}}, \qquad \gamma_{11} = \frac{1}{\sqrt{1 - \frac{2m}{r}}}
$$

---

## ⚙️ Funcionalidades

O notebook implementa as seguintes funções independentes:

| Função | Descrição |
|---|---|
| `construir_matriz(r, m, theta, phi)` | Monta a matriz 4×4 a partir dos parâmetros físicos |
| `calcular_determinante(matriz)` | Calcula o determinante via decomposição LU |
| `calcular_inversa(matriz)` | Calcula a inversa, com verificação de singularidade |
| `imprimir_matriz(matriz, nome)` | Exibe a matriz formatada no console |

---

## 📊 Resultados (parâmetros padrão)

Os parâmetros utilizados na execução padrão são:

| Parâmetro | Valor |
|---|---|
| `r` | `10.0` |
| `m` | `1.0` |
| `θ` (theta) | `π/4` (45°) |
| `φ` (phi) | `π/3` (60°) |

**Matriz A:**
```
  11.180340    0.000000    0.000000    0.000000
   0.000000    0.395285    3.535534   -6.123724
   0.000000    0.684653    6.123724    3.535534
   0.000000    0.790569   -7.071068    0.000000
```

**Determinante:**
```
det(A) = 883.883476
```

**Matriz Inversa A⁻¹:**
```
   0.089443    0.000000    0.000000    0.000000
   0.000000    0.316228    0.547723    0.632456
   0.000000    0.035355    0.061237   -0.070711
   0.000000   -0.122474    0.070711    0.000000
```

**Verificação:** `A × A⁻¹ = I` ✅ (erros numéricos abaixo de 10⁻¹⁵)

---

## 🚀 Como Executar

### Opção 1 — Google Colab (recomendado, sem instalação)

Clique no botão abaixo para abrir e executar o notebook diretamente no navegador:

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lucaslimacc/trabalho-algebra-linear1/blob/main/Atividade_Geo_Ana.ipynb)

### Opção 2 — Localmente

**Pré-requisitos:** Python 3.x instalado.

```bash
# 1. Clone o repositório
git clone https://github.com/lucaslimacc/trabalho-algebra-linear1.git
cd trabalho-algebra-linear1

# 2. Instale a dependência
pip install numpy

# 3. Abra o notebook
jupyter notebook Atividade_Geo_Ana.ipynb
```

> 💡 Você pode alterar os valores de `r`, `m`, `theta` e `phi` na última célula do notebook para explorar diferentes configurações da matriz.

---

## 🛠️ Tecnologias

- **Python 3** — linguagem principal
- **NumPy** — operações matriciais (`linalg.det`, `linalg.inv`)
- **Jupyter Notebook** — ambiente de execução interativo

---

## 📚 Referências

- BOLDRINI, J. L. et al. *Álgebra Linear*. 3. ed. São Paulo: Harper & Row do Brasil, 1986.
- ANTON, H.; RORRES, C. *Álgebra Linear com Aplicações*. 10. ed. Porto Alegre: Bookman, 2012.
- NumPy Documentation: [numpy.org/doc](https://numpy.org/doc/)

---

## 👤 Autor

**Lucas Cerqueira Lima**  
Centro Universitário de Brasília — CEUB  
Disciplina: Álgebra Linear e Geometria Analítica  
Professor: Ednardo P. Spaniol  
Brasília – DF · 2026
