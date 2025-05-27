# **Relatório do Projeto de Modelagem Dimensional**

## **1\. Introdução**

Este projeto demonstra a criação de um modelo dimensional simplificado utilizando dados simulados de vendas de uma empresa. O objetivo principal é ilustrar os conceitos fundamentais de modelagem dimensional, incluindo fatos, medidas e dimensões, e como os dados podem ser estruturados para análise eficiente.

## **2\. Metodologia**

O projeto foi desenvolvido utilizando Python com as bibliotecas Pandas e Xarray. A metodologia pode ser dividida nas seguintes etapas:

1. **Geração de Dados Simulados:**  
   * Foi criado um DataFrame do Pandas para simular dados de vendas.  
   * O DataFrame contém as colunas:  
     * `date`: Datas das vendas.  
     * `sales_amount`: Valores das vendas.  
     * `product_id`: Identificadores dos produtos.  
   * Os dados de `sales_amount` foram gerados aleatoriamente para simular diferentes valores de vendas.  
   * Os dados de `product_id` foram escolhidos aleatoriamente de um conjunto de três produtos ('P1', 'P2', 'P3').  
2. **Estruturação dos Dados:**  
   * O DataFrame foi utilizado para representar os fatos (vendas) e as medidas (valores de vendas).  
   * A coluna `date` representa a dimensão de tempo.  
   * A coluna `product_id` representa a dimensão do produto.  
   * A coluna `sales_amount` representa a medida dos fatos.  
3. **Conversão para Cubo de Dados:**  
   * A biblioteca Xarray foi utilizada para converter o DataFrame em um DataArray, que representa um cubo de dados multidimensional.  
   * O DataArray permite uma manipulação e análise mais eficiente dos dados em múltiplas dimensões.  
4. **Indexação para Otimização de Consultas:**  
   * O DataFrame original foi indexado pela coluna `date` para permitir consultas mais rápidas e eficientes baseadas na data.

## **3\. Resultados**

1. **DataFrame Inicial:**  
   * Foi criado um DataFrame contendo dados simulados de vendas, com as colunas `date`, `sales_amount` e `product_id`.  
   * Este DataFrame representa a estrutura básica dos dados de vendas, onde cada linha é uma transação individual.  
2. **DataArray (Cubo de Dados):**  
   * O DataFrame foi convertido em um DataArray, proporcionando uma visão multidimensional dos dados.  
   * As dimensões do cubo são `date` e `product_id`, e a medida é `sales_amount`.  
   * Isso facilita a análise das vendas por data e produto, permitindo agregações e filtros eficientes.  
3. **DataFrame Indexado por Data:**  
   * O DataFrame foi indexado pela coluna `date`, o que otimiza as consultas baseadas em datas.  
   * Isso permite acessar rapidamente os dados de vendas para um dia específico.

## **4\. Conclusão**

Este projeto demonstrou como criar um modelo dimensional simples a partir de dados simulados de vendas. A utilização de Pandas para estruturar os dados e Xarray para criar um cubo de dados multidimensional permite uma análise mais eficiente e intuitiva das informações. A indexação do DataFrame por data também melhora o desempenho das consultas.