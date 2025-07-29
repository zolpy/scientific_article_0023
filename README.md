<!-- Tab simulation using details -->

<details open>
<summary>🇧🇷 Português</summary>

Artigo Científico – Análise Preditiva da Composição Química do Café

Este repositório contém o conjunto de dados sintéticos e o código-fonte (notebooks Jupyter) utilizados nas análises apresentadas no artigo científico: "Análise Preditiva da Composição Fitoquímica do Café Utilizando Modelos de Regressão e uma Base de Dados Sintética de Alta Fidelidade".

O objetivo deste projeto é demonstrar a viabilidade da aplicação de técnicas de Machine Learning para prever a concentração de compostos químicos chave em café (Cafeína, Trigonelina, Ácidos Clorogênicos), utilizando uma base de dados sintética e robusta, fundamentada em um estudo de referência sobre cafés italianos em cápsula.

🎯 Objetivo do Repositório

Este repositório visa garantir a reprodutibilidade completa dos experimentos e análises descritos no artigo científico associado. Ele permite a exploração, validação ou adaptação dos modelos preditivos para a composição química do café. Serve como um recurso para pesquisadores interessados na aplicação de aprendizado de máquina à química de alimentos e quimiometria, particularmente utilizando conjuntos de dados sintéticos para superar a escassez de dados públicos.

📁 Estrutura do Repositório

/data/: Contém a base de dados sintética.

📄 base_sintetica_cafe.xlsx: Dataset com 10.010 registros, simulando a composição química de 65 tipos diferentes de cafés em cápsula, com suas respectivas variáveis de entrada (Volume, proxies de blend) e de saída (Cafeína, Trigonelina, Total_CQAs).

/notebooks/: Contém os notebooks Jupyter com todo o fluxo de análise.

📄 01_geracao_dados_sinteticos.ipynb: Código para a geração da base de dados sintética com base nos parâmetros estatísticos (média, desvio padrão) e na estrutura de correlação (inferida do PCA) do estudo de referência.

📄 02_analise_exploratoria_e_selecao_features.ipynb: Análise exploratória dos dados (Heatmaps de Correlação) e seleção de variáveis com base na correlação e na importância de features do Random Forest.

📄 03_benchmark_modelos_regressao.ipynb: Treinamento e avaliação de mais de 20 modelos de regressão para prever cada composto químico, utilizando validação cruzada k-fold.

📄 04_interpretabilidade_modelos_com_xai.ipynb: Análise de interpretabilidade (XAI) dos melhores modelos utilizando as bibliotecas SHAP e a análise de Dependência Parcial (PDP) para entender as relações não-lineares e as interações.

📄 05_analise_clustering_nao_supervisionada.ipynb: Aplicação do algoritmo K-Means para descobrir "personas" ou perfis químicos de café de forma não supervisionada.

📄 06_previsao_em_novos_cenarios.ipynb: Código final que utiliza os melhores modelos treinados para fazer previsões em um conjunto de novos cenários hipotéticos de blends de café.

/figures/: Contém as visualizações geradas pelos notebooks.

📄 correlation_heatmap.png: Matriz de correlação de Pearson e Spearman entre as variáveis.

📄 r2_performance_caffeine.png: Gráfico de barras comparando o R² dos modelos para predição de Cafeína.

📄 diagnostic_plots_trigonelline.png: Gráficos de diagnóstico (Previsto vs. Real, Resíduos) para o melhor modelo de Trigonelina.

📄 shap_summary_plot_trigonelline.png: Gráfico de resumo SHAP mostrando a importância e o impacto das features.

📄 pdp_interaction_plot.png: Gráfico de Dependência Parcial de Interação (2D).

📄 kmeans_elbow_plot.png: Gráfico do método do cotovelo para determinar o número ideal de clusters.

📄 pca_clusters_visualization.png: Visualização dos clusters descobertos em um espaço 2D (PCA).

/results/: Armazena as métricas de desempenho dos modelos em formato CSV.

📄 metricas_performance_caffeine.csv: Métricas (R², MAE, RMSE) para os modelos de predição de Cafeína.

📄 metricas_performance_trigonelline.csv: Métricas para os modelos de predição de Trigonelina.

📄 metricas_performance_total_cqas.csv: Métricas para os modelos de predição de CQAs Totais.

/article/: Contém os arquivos-fonte do manuscrito.

📄 manuscrito.tex: Código-fonte LaTeX do artigo científico.

📄 referencias_pt.bib: Arquivo de bibliografia BibTeX.

📝 Observações Metodológicas

Todos os dados são sintéticos, gerados com base nos parâmetros estatísticos (médias e desvios-padrão) e na estrutura de correlação reportados no estudo de referência de Angelino et al. (2018), Niacin, alkaloids and (poly)phenolic compounds in the most widespread Italian capsule-brewed coffees.

A lógica de geração dos dados buscou refletir as interações químicas e botânicas plausíveis (e.g., diferenças entre grãos Arábica e Robusta, efeitos da torra), mas é, por natureza, uma simulação controlada.

As dependências Python necessárias para executar os notebooks estão listadas no arquivo requirements.txt.

🚀 Como Utilizar

Clone o repositório:

Generated bash
git clone https://github.com/[seu-usuario]/analise_preditiva_cafe.git
cd analise_preditiva_cafe


Instale as dependências:

Generated bash
pip install -r requirements.txt
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END

Execute os notebooks: Abra os notebooks na pasta /notebooks/ utilizando Jupyter Lab ou Google Colab para replicar as análises.

📄 Como Citar

Se você utilizar este repositório, a base de dados ou os conceitos apresentados no artigo, por favor cite o trabalho original (a citação completa será atualizada após a publicação):

Autor(es). (Ano). Análise Preditiva da Composição Fitoquímica do Café Utilizando Modelos de Regressão e uma Base de Dados Sintética de Alta Fidelidade. Nome do Periódico, Volume(Edição), Páginas. DOI (se disponível)

⚖️ Licença

Este projeto está licenciado sob a Licença MIT.

</details>

<details>
<summary>🇺🇸 English</summary>

Scientific Article – Predictive Analysis of Coffee's Chemical Composition

This repository contains the synthetic dataset and source code (Jupyter notebooks) used in the analyses presented in the scientific article: "Predictive Analysis of Coffee's Phytochemical Composition Using Regression Models and a High-Fidelity Synthetic Database".

The goal of this project is to demonstrate the feasibility of applying Machine Learning techniques to predict the concentration of key chemical compounds in coffee (Caffeine, Trigonelline, Chlorogenic Acids), using a robust, synthetic database grounded in a reference study on Italian capsule-brewed coffees.

🎯 Repository Objective

This repository aims to ensure full reproducibility of the experiments and analyses described in the associated scientific article. It allows for the exploration, validation, or adaptation of predictive models for coffee's chemical composition. It serves as a resource for researchers interested in applying machine learning to food chemistry and chemometrics, particularly by using synthetic datasets to overcome the scarcity of public data.

📁 Repository Structure

/data/: Contains the synthetic dataset.

📄 synthetic_coffee_database.xlsx: Dataset with 10,010 records, simulating the chemical composition of 65 different types of capsule coffees, with their respective input variables (Volume, blend proxies) and output variables (Caffeine, Trigonelline, Total_CQAs).

/notebooks/: Contains the Jupyter notebooks with the entire analysis workflow.

📄 01_synthetic_data_generation.ipynb: Code for generating the synthetic dataset based on statistical parameters (mean, std dev) and the correlation structure (inferred from PCA) of the reference study.

📄 02_exploratory_analysis_and_feature_selection.ipynb: Exploratory data analysis (Correlation Heatmaps) and feature selection based on correlation and Random Forest feature importance.

📄 03_regression_model_benchmarking.ipynb: Training and evaluation of over 20 regression models to predict each chemical compound, using k-fold cross-validation.

📄 04_model_interpretability_with_xai.ipynb: Interpretable AI (XAI) analysis of the best models using SHAP and Partial Dependence Plot (PDP) to understand non-linear relationships and interactions.

📄 05_unsupervised_clustering_analysis.ipynb: Application of the K-Means algorithm to discover "coffee personas" or chemical profiles in an unsupervised manner.

📄 06_prediction_on_new_scenarios.ipynb: Final code that uses the best-trained models to make predictions on a set of new hypothetical coffee blend scenarios.

/figures/: Contains visualizations generated by the notebooks.

📄 correlation_heatmap.png: Pearson and Spearman correlation matrix between variables.

📄 r2_performance_caffeine.png: Bar chart comparing the R² scores of models for Caffeine prediction.

📄 diagnostic_plots_trigonelline.png: Diagnostic plots (Predicted vs. Actual, Residuals) for the best Trigonelline model.

📄 shap_summary_plot_trigonelline.png: SHAP summary plot showing feature importance and impact.

📄 pdp_interaction_plot.png: Partial Dependence Interaction Plot (2D).

📄 kmeans_elbow_plot.png: Elbow method plot to determine the optimal number of clusters.

📄 pca_clusters_visualization.png: Visualization of the discovered clusters in a 2D space (PCA).

/results/: Stores model performance metrics in CSV format.

📄 performance_metrics_caffeine.csv: Metrics (R², MAE, RMSE) for Caffeine prediction models.

📄 performance_metrics_trigonelline.csv: Metrics for Trigonelline prediction models.

📄 performance_metrics_total_cqas.csv: Metrics for Total CQAs prediction models.

/article/: Contains the source files for the manuscript.

📄 manuscript.tex: LaTeX source code for the scientific article.

📄 references_en.bib: BibTeX bibliography file.

📝 Methodological Notes

All data are synthetic, generated based on the statistical parameters (means and standard deviations) and correlation structure reported in the reference study by Angelino et al. (2018), Niacin, alkaloids and (poly)phenolic compounds in the most widespread Italian capsule-brewed coffees.

The data generation logic aimed to reflect plausible chemical and botanical interactions (e.g., differences between Arabica and Robusta beans, roasting effects) but is, by nature, a controlled simulation.

The Python dependencies required to run the notebooks are listed in the requirements.txt file.

🚀 How to Use

Clone the repository:

Generated bash
git clone https://github.com/[your-username]/coffee-predictive-analysis.git
cd coffee-predictive-analysis
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END

Install dependencies:

Generated bash
pip install -r requirements.txt
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Bash
IGNORE_WHEN_COPYING_END

Run the notebooks: Open the notebooks in the /notebooks/ folder using Jupyter Lab or Google Colab to replicate the analyses.

📄 How to Cite

If you use this repository, the dataset, or the concepts presented in the article, please cite the original work (full citation will be updated upon publication):

Author(s). (Year). Predictive Analysis of Coffee's Phytochemical Composition Using Regression Models and a High-Fidelity Synthetic Database. Journal Name, Volume(Issue), Pages. DOI (if available)

⚖️ License

This project is licensed under the MIT License.

</details>
