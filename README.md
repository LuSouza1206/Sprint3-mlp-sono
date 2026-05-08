# Sprint 3 — MLP: Predição de Qualidade do Sono

#Integrantes :

- Kaio Vinicius Meireles Alves - RM553282
- Lucas Alves de Souza -  RM553956
- Lucas de Freitas Pagung -  RM553242
- Guilherme Fernandes de Freitas - RM554323
- João Pedro Chizzolini de Freitas - RM553172

> Projeto desenvolvido para a disciplina de Inteligência Artificial.  
> App de Saúde Digital — promoção de bem-estar e hábitos saudáveis.

---

# Problema

Usuários de apps de saúde não conseguem identificar quais hábitos diários prejudicam seu sono. O modelo prevê se o usuário terá uma boa ou má qualidade de sono com base em dados comportamentais coletados pelo app, devolvendo recomendações personalizadas.

---

# Dataset

**Sleep Health and Lifestyle Dataset** — Kaggle  
🔗 https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset

- 400 registros de adultos
- 13 variáveis (estresse, atividade física, duração do sono, IMC, passos diários, etc.)
- Tarefa: classificação binária — sono bom (1) ou ruim (0)

---

# Arquitetura da MLP
Entrada (9 features) → Oculta 1 (64, ReLU) → Oculta 2 (32, ReLU) → Saída (2 classes)

| Parâmetro | Valor |
|---|---|
| Otimizador | Adam |
| Taxa de aprendizado | 0.001 |
| Early stopping | Ativo |
| Épocas até convergência | 27 |

---

# Resultados

| Métrica | Valor |
|---|---|
| Acurácia | **94.7%** |
| Precision (classe Boa) | 0.93 |
| Recall (classe Boa) | 1.00 |
| F1-score médio | 0.95 |
| Baseline (Dummy) | 69.3% |

> O modelo supera o baseline em **+25.4 pontos percentuais**.

---

# Como rodar

1. Acessa o Google Colab: https://colab.research.google.com
2. Faz upload do arquivo `notebook_mlp_sono.ipynb`
3. Faz upload do dataset CSV do Kaggle
4. Executa as células em ordem

Ou clona o repositório e roda localmente:

```bash
git clone https://github.com/LuSouza1206/Sprint3-mlp-sono.git
cd sprint3-mlp-sono
pip install scikit-learn pandas numpy matplotlib seaborn
python mlp_sono.py
```

---

# Tecnologias

- Python 3.10+
- scikit-learn
- pandas / numpy
- matplotlib / seaborn
- Google Colab

---

# Estrutura do repositório
sprint3-mlp-sono/
├── README.md
├── mlp_sono.py
├── notebook_mlp_sono.ipynb
└── assets/
├── eda_sono.png
├── resultados_mlp.png
└── matriz_confusao.png

