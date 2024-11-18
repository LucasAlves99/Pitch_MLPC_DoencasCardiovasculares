# Previsão de Doenças Cardiovasculares com Redes Neurais

Este é um projeto desenvolvido para o **pitch de pós-graduação**, cujo objetivo é prever a probabilidade de ocorrência de **doenças cardiovasculares** em pacientes, utilizando **redes neurais artificiais**. O modelo foi treinado em um conjunto de dados relevante e obteve uma **acurácia de 86.9%** e **f1-score de 88% para a classe predita**, o que demonstra a eficácia do método para realizar previsões precisas.

---

## Índice

1. [Sobre](#sobre)
2. [Objetivo do Projeto](#objetivo-do-projeto)
3. [Tecnologias e Bibliotecas](#tecnologias-e-bibliotecas)
4. [Instalação e uso](#instalação-e-uso)
5. [Resultados](#resultados)
6. [Desafios](#desafios)
7. [Licença](#licença)

---

## Sobre

Este projeto visa a **previsão de doenças cardiovasculares** utilizando um modelo de **rede neural**. Os dados utilizados para treinar o modelo são de uma [base pública](https://archive.ics.uci.edu/dataset/45/heart+disease), com informações relacionadas a fatores de risco conhecidos para doenças cardíacas, como pressão arterial, níveis de colesterol,BPM, entre outros.

Após o treinamento, o modelo foi capaz de alcançar uma **acurácia de 86.9%** e **f1-score de 88% para a classe predita**, o que demonstra um bom desempenho para previsões em tempo real. O projeto é uma aplicação direta de técnicas de **aprendizado de máquina**.

---

## Objetivo do Projeto

O objetivo deste projeto é **prever a probabilidade de doenças cardiovasculares** com base em variáveis clínicas e comportamentais. A rede neural foi escolhida , pois foi um dos conteúdos estudados no último módulo(requisito do pitch)

- **Entrada**: Dados sobre fatores de risco cardiovascular (ex: pressão arterial, colesterol, BPM, etc.).
- **Saída**: Probabilidade de o paciente ter ou não uma doença cardiovascular.

O modelo foi implementado utilizando bibliotecas **scikit-learn**, e treinado com dados de um conjunto de dados amplamente utilizado, como o conjunto de dados de [Cardiovascular Disease Data](https://archive.ics.uci.edu/dataset/45/heart+disease).

---

## Tecnologias e Bibliotecas

Este projeto foi desenvolvido utilizando as seguintes tecnologias e bibliotecas:

- **Python** (linguagem de programação principal)
- **ucimlrepo** (Importar os dados)
- **Scipy** (Estatística)
- **Pandas** (para manipulação de dados)
- **NumPy** (para operações numéricas)
- **Matplotlib / Seaborn** (para visualização de dados)
- **Scikit-learn** (para pré-processamento de dados, métricas de avaliação e modelagem)

---

## Instalação

### Requisitos

- **Python** (versão 3.6 ou superior)
- **Pip** (gerenciador de pacotes Python)

### Passos para instalação

1. Clone este repositório:
    ```bash
    git clone https://github.com/LucasAlves99/Pitch_MLPC_DoencasCardiovasculares.git
    ```

2. Acesse a pasta do projeto:
    ```bash
    cd nome-do-projeto
    ```

3. Crie e ative um ambiente virtual:
    ```bash
    python -m venv nome_do_ambiente
    source nome_do_ambiente/bin/activate # Para sistemas Unix
    nome_do_ambiente\Scripts\activate # Para Windows
    ```

4. Instale as dependências necessárias:
    ```bash
    pip install -r requirements.txt
    ```

### Arquivo `requirements.txt`

Este repositório inclui um arquivo `requirements.txt` contendo todas as dependências necessárias para rodar o projeto. Basta executar o comando acima para instalar todos os pacotes.

---

## Uso

### Predição do Modelo

#### Carregar o pipeline
```bash
pipeline_carregado = joblib.load('pipeline_completo.pkl')
```
#### Fazer previsões com o pipeline carregado
```bash
predicoes = pipeline_carregado.predict(X_teste)
```
---

## Resultados

O modelo alcançou uma acurácia de 86.9%, f1-score da classe prevista de 88%, e 
uma curva ROC de 0.71. Resultados bons, é eficaz para prever doenças cardiovasculares.

---

## Desafios 
- Dúvidas sobre algumas features.

- Tive que reduzir a complexidade da classe target, Reduzindo seus grupos (Sem doença cardíaca,Chance mínima de doença cardíaca, Chance moderada de doença cardíaca, Chance significativa de doença cardíaca, Chance máxima de doença cardíaca) para (Saudável, chance de doença cardíaca), o que resultou em um aumento em todas as métricas de avaliação.

---


## Licença

MIT License [LICENSE.md](LICENSE.md) 
