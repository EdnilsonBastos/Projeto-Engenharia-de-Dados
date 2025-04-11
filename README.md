# Projeto-Engenharia-de-Dados

Meu amigo possui  um salão de beleza que utiliza um sistema desktop para registrar os pagamentos dos clientes pelos serviços feitos pelos profissionais do Salão. Ele deseja analisar os dados gerados pelo sistema para obter insights que o ajudem na tomada de decisões e na descoberta de informações estratégicas.
As principais perguntas que ele deseja obter respostas são:

1.	Qual o faturamento anual da empresa?
2.	Quais os três Prestadores receberam os maiores valores durante os anos de 2024 e 2025?
3.	Quais são os dez Serviços mais vendidos por ano?
4.	Qual foi o mês com maior receita de cada ano?
5.	Qual o lucro mensal da empresa, considerando um gasto fixo de R$ 7.000,00 por mês mais as comissões pagas aos Prestadores?
6.	Qual a forma de pagamento mais utilizada pelos clientes?
7.	Quais o três clientes que mais gastaram dinheiro no salão durante o ano?
8.	Com base nas informações coletadas, quais estratégias podem ser adotadas para aumentar o faturamento do salão?<br><br>

<center><strong>Explicação do arquivos Notebook:</strong></center><br>
Importar_arquivos.ipyn - > Importar os arquivos (.csv) para os dataframes.<br>
<a href="https://github.com/EdnilsonBastos/Projeto-Engenharia-de-Dados/blob/main/Importar_arquivos.ipynb">Notebook Importar Arquivos</a>.<br>
Bronze.ipynb - > Gera as tabelas no database Bronze com seus respectivos dataframes carregados.<br>
<a href="https://github.com/EdnilsonBastos/Projeto-Engenharia-de-Dados/blob/main/Bronze.ipynb ">Notebook Bronze</a>.<br>
QualidadeDados.ipynb - > Desmonstra quais tabelas tivemos problemas na qualidade dos dados.<br>
<a href="https://github.com/EdnilsonBastos/Projeto-Engenharia-de-Dados/blob/main/QualidadeDados.ipynb ">Notebook Qualidade de Dados</a>.<br>
Catalogos.ipynb - > Foi feito os catalogos nas três camadas Bronze, Prata e Ouro.<br>
<a href="https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/88263800885915/3970626668299490/7601240088140268/latest.html">Notebook Catalago de Dados</a>.<br>
Prata.ipynb - > Trata os dataframes retirando colunas em branco, troca o tipo de coluna e altera os dados de uma coluna. Gera o database Prata com os dataframes tratados.<br>
<a href="https://github.com/EdnilsonBastos/Projeto-Engenharia-de-Dados/blob/main/Prata.ipynb ">Notebook Prata</a>.<br>
Ouro.ipynb - > Cria as tabelas no database Ouro e responde as perguntas atráves do comando SQL.<br>
<a href="https://github.com/EdnilsonBastos/Projeto-Engenharia-de-Dados/blob/main/Ouro.ipynb  ">Notebook Ouro</a>.<br>
AutoAvaliacao.ipynb - > Fala sobre a construção do projeto as dificuldades enfrentadas até chegar nas respostas das métricas pedidas. E faz uma explicação do SQL de cada resposta e como chegamos no obetivo.<br>
<a href="https://github.com/EdnilsonBastos/Projeto-Engenharia-de-Dados/blob/main/AutoAvaliacao.ipynb">Notebook da AutoAvaliação</a>.<br><br>

<center><strong>MODELO</strong></center><br><br>
Foi escolhido o  modelo Estrela. Foi criado as tabelas fatos para responder as métricas acima.<br><br>

<IMG SRC='https://github.com/EdnilsonBastos/Projeto-Engenharia-de-Dados/blob/main/modelo.jpg'/><br><br>

<strong>RELACIONAMENTOS DA TABELAS</strong><br><br>

CLIENTES  --> COMANDACLIENTE<br>
ID_CLIENTE da tabela “CLIENTE” com ID_CLIENTE da tabela “COMANDA_CLIENTE”
Incluir TODOS os registros de 'CLIENTES' e somente os registros de 'COMANDACLIENTE' quando os campos unidos forem iguais.<br>
	
PRESTADOR  --> COMANDACLIENTE<br>
ID_PRESTADOR da tabela “PRESTADOR” com ID_PRESTADOR da tabela “COMANDACLIENTE”
Incluir TODOS os registros de 'PRESTADOR' e somente os registros de 'COMANDACLIENTE' quando os campos unidos forem iguais.

SERVICOS  --> COMANDACLIENTE<br>
ID_SERVICO da tabela “SERVICOS” com ID_SERVICO da tabela “COMANDACLIENTE”
Incluir TODOS os registros de 'SERVICOS' e somente os registros de 'COMANDACLIENTE' quando os campos unidos forem iguais.

COMANDA --> COMANDACLIENTE<br>
ID_COMANDA da tabela “COMANDA” com ID_COMANDA da tabela “COMANDACLIENTE”
Incluir TODOS os registros de 'COMANDA' e somente os registros de 'COMANDACLIENTE' quando os campos unidos forem iguais.

PAGAMENTOS --> COMANDA<br>
ID_COMANDA da tabela “PAGAMENTOS” com ID_COMANDA da tabela “COMANDA”
Incluir TODOS os registros de 'COMANDA' e somente os registros de 'PAGAMENTOS' quando os campos unidos forem iguais.<br>








		
	















