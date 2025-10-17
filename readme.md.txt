# Análise Estatística de Experimento (Teste A/B) com Python

![Status](https://img.shields.io/badge/status-concluído-green) ![Python](https://img.shields.io/badge/Python-3.11-blue?style=flat&logo=python) ![Statsmodels](https://img.shields.io/badge/Statsmodels-0.13-blue?style=flat)

Este projeto apresenta uma análise estatística completa de um experimento de **Teste A/B**, desde a limpeza dos dados e formulação da hipótese até a execução do teste estatístico e a **recomendação de negócio baseada em evidências**. O objetivo é determinar se uma nova página de um site (`treatment`) gera uma taxa de conversão superior à página antiga (`control`).

Este tipo de análise é uma das ferramentas mais poderosas para times de **Produto e Marketing**, pois permite tomar decisões de alto impacto com rigor científico.

---

## 📈 Metodologia

O fluxo de trabalho seguiu as melhores práticas para análise de experimentos:

1.  **Limpeza e Preparação dos Dados:** Foram removidas inconsistências (usuários expostos a ambos os grupos) e duplicatas para garantir a validade estatística do experimento.
2.  **Formulação da Hipótese:**
    *   **Hipótese Nula (H₀):** A nova página tem uma taxa de conversão menor ou igual à da página antiga (`p_nova ≤ p_antiga`).
    *   **Hipótese Alternativa (H₁):** A nova página tem uma taxa de conversão superior à da página antiga (`p_nova > p_antiga`).
3.  **Teste Estatístico:** Foi utilizado um **Teste Z para duas proporções** da biblioteca `Statsmodels` com um nível de significância (α) de **5%**.
4.  **Conclusão Estatística:** O p-valor resultante do teste foi comparado com o nível de significância para decidir se há evidências para rejeitar a hipótese nula.

---

## 🛠️ Tecnologias Utilizadas

*   **Linguagem:** Python 3
*   **Ambiente:** Jupyter Notebook (via VS Code)
*   **Bibliotecas:**
    *   `Pandas`: Para manipulação e análise dos dados.
    *   `NumPy`: Para operações numéricas.
    *   `Statsmodels`: Para a execução do teste Z estatístico.
    *   `Matplotlib`: Para visualização de dados.
*   **Dataset:** [A/B Testing Dataset](URL_DO_DATASET_NO_KAGGLE) - *Adicionar o link direto para a página do dataset no Kaggle.*

---

## 🚀 Conclusão e Recomendação de Negócio

A análise estatística resultou em um **p-valor de 0.9052**. Como este valor é muito maior que o nosso limiar de significância (α = 0.05), **falhamos em rejeitar a Hipótese Nula.**

**Recomendação de Negócio:**
**Não há evidências estatísticas para justificar o lançamento da nova página para todos os usuários.** A pequena diferença de conversão observada entre os grupos pode ser meramente fruto do acaso. **Recomenda-se manter a versão antiga da página (controle)** e que o time de produto utilize os aprendizados deste teste para formular novas hipóteses e iterar no design.

---

## ⚙️ Como Executar a Análise

1.  Clone este repositório.
2.  Crie um ambiente virtual e instale as dependências: `pip install pandas numpy matplotlib statsmodels`.
3.  Abra o arquivo `analise_ab.ipynb` em um ambiente Jupyter.
4.  Execute as células em ordem para reproduzir a análise.