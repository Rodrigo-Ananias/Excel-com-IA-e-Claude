Desafio "Criando uma Dashboard da Porsche com Claude e ChatGPT com Canvas"

_1° parte: Tratamento da Planilha - 

1° Fornecimento da "Planilha_base_Porsche.xlsx" e criação da schema.md com a "receita de bolo" para fazer a limpeza dos dados. Seguido do Prompt no Claude "Crie um Agent que leia o "Planilha_base_Porsche.xlsx" e aplique as regras do "schema.md" para gerar um novo arquivo tratado." Que resultou em 2 arquivos, sendo um o "porsche_sanitize_agent.py" e o outro "Planilha_Porsche_Tratada.xlsx"

-Tratamento da "Planilha_Porsche_Tratada.xlsx"

Com a planilha pré-tratada, abrimos ela e fizemos as adequações nas colunas Sanitized necessárias (convertemos texto em número, removemos casas decimais, fizemos substituições - . to , - e demais limpezas identificadas. Depois, excluímos as colunas originais (com preenchimento vermelho) com exceção de "customer_name" e "salesperson". Removemos o "Log_Tratamento" e, por fim, salvamos e criamos uma cópia com o nome "Planilha_base_Porsche(Sanitizada).xlsx".



_ 2° parte: Instruções dadas ao ChatGPT + Canvas

1° - Forneça a planilha "Planilha_base_Porsche(Sanitizada).xlsx" ao ChatGPT e insira os comandos abaixo:

- Comandos dados ao ChatGPT + Canvas

Utilizando o recurso de canvas, renderize uma dashboard em html ao lado

#Filtro

-> Porsche Model
-> Model Year
-> City
-> State

# Perguntas de Negócio e KPIs

1° Qual é a Porsche mais vendida no universo?
2° Qual é a Porsche mais vendida por cidade?
3° Qual é a Porsche mais vendida por Estado?


Essas perguntas foram feitas para que o usuário tenha uma visão exclusiva voltada as vendas. Nelas são destacadas informações chaves, como o modelo mais vendido, o estado com o maior número de vendas; o faturamento anual dentre outras. Então, caso o tomador de decisões queira fazer uma campanha de vendas ele pode direcionar nos modelos de Porsche mais vendidas por cada estado e assim por diante.

# Interface do site

Sobre o ui/ux, se baseie no site oficial da Porsche brasil:
https://www.porsche.com/brazil/pt/

Tenha um ar elegante e refinado.

_ Complementando o Dashboard

Depois de gerada a primeira Dashboard, adicionei mais pedidos como

1° Inclua, também

-> faturamento médio por modelo
-> o faturamento anual
-> o ticket médio por modelo

2° Adicione um novo filtro na dashboard
-> Estado


3° Depois, faça a tradução dos filtros, como:

Porsche Model -> Modelo Porsche;
Model Year -> Ano do Modelo;
City -> Cidade;
Pay Method -> Método de Pagamento

4° Por fim, traduza as formas de pagamento, como:

Credit Card -> Cartão de Crédito;
Cash -> Dinheiro;
Debit Card -> Cartão de Débito
Wire Transfer -> Transferência Bancária (Wire)

- Link da Dashboard criada

Finalizado o dashboard em html, upei ele no repositório do GitHub.

Link: https://rodrigo-ananias.github.io/Dashboard_da_Porsche/