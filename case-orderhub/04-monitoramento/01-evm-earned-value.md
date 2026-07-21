# EVM — Earned Value Management

## Baseline (fim mês 5)
| Métrica | Valor |
|---------|-------|
| BAC (Budget at Completion) | R$ 1.400.000 |
| PV (Planned Value)  | R$ 840.000 |
| EV (Earned Value)   | R$ 868.000 |
| AC (Actual Cost)    | R$ 835.000 |

## Índices
| Índice | Fórmula | Valor | Interpretação |
|--------|---------|-------|---------------|
| CV | EV - AC | +R$ 33.000 | 🟢 Abaixo do custo |
| SV | EV - PV | +R$ 28.000 | 🟢 Adiantado |
| CPI | EV / AC | **1,04** | 🟢 Eficiência custo |
| SPI | EV / PV | **1,03** | 🟢 Eficiência prazo |
| EAC | BAC / CPI | R$ 1.346k | 🟢 Estimativa final |
| VAC | BAC - EAC | +R$ 54k | 🟢 Sobra prevista |

## Curva S
```mermaid
xychart-beta
    title "Curva S — PV / EV / AC (R$ mil)"
    x-axis [M1, M2, M3, M4, M5, M6, M7, M8]
    y-axis "R$ mil" 0 --> 1500
    line [120, 300, 520, 720, 840, 1050, 1250, 1400]
    line [115, 295, 530, 745, 868, 1085, 1265, 1408]
    line [110, 285, 515, 720, 835, 1050, 1230, 1355]
```
