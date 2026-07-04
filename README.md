# MVP — Machine Learning & Analytics

Previsão da **segmentação assistencial** de planos de saúde (classificação multiclasse) a partir do perfil demográfico e contratual de beneficiários, usando dados públicos da Agência Nacional de Saúde Suplementar (ANS).

Trabalho desenvolvido para a Sprint de Machine Learning & Analytics da pós-graduação em Ciência de Dados e Analytics (PUC-Rio).

## Objetivo

Construir e comparar modelos de Machine Learning capazes de prever a segmentação assistencial de um plano (Ambulatorial, Hospitalar, Hospitalar e Ambulatorial, Referência ou Odontológico) com base em características como sexo, faixa etária, UF, tipo de contratação, abrangência e modalidade da operadora — apoiando o direcionamento comercial de produtos no mercado de saúde suplementar.

## Dataset

- **Fonte:** Dados de Beneficiários por Região Geográfica — ANS (Portal de Dados Abertos do Governo Federal)
- **Competência:** dezembro/2025
- **Volume:** 670.917 registros × 14 atributos
- **Arquivo:** `tb_br_2512.zip` (consumido diretamente por URL pública neste repositório)
- **Referência:** `Dicionário de Dados ANS.pdf`

## Estrutura do repositório

| Arquivo | Descrição |
|---|---|
| `MVP_Machine_Learning_Analytics_Lucas_Igreja_Mac_Laren.ipynb` | Notebook principal do projeto |
| `tb_br_2512.zip` | Base de dados da ANS (dez/2025) |
| `Dicionário de Dados ANS.pdf` | Documentação oficial das variáveis |

## Como executar

O notebook foi desenvolvido no Google Colab e executa do início ao fim sem configuração local, upload manual ou autenticação. A base é carregada diretamente pela URL pública deste repositório.

1. Abra o notebook no Google Colab.
2. Menu **Ambiente de execução → Executar tudo**.

## Metodologia

Fluxo completo de um projeto de ML:

1. **Definição do problema** — contexto, objetivo, hipóteses e critérios de sucesso.
2. **Análise exploratória** — distribuição da variável-alvo e relação das features com o alvo.
3. **Preparação dos dados** — tradução de códigos, filtros, prevenção de vazamento de dados e amostragem estratificada.
4. **Modelagem** — baseline (classe majoritária) e dois modelos candidatos (Árvore de Decisão e HistGradientBoosting), organizados em pipelines.
5. **Otimização** — ajuste de hiperparâmetros via `RandomizedSearchCV` com validação cruzada estratificada.
6. **Avaliação** — métricas coerentes com o desbalanceamento (F1 ponderado), matriz de confusão e discussão crítica de limitações.

## Principais tecnologias

Python · pandas · NumPy · scikit-learn · Matplotlib

## Autor

**Lucas Igreja Mac Laren**
Pós-graduação em Ciência de Dados e Analytics — PUC-Rio
