# 🏚️ Predição de Tempo de Duração dos Mantimentos em Abrigos

Este projeto desenvolve um modelo de regressão utilizando redes neurais para estimar o **tempo médio de duração dos mantimentos (comida, água e remédios) em abrigos**, considerando suas capacidades e estoques. Essa previsão busca auxiliar na gestão de recursos, planejamento logístico e tomada de decisões em situações emergenciais ou humanitárias.

## 📋 Descrição do Problema

A gestão de recursos em abrigos é um desafio constante, especialmente em cenários de emergência. Saber **quantos dias os mantimentos disponíveis irão durar**, considerando variáveis como o número de vagas ocupadas e os estoques de comida, água e remédios, permite um gerenciamento mais eficiente e proativo.

## 📑 Índice

- [🔧 Funcionalidades](#-funcionalidades)
- [🚀 Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [🗂️ Estrutura dos Dados](#-estrutura-dos-dados)
- [🔨 Etapas do Projeto](#-etapas-do-projeto)
- [📈 Resultados Esperados](#-resultados-esperados)
- [💡 Melhorias Futuras](#-melhorias-futuras)
- [▶️ Como Executar](#-como-executar)
- [📜 Licença](#-licença)
- [👥 Autores](#-autores)

## 🔧 Funcionalidades

- Análise exploratória dos dados dos abrigos.
- Treinamento de uma rede neural para previsão do tempo de duração dos mantimentos.
- Avaliação do desempenho do modelo com métricas de regressão.
- Geração de previsões para cada abrigo com base nos estoques e capacidade.

## 🚀 Tecnologias Utilizadas

- 🐍 Python
- 📊 Pandas e NumPy (manipulação de dados)
- 📈 Seaborn e Matplotlib (visualização de dados)
- 🧠 Scikit-Learn (pré-processamento e divisão dos dados)
- 🔗 TensorFlow / Keras (modelagem da rede neural)

## 🗂️ Estrutura dos Dados

| Coluna               | Descrição                                    |
|----------------------|-----------------------------------------------|
| id_abrigo            | Identificador único do abrigo                |
| vagas_disponiveis    | Número de vagas disponíveis no abrigo        |
| estoque_comida       | Quantidade de comida disponível (unidade)    |
| estoque_agua         | Quantidade de água disponível (litros)       |
| estoque_remedios     | Quantidade de remédios disponíveis (unidade) |
| tempo_duracao        | Tempo de duração dos mantimentos (target, em dias) |

## 🔨 Etapas do Projeto

### ✔️ Importação de Bibliotecas
- Pacotes para manipulação de dados, visualização e construção de modelos.

### ✔️ Carregamento dos Dados
- Leitura do arquivo CSV contendo os dados dos abrigos.

### ✔️ Análise Exploratória
- Verificação de tipos de dados e possíveis inconsistências.
- Visualização da distribuição dos estoques e capacidade dos abrigos.

### ✔️ Pré-processamento dos Dados
- Seleção das features: `vagas_disponiveis`, `estoque_comida`, `estoque_agua`, `estoque_remedios`.
- Normalização dos dados com `MinMaxScaler`.

### ✔️ Divisão dos Dados
- Separação em treino (70%) e teste (30%) com `train_test_split`.

### ✔️ Modelagem
- Arquitetura da rede neural:
  - 🔸 1ª camada: 16 neurônios (ReLU)
  - 🔸 2ª camada: 8 neurônios (ReLU)
  - 🔸 Camada de saída: 1 neurônio (ReLU) — saída contínua (regressão)
- Otimizador: **Adam**
- Função de perda: **Erro Quadrático Médio (MSE)**

### ✔️ Treinamento
- 40 épocas, validação de 20% dos dados de treino.

### ✔️ Avaliação do Modelo
- Métricas utilizadas:
  - 🔹 MAE (Erro Médio Absoluto)
  - 🔹 MSE (Erro Quadrático Médio)
  - 🔹 RMSE (Raiz do Erro Quadrático Médio)
  - 🔹 R² (Coeficiente de Determinação)

### ✔️ Predição
- Estimativa do tempo de duração dos mantimentos para cada abrigo.

## 📈 Resultados Esperados

O modelo prevê **quantos dias os mantimentos de um abrigo irão durar**, permitindo:

- Melhor gestão dos recursos.
- Planejamento antecipado de reabastecimento.
- Redução de riscos de falta de suprimentos.

## 💡 Melhorias Futuras

- Testar outros algoritmos de regressão (Random Forest, XGBoost, etc.).
- Implementação de validação cruzada para maior robustez.
- Otimização da arquitetura da rede neural.
- Implementação de uma API para disponibilizar o modelo.
- Inserção de novas variáveis, como fluxo de entrada e saída de pessoas.

## ▶️ Como Executar

1. Clone este repositório.
2. Execute o código em um ambiente como **Google Colab**, **Jupyter Notebook** ou localmente.
3. Garanta que o arquivo `abrigos_com_tempo_duracao_balanceado.csv` esteja na pasta correta ou vinculado ao seu ambiente.

## 📜 Licença

Projeto desenvolvido para fins acadêmicos e educacionais.

## 👥 Autores

| Nome	                    | RM     | GitHub                                      |
|---------------------------|--------|---------------------------------------------|
| Fernanda Budniak de Seda  | 558274 | [Febudniak](https://github.com/Febudniak)   |
| Lucas Lerri de Almeida    | 554635 | [lerri05](https://github.com/lerri05)       |
| Karen Marques dos Santos  | 554556 | [KarenMarquesS](https://github.com/KarenMarquesS) |
