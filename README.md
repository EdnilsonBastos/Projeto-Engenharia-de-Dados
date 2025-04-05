# Projeto-Engenharia-de-Dados

Meu amigo possui  um salão de beleza que utiliza um sistema desktop para registrar os pagamentos dos clientes pelos serviços feitos pelos profissionais do Salão. Ele deseja analisar os dados gerados pelo sistema para obter insights que o ajudem na tomada de decisões e na descoberta de informações estratégicas.
As principais perguntas que ele deseja obter respostas são:

1.	Qual o faturamento anual da empresa?
2.	Quais prestadores receberam os maiores valores durante o ano?
3.	Quais são os serviços mais vendidos?
4.	Qual foi o mês com maior receita de cada ano?
5.	Qual o lucro mensal da empresa, considerando um gasto fixo de R$ 10.000,00 por mês?
6.	Qual a forma de pagamento mais utilizada pelos clientes?
7.	Com base nas informações coletadas, quais estratégias podem ser adotadas para aumentar o faturamento do salão?<br><br>

<center><strong>Explicação do arquivos Notebook:</strong></center><br>
Importar_arquivos.ipyn - > Importar os arquivos (.csv) para os dataframes.<br>
Bronze.ipynb - > Gera as tabelas no database Bronze com seus respectivos dataframes carregados.<br>
Prata.ipynb - > Trata os dataframes retirando colunas em branco, troca o tipo de coluna e altera os dados de uma coluna. Gera o database Prata com os dataframes tratados.<br>
Ouro.ipynb - > Responde as perguntas atráves do comando SQL. Cria a tabela flat no database Ouro.<br><br>

<center><strong>MODELO</strong></center><br><br>

<IMG SRC='https://github.com/EdnilsonBastos/Projeto-Engenharia-de-Dados/blob/main/modelo.jpg'/><br><br>

<strong>RELACIONAMENTOS DA TABELAS</strong><br><br>

CLIENTE  --> COMANDA_CLIENTE<br>
ID_CLIENTE da tabela “CLIENTE” com ID_CLIENTE da tabela “COMANDA_CLIENTE”
Incluir TODOS os registros de 'CLIENTES' e somente os registros de 'COMANDACLIENTE' quando os campos unidos forem iguais.<br>
	
PRESTADOR  --> COMANDACLIENTE<br>
ID_PRESTADOR da tabela “PRESTADOR” com ID_PRESTADOR da tabela “COMANDA_CLIENTE”
Incluir TODOS os registros de 'PRESTADOR' e somente os registros de 'COMANDACLIENTE' quando os campos unidos forem iguais.

SERVICOS  --> COMANDACLIENTE<br>
ID_SERVICO da tabela “SERVICOS” com ID_SERVICO da tabela “COMANDA_CLIENTE”
Incluir TODOS os registros de 'SERVICOS' e somente os registros de 'COMANDACLIENTE' quando os campos unidos forem iguais.

COMANDA --> COMANDACLIENTE<br>
ID_COMANDA da tabela “COMANDA” com ID_COMANDA da tabela “COMANDA_CLIENTE”
Incluir TODOS os registros de 'COMANDA' e somente os registros de 'COMANDACLIENTE' quando os campos unidos forem iguais.

PAGAMENTOS --> COMANDA<br>
ID_COMANDA da tabela “PAGAMENTOS” com ID_COMANDA da tabela “COMANDA”
Incluir TODOS os registros de 'COMANDA' e somente os registros de 'PAGAMENTOS' quando os campos unidos forem iguais.

<strong>CATALAGO DE DADOS DA CAMADA BRONZE</strong><br><br>
<IMG SRC='https://github.com/EdnilsonBastos/Projeto-Engenharia-de-Dados/blob/main/catalogobronze.JPG'/><br>
<IMG SRC='https://github.com/EdnilsonBastos/Projeto-Engenharia-de-Dados/blob/main/catalogobronze1.JPG'/><br>
<IMG SRC='https://github.com/EdnilsonBastos/Projeto-Engenharia-de-Dados/blob/main/catalogobronze2.JPG'/><br>



