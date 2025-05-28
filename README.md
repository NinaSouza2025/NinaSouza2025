# 📊 Boot Invest – Simulador de Investimentos Mensais

Este projeto é uma simulação de investimento mensal baseada em salário, rendimento da carteira e taxa de juros compostos. A ferramenta foi idealizada para oferecer uma visão clara sobre como o hábito de investir periodicamente pode gerar um patrimônio acumulado ao longo do tempo.

---

## 🧮 Parâmetros de Entrada

Abaixo estão os dados de entrada que o usuário pode configurar:

| Parâmetro                         | Valor Exemplo | Descrição |
|----------------------------------|---------------|-----------|
| **Salário**                      | R$ 1.582,00   | Renda mensal usada como base para a sugestão de investimento. |
| **Rendimento da Carteira (%)**  | 0,5% (0.005)  | Rentabilidade esperada da carteira, usada para sugerir o valor a ser investido mensalmente. |
| **Sugestão de Investimento (30%)** | R$ 474,60   | Calculado como 30% do salário. Fórmula: `Salário * 0.3` |
| **Quanto investir por mês?**     | R$ 50,00      | Valor efetivo que será investido mensalmente. |
| **Por quantos anos?**            | 1             | Período de investimento, em anos. |
| **Taxa de rendimento mensal (%)**| 0,79% (0.0079)| Rentabilidade efetiva dos investimentos. |
| **Patrimônio acumulado**         | R$ 626,77     | Valor final ao término do período de aplicação mensal. Calculado com juros compostos. |

---

## 📐 Fórmulas Utilizadas

### 1. Sugestão de Investimento Mensal (30%)

\[
\text{Investimento Sugerido} = \text{Salário} \times 0,3
\]

---

### 2. Patrimônio Acumulado com Aportes Mensais (Juros Compostos)

\[
FV = P \times \frac{(1 + i)^n - 1}{i}
\]

Onde:

- \( FV \): Patrimônio acumulado  
- \( P \): Aporte mensal (quanto investir por mês)  
- \( i \): Taxa de rendimento mensal (em formato decimal)  
- \( n \): Número total de períodos (meses)

#### Exemplo aplicado:
- \( P = 50 \)
- \( i = 0,0079 \)
- \( n = 12 \) (1 ano)

\[
FV = 50 \times \frac{(1 + 0{,}0079)^{12} - 1}{0{,}0079} \approx 626{,}77
\]

---

## 🛠️ Processo Técnico

1. **Definição do salário base**: usado para sugerir um valor de investimento mensal.
2. **Determinação da taxa de rendimento esperada**: aplicada para simular o crescimento do patrimônio.
3. **Cálculo do aporte mensal**: o usuário define quanto irá investir.
4. **Cálculo do patrimônio acumulado**: aplica-se a fórmula de juros compostos com aportes mensais.

---

## 💡 Observações

- A taxa de rendimento mensal deve estar em formato decimal (ex: 0.0079 para 0,79%).
- O período de tempo é convertido para meses ao multiplicar os anos por 12.
- A simulação não leva em conta impostos, taxas ou inflação.

