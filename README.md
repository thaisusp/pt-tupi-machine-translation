# Tradução Automática de Baixo Recurso: Português ↔ Tupi Antigo

Repositório oficial do **Exercício Programa 2 (EP2)** da disciplina **MAC0508 - Introdução ao Processamento de Língua Natural (USP)**. Este projeto avalia o desempenho de LLMs (*Large Language Models*) na tradução entre Português e Tupi Antigo, explorando regimes *Zero-Shot* e *Fine-Tuning*.

## Autores
* **Gustavo Ribeiro Bernardo** (NUSP: 14577174)
* **Thaís Martins de Sousa** (NUSP: 14608786)

## Estrutura do Projeto

── data
│   ├── processed
│   │   ├── test_modern.csv
│   │   ├── test.csv
│   │   ├── train_modern.csv
│   │   ├── train.csv
│   │   ├── val_modern.csv
│   │   └── val.csv
│   ├── raw
│   │   ├── Cópia de portugues-guarani-tupi antigo.xlsx
│   │   └── tupiantigo_portugues_moderno.csv
│   ├── tupi_portugues_moderno_limpo.csv
│   ├── tupi_portugues_moderno.csv
│   └── tupi_portugues_original_limpo.csv
├── enunciado_ep2_mac0508.pdf
├── main.py
├── README.md
├── Relatório EP2 - MAC0508 - Tradução Tupi Português.pdf
├── requirements.txt
├── results
│   ├── metrics
│   │   ├── RELATORIO_FINAL_NLLB_ANTIGO.csv
│   │   ├── RELATORIO_FINAL_NLLB_MODELOFINETUNED.csv
│   │   ├── RELATORIO_FINAL_NLLB_MODERNO.csv
│   │   └── RELATORIO_FINAL_ZEROSHOT.csv
│   ├── models
│   └── predictions
│       ├── few_shot
│       │   ├── traducoes_antigo_ida_modelofinetuned_antigo.csv
│       │   ├── traducoes_antigo_ida_modelofinetuned_moderno.csv
│       │   ├── traducoes_antigo_volta_modelofinetuned_antigo.csv
│       │   ├── traducoes_antigo_volta_modelofinetuned_moderno.csv
│       │   ├── traducoes_moderno_ida_modelofinetuned_antigo.csv
│       │   ├── traducoes_moderno_ida_modelofinetuned_moderno.csv
│       │   ├── traducoes_moderno_volta_modelofinetuned_antigo.csv
│       │   └── traducoes_moderno_volta_modelofinetuned_moderno.csv
│       └── zero-shot
│           ├── results_mbart_antigo.csv
│           ├── results_mbart_moderno.csv
│           ├── results_mt5_antigo.csv
│           ├── results_mt5_moderno.csv
│           ├── results_nllb_antigo.csv
│           └── results_nllb_moderno.csv
└── src
    ├── gerar_predicoes.py
    ├── plots.ipynb
    ├── treino.py
    └── zero_shot.py

# Modelos e Estratégias

Modelo	Arquitetura	Estratégia Zero-Shot
mBART-50	Encoder-Decoder	Placeholder pt_XX (Forcing)
NLLB-200	Encoder-Decoder	Proxy grn_Latn (Guarani)
mT5-small	Text-to-Text	Prompt "translate Portuguese to Tupi..."

# Metodologia

Dados: Córpus paralelo Português-Tupi (Rezende, 2025). Inclui versão em Português Moderno (via GPT-4o) para reduzir a perplexidade dos modelos.

# Métricas:

BLEU: Precisão de n-gramas.

chrF3: F-score de caracteres com peso na cobertura (recall), ideal para a morfologia aglutinativa do Tupi.

# Como Executar
Instalação:

Bash
pip install -r requirements.txt
Reprodução:

Execute os notebooks na ordem numérica.

Para o Fine-Tuning, utilize GPU (T4 ou superior).
=======
# tradutor-pt-tupi-ep2
End-to-end NLP pipeline for PT–Old Tupi translation: preprocessing, zero-shot baselines, fine-tuning, metrics and analysis.

## **🚧 This project is still under active development 🚧**
Features, experiments, and documentation will be added soon
>>>>>>> 9a145e143c535279e367763e508a2d6a301b91cc
