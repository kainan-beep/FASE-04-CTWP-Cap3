# [FIAP - Faculdade de Informática e Administração Paulista](https://www.fiap.com.br/)

# Da Terra ao Código: Automatizando a Classificação de Grãos com Machine Learning

## FarmTech Solutions

## 👨‍🎓 Integrantes:
- <a href="https://www.linkedin.com/company/inova-fusca">Kainan Bilibio Aguiar</a>
- <a href="https://www.linkedin.com/company/inova-fusca">Guilherme C. Ávila</a>

## 📜 Descrição

Em cooperativas agrícolas de pequeno porte, a classificação dos grãos costuma ser feita manualmente por especialistas, um processo demorado e sujeito a erros humanos. Este projeto aplica a metodologia **CRISP-DM** para automatizar essa classificação por meio de Machine Learning, utilizando o *Seeds Dataset* do UCI Machine Learning Repository, que contém 210 amostras de grãos de trigo de três variedades (**Kama**, **Rosa** e **Canadian**), descritas por sete medidas físicas (área, perímetro, compacidade, comprimento e largura do núcleo, coeficiente de assimetria e comprimento do sulco do núcleo).

O trabalho está organizado em quatro etapas, todas implementadas no notebook [`src/classificacao_graos.ipynb`](src/classificacao_graos.ipynb):

1. **Análise e pré-processamento dos dados** — exploração do dataset, estatísticas descritivas, histogramas, boxplots, gráficos de dispersão, verificação de valores ausentes e padronização (`StandardScaler`) das características.
2. **Implementação e comparação de algoritmos de classificação** — divisão treino/teste (70/30) e treinamento de cinco modelos (KNN, SVM, Random Forest, Naive Bayes e Regressão Logística), avaliados por acurácia, precisão, recall, F1-score e matriz de confusão.
3. **Otimização dos modelos** — busca de hiperparâmetros com `GridSearchCV` para cada algoritmo, comparando o desempenho antes e depois da otimização.
4. **Interpretação dos resultados** — análise dos pontos fortes/limitações de cada modelo e dos insights extraídos para o contexto da classificação automatizada de grãos.

## 📁 Estrutura de pastas

Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:

- <b>.github</b>: arquivos de configuração específicos do GitHub para gerenciar e automatizar processos no repositório.

- <b>assets</b>: arquivos relacionados a elementos não-estruturados deste repositório, como imagens.

- <b>config</b>: arquivos de configuração usados para definir parâmetros e ajustes do projeto.

- <b>document</b>: documentos do projeto. Na subpasta "other", documentos complementares e menos importantes.

- <b>scripts</b>: scripts auxiliares para tarefas específicas do projeto (ex.: deploy, migrações, backups).

- <b>src</b>: todo o código-fonte do projeto, incluindo o notebook [`classificacao_graos.ipynb`](src/classificacao_graos.ipynb) e o dataset [`seeds_dataset.txt`](src/seeds_dataset.txt).

- <b>README.md</b>: arquivo que serve como guia e explicação geral sobre o projeto (o mesmo que você está lendo agora).

## 🔧 Como executar o código

### Pré-requisitos
- Python 3.10+ (testado com Python 3.13)
- Jupyter Notebook ou Visual Studio Code com a extensão Jupyter

### Instalação das dependências

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter notebook ipykernel
```

### Passo a passo

1. Clone o repositório:
   ```bash
   git clone https://github.com/kainan-beep/FASE-04-CTWP-Cap3.git
   cd FASE-04-CTWP-Cap3
   ```
2. Abra o notebook `src/classificacao_graos.ipynb` no Jupyter ou no VS Code.
3. Garanta que o kernel selecionado seja o Python onde as dependências foram instaladas.
4. Execute todas as células (`Run All`). O notebook lê automaticamente o arquivo `seeds_dataset.txt` localizado na mesma pasta (`src/`).

## 🗃 Histórico de lançamentos

* 1.0.0 - 17/06/2026
    * Pipeline completo de classificação dos grãos de trigo (Seeds Dataset) com CRISP-DM: análise exploratória, 5 modelos de classificação, otimização via GridSearchCV e interpretação de resultados.

## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>
