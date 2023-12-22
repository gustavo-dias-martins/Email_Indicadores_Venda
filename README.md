<h1> Automação dos Envios dos Indicadores de Vendas </h1>
<p>A empresa tem mais de 100 lojas abertas em todo estado, e todo o dia o gerente da loja tinha que pegar em diversos dashboards os principais resultados do dia anterior e do mês, tirar print e montar um excel para apresentar para seus colaboradores da loja. Isso acarretava muito tempo, e eu precisava encontrar uma forma de resolver isso.</p> 
<p>O projeto é um código desenvolvido em Python, para resolver esse problema. Nele automatizo o envio desses indicadores e reduzo o tempo que perdemos nesse processo.</p>

<h2> Bibliotecas Utilizadas </h2>
<p>- Numpy</p>
<p>- pyodbc</p>
<p>- smtplib</p>
<p>- datetime</p>
<p>- Pandas</p>
<p>- email.mime.multipart</p>
<p>- email.mime.text</p>
<p>- email.mime.application</p>

<h2> Arquivos Utilizados </h2>

<p>No projeto original, pegamos os dados diretamente do banco de dados da empresa. Para replicar, considerei bases em excel como fonte de dados </p>

<h2> Como funciona? </h2>
<p>Como qualquer problema, não consegui resolver de primeira. Inicialmente ao fazer os tratamentos iniciais via SQL e puxar os dados do nosso banco, levava em torno de 30 minutos. Precisei achar alguma forma de reduzir esse tempo, então a solução encontrada foi fazer um processo prévio no Pentaho, que ocorria durante a noite (momento mais tranquilo para rodar), e incluía essas tabelas já reduzidas, somente com as informações necessárias, em nosso banco de dados. Resultado final: o tempo de carga caiu de 30 para 3 minutos.
Depois com o Python, realizei a automação de todos os cálculos finais, formatação e envio dos email individualmente para cada gerente de loja e seus supervisores. O processo final não dura nem 5 minutos, e quando o gerente abre a loja, já tem todas as informações prontas para a apresentação e orientações iniciais. </p>
<p> Exemplos de indicadores finais:</p>
<p>- Tempo Médio de Atendimento</p>
<p>- Venda do dia anterior e do mês acumulada com seus desvios</p>
<p>- Resultado dos funcionários</p>
<p>- Aniversariante do dia</p>
