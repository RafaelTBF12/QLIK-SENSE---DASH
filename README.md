# Criação de Dashboard em Qlik Sense

## Entendimento do Problema

### Dashboard para Acompanhamento de Entregas Integrado com Microsoft Planner


Este dashboard ajuda a empresa a entender melhor os seus indicadores financeiros, utilizando o Qlik Sense para construir uma plataforma abrangente de análise e visualização de dados. O objetivo é criar um dashboard que facilite a visualização das informações financeiras e acompanhe métricas essenciais como receita, ticket médio, lucro e vendas.

A construção deste dashboard começa com a coleta de dados financeiros detalhados, que são então organizados e carregados no Qlik Sense. Uma vez no Qlik Sense, esses dados são transformados em visualizações dinâmicas e interativas, permitindo uma análise aprofundada e em tempo real das finanças da empresa.

O dashboard inclui várias seções e gráficos que destacam diferentes aspectos das operações financeiras:

   <p align="center">
   <img src= "P1 - OVERVIEW.jpeg">

### Passos Seguidos

1. **Carregar dados no Qlik Sense Desktop**: Integração com arquivos excel.

2. **Preparação dos Dados no Desktop**: As colunas que não "Hórario", "Task ID" e "Identificação" foram desflegada pois não tinham uso em nossos visuais

3. **Editor de Texto**: Notepad ++

   <p align="center">
   <img src= "P1 - NOTEPAD++.jpeg">   
   
5. **FrameWork para Designer**: BootStrap adicionado ao Head do HTML
      
        <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css">
       <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
       <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.2.0/js/bootstrap.min.js"></script>


    Adicionando div de container:
   
       container-fluid
       row
       col-xs-  1 a 12
       col-md-  1 a 12
   
3. **KPI's**:
   
Criação de KPI para:
- Receita
- Ticket Médio
- Lucro
- Vendas

Além dessas métricas principais, o dashboard pode incluir filtros interativos que permitem aos usuários segmentar os dados por período, região, produto ou qualquer outra dimensão relevante. Isso proporciona uma visão personalizada e detalhada das finanças, adaptada às necessidades de diferentes usuários dentro da empresa

4. **Graficos Gerais**
   
   <p align="center">
   <img src= "P2 - Geral.jpeg">
    
    MÉDIA DE DIAS DE ENTREGA = 
        
        avg({<Ano_Ordem={"$(=MAX(Ano_Ordem))"}>} Dias_Entrega)


     Comprimento de Meta = 
        
       if((avg({<Ano_Ordem={"$(=MAX(Ano_Ordem))"}>} Dias_Entrega)/21)>1,1-((avg({<Ano_Ordem={"$(=MAX(Ano_Ordem))"}>} Dias_Entrega)/21)-1),1)

   

## Resultado Final

O dashboard criado fornece uma visão abrangente das operações de entrega, permitindo um acompanhamento eficiente das tarefas e facilitando a tomada de decisões estratégicas. Com a integração do Microsoft Planner ao Power BI, a empresa consegue monitorar o progresso das entregas e a performance da equipe em tempo real, promovendo uma gestão mais eficaz e proativa.
