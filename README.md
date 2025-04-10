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
Bronze.ipynb - > Gera as tabelas no database Bronze com seus respectivos dataframes carregados.<br>
QualidadeDados.ipyn - > Desmonstra quais tabelas tivemos problemas na qualidade dos dados.<br>
Prata.ipynb - > Trata os dataframes retirando colunas em branco, troca o tipo de coluna e altera os dados de uma coluna. Gera o database Prata com os dataframes tratados.<br>
Ouro.ipynb - > Cria as tabelas no database Ouro e responde as perguntas atráves do comando SQL.<br><br>
AutoAvaliacao.ipynb - > Fala sobre a construção do projeto as dificuldades enfrentadas até chegar nas respostas das métricas pedidas. E faz uma explicação do SQL de cada resposta e como chegamos no obetivo.<br><br>

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
Incluir TODOS os registros de 'COMANDA' e somente os registros de 'PAGAMENTOS' quando os campos unidos forem iguais.

<strong>CATALAGO DE DADOS DA CAMADA BRONZE</strong><br><br>
<table border="1">
  <tr>
    <th colspan="6">TABELA CLIENTES</th>
  </tr>
  <tr>
    <th colspan="6" align="left">ORIGEM: TABELA CLIENTE EXPORTADA DO SISTEMA DESKTOP DO SALÃO PARA O FORMATO (.CSV)</th>
  </tr>
<tr>
    <th colspan="6" align="left">EXEMPLO DO ARQUIVO: (clientes.csv)</th>
  </tr>
  <tr>
    <td><strong>NOME DO CAMPO</strong></td>
    <td><strong>TIPO DO DADO</strong></td>
    <td><strong>TAMANHO</strong></td>
    <td><strong>DESCRIÇÃO</strong></td>
    <td><strong>CHAVE PRIMÁRIA</strong></td>
    <td><strong>ACEITA NULO</strong></td>
  </tr>
    <td>ID_CLIENTE</td>
    <td>INT</td>
    <td align="center">7</td>
    <td>IDENTIFICADOR ÚNICO (IDENTITY)</td>
    <td align="center">S</td>
    <td align="center">N</td>
  </tr>
  <tr>
    <td>NOME</td>
    <td>Varchar</td>
    <td align="center">100</td>
    <td>INFORMA O NOME DO CLIENTE</td>
    <td align="center">N</td>
    <td align="center">N</td>
  </tr>
   <tr>
    <td>DATA_NASCIMENTO</td>
    <td>varchar</td>
    <td align="center">10</td>
    <td>INFORMA A DATA DE NASCIMENTO DO CLIENTE</td>
    <td align="center">N</td>
    <td align="center">S</td>
  </tr>
   <tr>
    <td>TELEFONE</td>
    <td>varchar</td>
    <td align="center">15</td>
    <td>INFORMA O TELEFONE CELULAR DO CLIENTE</td>
    <td align="center">N</td>
    <td align="center">S</td>
  </tr>	
</table><br><br>
		
	



<strong>CATALAGO DA CAMADA PRATA</strong><br> 
*(Coloquei somente as tabelas que teve mudança na sua estrutura em referência a camada “Bronze”)<br><br>


<strong>CATALAGO DA CAMADA OURO</strong><br><br> 




<a href="https://github.com/EdnilsonBastos/Projeto-Engenharia-de-Dados/blob/main/Bronze.ipynb">Notebook Bronze</a>.






