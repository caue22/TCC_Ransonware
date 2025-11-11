
# Ransomware: A Problemática do Ataque e o Impacto do Balanceamento de Dados em Algoritmos de Classificação de Ataques

Este repositório reúne o **Trabalho de Conclusão de Curso (TCC)** de **Cauê Garcia Nascimento** e **Felipe Ribeiro de Rezende**, apresentado ao **Instituto Federal Goiano – Campus Urutaí**, no curso de **Sistemas de Informação**, sob orientação do **Prof. Dr. Gabriel da Silva Vieira**.

O estudo investiga o **impacto do balanceamento de dados** na detecção de **ataques de ransomware** por meio de **algoritmos de machine learning**, utilizando os classificadores **Random Forest** e **Decision Tree**.

---

## 📁 Estrutura do Repositório

```
├── 📄 tcc_Caue_Garcia_Felipe_Rezende.pdf        # Trabalho completo em PDF
└── 📂 notebooks/
    ├── 📂 dataset_balanceado/
    │   └── Dataset_balanceado_com_undersampling.ipynb  # Criação do dataset balanceado
    │
    ├── 📂 treinamentos/
    │   ├── Treinando_Modelo_Decision_Tree_Desbalanceado.ipynb
    │   ├── Treinando_Modelo_Random_Forest_Desbalanceado.ipynb
    │   ├── Treinando_Modelo_Decision_Tree_Balanceado.ipynb
    │   └── Treinando_Modelo_Random_Forest_Balanceado.ipynb
    │
    └── 📂 uso_modelos/
        ├── Usando_Modelo_Treinado_Decision_Tree_Desbalanceado.ipynb
        ├── Usando_Modelo_Treinado_Random_Forest_Desbalanceado.ipynb
        ├── Usando_Modelo_Treinado_Decision_Tree_Balanceado.ipynb
        └── Usando_Modelo_Treinado_Random_Forest_Balanceado.ipynb
```

📌 *A estrutura foi separada para tornar o fluxo do projeto mais claro: primeiro gera-se o dataset balanceado (caso necessário), depois treina-se os modelos e, por fim, executa-se os notebooks de uso/análise.*

---

## 🚀 Execução dos Algoritmos no Google Colab

Os notebooks estão prontos para serem executados diretamente no **Google Colab**, sem necessidade de instalação local.

### 👉 Passo a passo geral

1. **Acesse o repositório** no GitHub.

2. Abra o notebook desejado (`.ipynb`).

3. Clique no botão **“Open in Colab”** (ou adicione manualmente o prefixo abaixo ao link do arquivo):

   ```
   https://colab.research.google.com/github/<seu_usuario>/<seu_repositorio>/blob/main/caminho/do/notebook.ipynb
   ```

4. **Monte seu Google Drive** dentro do Colab, executando o trecho:

   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

5. **Execute as células sequencialmente** para reproduzir o treinamento e a avaliação dos modelos.

---

## 💾 Pré-requisitos Importantes

Para executar os notebooks corretamente, é necessário:

1. Ter uma **conta Google ativa**, pois o **Google Colab** e o **Google Drive** são utilizados para armazenar e carregar datasets e modelos.
2. Garantir que os arquivos gerados (modelos e datasets) sejam salvos no **seu Google Drive**, conforme indicado no código dos notebooks.
3. Executar as células de **montagem do Google Drive** sempre que abrir um novo notebook, para que os arquivos possam ser lidos e gravados corretamente.

---

## 🧩 Fluxo de Execução dos Modelos

O projeto é dividido em **dois fluxos principais**:
➡️ **Modelos desbalanceados** e
➡️ **Modelos balanceados (com undersampling)**.

Abaixo está o passo a passo completo para cada caso:

---

### 🔹 **Modelos Desbalanceados**

1. Execute primeiro o notebook de **treinamento** (usando o dataset original):

   * [Treinando_Modelo_Decision_Tree_Desbalanceado.ipynb](notebooks/treinamentos/Treinando_Modelo_Decision_Tree_Desbalanceado.ipynb)
   * [Treinando_Modelo_Random_Forest_Desbalanceado.ipynb](notebooks/treinamentos/Treinando_Modelo_Random_Forest_Desbalanceado.ipynb)

2. Os modelos são treinados diretamente com o **dataset original (sem balanceamento)**.

3. Após o treinamento, os arquivos do modelo são **salvos automaticamente no Google Drive**.

4. Em seguida, execute os notebooks de **uso e análise dos modelos treinados**:

   * [Usando_Modelo_Treinado_Decision_Tree_Desbalanceado.ipynb](notebooks/uso_modelos/Usando_Modelo_Treinado_Decision_Tree_Desbalanceado.ipynb)
   * [Usando_Modelo_Treinado_Random_Forest_Desbalanceado.ipynb](notebooks/uso_modelos/Usando_Modelo_Treinado_Random_Forest_Desbalanceado.ipynb)

---

### 🔹 **Modelos Balanceados (com Undersampling)**

1. Antes de treinar qualquer modelo balanceado, execute o notebook responsável por criar o dataset balanceado:

   * [Dataset_balanceado_com_undersampling.ipynb](notebooks/dataset_balanceado/Dataset_balanceado_com_undersampling.ipynb)

   Esse notebook aplica a técnica de **undersampling**, gerando um novo dataset equilibrado e salvo no Google Drive.

2. Após a geração do dataset balanceado, execute os notebooks de **treinamento dos modelos**:

   * [Treinando_Modelo_Decision_Tree_Balanceado.ipynb](notebooks/treinamentos/Treinando_Modelo_Decision_Tree_Balanceado.ipynb)
   * [Treinando_Modelo_Random_Forest_Balanceado.ipynb](notebooks/treinamentos/Treinando_Modelo_Random_Forest_Balanceado.ipynb)

3. Os modelos treinados serão salvos no Google Drive.
   Depois, rode os notebooks de **uso e análise**:

   * [Usando_Modelo_Treinado_Decision_Tree_Balanceado.ipynb](notebooks/uso_modelos/Usando_Modelo_Treinado_Decision_Tree_Balanceado.ipynb)
   * [Usando_Modelo_Treinado_Random_Forest_Balanceado.ipynb](notebooks/uso_modelos/Usando_Modelo_Treinado_Random_Forest_Balanceado.ipynb)

💡 **Importante:** o dataset balanceado precisa ser criado **apenas uma vez** — depois disso, os notebooks de treinamento podem utilizá-lo diretamente.

---

## 🧠 Objetivos do Trabalho

* Analisar o **impacto do balanceamento de dados** (usando undersampling) no desempenho dos modelos de classificação.
* Avaliar as diferenças entre datasets **balanceados e desbalanceados** na detecção de **ransomware**.
* Comparar os resultados das métricas **Precision**, **Recall**, **F1-Score** e **AUC-ROC**.

---

## 📊 Resultados Principais

* O modelo **Random Forest** apresentou melhor desempenho geral, com **AUC-ROC superior a 99%**.
* O **balanceamento de dados** proporcionou uma **distribuição mais justa dos acertos** entre as classes (`E = Encrypter`, `L = Locker`, `G = Goodware`).
* Os modelos desbalanceados mostraram **tendência a favorecer classes majoritárias**, impactando a detecção de ataques menos frequentes.

---

## 🧩 Principais Tecnologias Utilizadas

* **Python 3.10**
* **Google Colab**
* **Pandas**
* **Scikit-Learn**
* **Matplotlib / Seaborn**
* **NumPy**

---

## 👨‍💻 Autores

<p>
    <img 
      align=left 
      margin=10 
      width=80 
      src="https://avatars.githubusercontent.com/u/115797711?v=4"
    />
    <p>&nbsp&nbsp&nbspCauê Garcia Nascimento<br>
    &nbsp&nbsp&nbsp
    <a href="https://github.com/caue22">GitHub</a>&nbsp;|&nbsp;
    <a href="https://www.linkedin.com/in/cau%C3%AA-garcia-nascimento-436a14213">LinkedIn</a>

</p>
<br/><br/>
<p>
    <img 
      align=left 
      margin=10 
      width=80 
      src="https://avatars.githubusercontent.com/u/106535940?v=4"
    />
    <p>&nbsp&nbsp&nbspFelipe Ribeiro de Rezende<br>
    &nbsp&nbsp&nbsp
    <a href="https://github.com/eufrezende">GitHub</a>&nbsp;|&nbsp;
    <a href="https://www.linkedin.com/in/feliperrezende/">LinkedIn</a>

</p>

---

## 🏫 Instituição

**Instituto Federal Goiano – Campus Urutaí**

Curso de **Bacharelado em Sistemas de Informação**

Orientador: **Prof. Dr. Gabriel da Silva Vieira**