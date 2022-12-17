# Tableau Prep

This is a repository where I publish my studies with Tableau Prep

# União de duas tabelas

1. Clicamos no símbolo de + e em seguida em Etapa de Limpeza. Assim, conseguimos ter uma visão dos dados de cada tabela:

<img width="401" alt="image" src="https://user-images.githubusercontent.com/81119854/208109135-dd484925-9395-4664-a0ff-f3216137c03a.png">

<img width="1309" alt="image" src="https://user-images.githubusercontent.com/81119854/208109307-fd128e2c-f33f-42ef-84b1-799a6344b2e0.png">

<img width="1309" alt="image" src="https://user-images.githubusercontent.com/81119854/208109404-93dc6dcb-103f-41af-bfbf-61026ee83181.png">

- Note que assim conseguimos identificar que a cidade Rio de Janeiro deve ter seu nome padronizado em etapas futuras. Além disso, conseguimos observar que só existem pessoas do gênero masculino como clientes nessa cidade. 

2. Agora vamos alterar o campo CPF de numérico para cadeia de caractes. Para tanto, basta clicar no símbolo # e selecionar "cadeia de caracteres".

<img width="260" alt="image" src="https://user-images.githubusercontent.com/81119854/208109927-df294d3c-9689-49a8-880d-d9036c75d601.png">

3. O Tableau tem recomendações automáticas. Nesse caso, ele sugere alterar os campos cidade e estado para o tipo geográfico. Para o Rio de Janeiro, ainda só vamos acatar a recomendação de estado, porque ainda precisamos padronizar a escrita da cidade. 

<img width="1456" alt="image" src="https://user-images.githubusercontent.com/81119854/208111270-2b07f733-909e-4a86-abfb-1b4fd4c1d226.png">

- Nem sempre as recomendações do Tableau são aplicáveis. É importante analisar antes de acatá-las. 

4. Vamos passar o campo gênero de M e F para masculino e feminino. 

- Clicar no campo desejado e em seguida em criar campo calculado. 

<img width="1306" alt="image" src="https://user-images.githubusercontent.com/81119854/208115568-acf1a7cd-2e60-4efb-8e51-9a66b3941a87.png">

<img width="846" alt="image" src="https://user-images.githubusercontent.com/81119854/208115235-70f4aeb1-1416-4df1-926b-87c6c130aac6.png">

5. Corrigindo a cidade do Rio de Janeiro para uma única string e acatando a recomendação do Tableau para mudar cidade para campo geográfico.

<img width="846" alt="image" src="https://user-images.githubusercontent.com/81119854/208117495-1a507739-6874-4702-90eb-a5807a8de6bf.png">

<img width="434" alt="image" src="https://user-images.githubusercontent.com/81119854/208117653-19717586-db0a-46f8-bebd-b415e6ee7a5c.png">

6. Aplicando UNIÃO das tabelas. Basta arrastar um dos fluxos limpos para cima do outro fluxo limpo. Assim, teremos as opções: união de linhas e união de colunas. Nesse caso, escolhemos a união de linhas.

<img width="970" alt="image" src="https://user-images.githubusercontent.com/81119854/208121704-a5f01cab-3b64-4465-9553-99476b5120df.png">

- Ao fazer a união, nós temos alguns campos não correspondentes. Esses são campos que existem em uma tabela mas não existem na outra. 

- Para corrigir, primeiro vamos na tabela limpa do Rio de Janeiro e vamos excluir o campo cidade. 

<img width="427" alt="image" src="https://user-images.githubusercontent.com/81119854/208122061-66775658-dfd9-4e66-9805-e4761fd5a212.png">

- Agora vamos para a tabela união e clicamos sobre a caixa "mostrar apenas campos não correspondentes". 

<img width="858" alt="image" src="https://user-images.githubusercontent.com/81119854/208122380-8e4edea1-0aca-451f-b9f1-06f02c117174.png">

- Para tanto, basta arrastar o campo CIDADE_CORRIGIDA sobre o campo CIDADE. Assim, vai aparecer a mensagem "solte para mesclar os campos". Depois fazemos o mesmo para a coluna SEXO.

# Separando tabelas

1. Primeiro criamos mais um fluxograma de etapa de limpeza.

2. Segundo, removemos a coluna Table Names:

<img width="426" alt="image" src="https://user-images.githubusercontent.com/81119854/208162339-d3668f78-4343-49c8-88ee-76cf8418363d.png">

3. Terceiro, removemos a coluna SEXO:

<img width="250" alt="image" src="https://user-images.githubusercontent.com/81119854/208162660-03d1b191-7ae2-442e-bbd0-d143f40850a8.png">

4. Renomeamos a coluna GENERO_NOME apenas para GENERO:

<img width="428" alt="image" src="https://user-images.githubusercontent.com/81119854/208163569-efcafae7-6374-42c1-9a13-82e98560a755.png">

5. Agora criamos mais um fluxograma de limpeza para preparar os dados para a Tabela Cidades, onde vamos manter apenas a cidade e o estado:

<img width="859" alt="image" src="https://user-images.githubusercontent.com/81119854/208164935-e4390a26-8263-4c45-b367-3c74ce0efd37.png">

6. Agora vamos criar mais uma etapa para agregar a tabela de cidades:

<img width="346" alt="image" src="https://user-images.githubusercontent.com/81119854/208165550-db3dbaed-50c2-4e42-b05f-cb0c33784429.png">

- Para agregar, basta arrastar os campos cidade e estado para a região de campos agrupados:

<img width="1140" alt="image" src="https://user-images.githubusercontent.com/81119854/208165931-8cad3ce5-ba53-4c2b-b18e-dbc704e296a2.png">

<img width="1585" alt="image" src="https://user-images.githubusercontent.com/81119854/208166032-07816f03-a14d-4feb-87cc-ff2822c7e675.png">

7. De forma similar, criamos um fluxograma para agrupar apenas os estados:

<img width="1113" alt="image" src="https://user-images.githubusercontent.com/81119854/208167274-f8baa797-5185-4f64-ad57-856f3ab68d0a.png">

8. Agora criamos uma tabela apenas para clientes, sem os estados:

<img width="1057" alt="image" src="https://user-images.githubusercontent.com/81119854/208168528-f363c8a3-01e2-409d-9afb-3b49a1e98694.png">

# Tratamento da tabela de produtos

- Vamos separar o campo NOME_PRODUTO em marca, tamanho e sabor. 

<img width="781" alt="image" src="https://user-images.githubusercontent.com/81119854/208174747-42b0fd90-5304-494b-9f1f-52907e9e205a.png">

<img width="848" alt="image" src="https://user-images.githubusercontent.com/81119854/208175778-c68a8b4a-5087-4be3-8cba-7e9e7f08a25c.png">

<img width="847" alt="image" src="https://user-images.githubusercontent.com/81119854/208175836-b13b81ae-43d8-4a85-adb6-a83426309f3e.png">

<img width="844" alt="image" src="https://user-images.githubusercontent.com/81119854/208175899-7614b338-9908-401d-be3a-f6bbf4698764.png">

# Filtrando dados

- Vamos retirar os registros em que o tamanho é igual a 1 L. Pelas estatísticas, nós temos 5 registros iguais a 1 L.

<img width="1595" alt="image" src="https://user-images.githubusercontent.com/81119854/208194986-1e175d38-7a08-4b16-8383-23b3aba9e9ae.png">

- Para retirar o valor de 1 L, basta clicar sobre esse valor na coluna TAMANHO e excluir:

<img width="1157" alt="image" src="https://user-images.githubusercontent.com/81119854/208196218-b023e323-c4f6-434a-92e4-21f6dc701825.png">

# Inserir fluxo

- Vamos inserir o fluxo de produtos e o fluxo de clientes no fluxo de itens, notas e vendedores. Com o botão direito do mouse: inserir fluxo.

<img width="1578" alt="image" src="https://user-images.githubusercontent.com/81119854/208197011-bd532fa2-6627-4b1d-a35c-03c30928db78.png">

- Resultado:

<img width="1182" alt="image" src="https://user-images.githubusercontent.com/81119854/208197260-faf4d5f5-1a2e-4b2a-a67f-60fa0236e584.png">

# Junção de dados

- Para fazer a junção, basta arrastar o fluxo de itens para o fluxo de notas e selecionar união de colunas. 

<img width="467" alt="image" src="https://user-images.githubusercontent.com/81119854/208198894-4c134808-3f74-4f43-ade8-80d939c775ca.png">

- A gente pode escolher o tipo de JOIN simplesmente clicando sobre o diagrama abaixo abaixo e selecionando o JOIN que desejamos. Nesse caso foi INNER JOIN.

<img width="326" alt="image" src="https://user-images.githubusercontent.com/81119854/208199511-6bc3ebcc-f7a2-45de-b55c-8e9bb354f101.png">

# Limpeza da tabela Notas e Itens

1. Remover colunas duplicadas.

<img width="588" alt="image" src="https://user-images.githubusercontent.com/81119854/208201485-58cd2257-a62a-4fc3-95a0-424259dcc1e9.png">

2. Transformação da data para mês e ano. 

- Primeiro, transformamos o campo de data para cadeia de caracteres.

<img width="228" alt="image" src="https://user-images.githubusercontent.com/81119854/208201785-6760c753-d190-4df8-9bcd-dc152ba24cdd.png">

- Agora, basta criarmos um campo calculado para pegarmos o mês e o ano. Usamos a função MID, para retornar os 7 caracteres a partir do primeiro. 

<img width="918" alt="image" src="https://user-images.githubusercontent.com/81119854/208201998-23f2f509-2e4c-4b86-9641-dd51ed276436.png">

<img width="837" alt="image" src="https://user-images.githubusercontent.com/81119854/208202326-89b4b2e0-3a02-4934-b615-cf8def357af5.png">

- Como é uma string, podemos concatenar e depois transformar para data novamente:

<img width="844" alt="image" src="https://user-images.githubusercontent.com/81119854/208202668-ac5e84cc-db9d-4b5d-a060-4203392bdbaf.png">

# Agrupamento de preços 

- Nós precisamos fazer agrupamento agora que mudamos a data. Existem muitas informações repetidas e agora precisamos agrupar pelo mês, não mais pelo dia. 

- Nós não podemos fazer o agrupamento de preços porque a variável preço é por quantidade de produto. Assim, primeiro vamos calcular o agrupamento da quantidade e do faturamento (preço * quantidade), depois calcular o preço por quantidade agrupada. 

<img width="1128" alt="image" src="https://user-images.githubusercontent.com/81119854/208203668-a7b887a6-bf04-486d-a435-d99d0237203d.png">

1. FATURAMENTO:

<img width="842" alt="image" src="https://user-images.githubusercontent.com/81119854/208203863-fbc74953-bd5a-4f23-9690-9147731fcc95.png">

2. Removemos a coluna de preço.

<img width="275" alt="image" src="https://user-images.githubusercontent.com/81119854/208203949-18a21fd4-1248-4408-9765-5589a97bb4a2.png">

3. Criamos um fluxograma de agregação e arrastamos para "Campos agrupados" as dimensões e "Campos agregados" as métricas (quantidade, faturamento e o número de linhas) 

<img width="1579" alt="image" src="https://user-images.githubusercontent.com/81119854/208204322-55a5ea38-55b6-4423-8028-b267c8cd7605.png">

<img width="1585" alt="image" src="https://user-images.githubusercontent.com/81119854/208204416-06ef3d8f-17a6-47eb-ade8-aff2cbb35e6c.png">

4. Agora podemos criar uma variável preço já com valores agrupados. Basta dividir o faturamento agrupado pela quantidade agrupada.

- Fazemos isso em um novo fluxograma de limpeza.

- Criamos um campo calculado com o cálculo que desejamos.

<img width="1094" alt="image" src="https://user-images.githubusercontent.com/81119854/208204886-f4e3f44a-6efb-4671-816b-4a32f2cd6797.png">

# Integridade da tabela Notas e Itens

1. Vamos fazer a união, por colunas, da tabela de vendedores com a tabela de notas e itens (tabela fato).

<img width="1174" alt="image" src="https://user-images.githubusercontent.com/81119854/208243780-82b37e6c-f968-4224-be21-f77a33daf2b0.png">

2. Criamos uma etapa de limpeza para remover os campos a mais quando fizemos a união.

<img width="776" alt="image" src="https://user-images.githubusercontent.com/81119854/208244136-1d8c26b9-d0db-4a9a-83f4-a27b171b720b.png">

<img width="393" alt="image" src="https://user-images.githubusercontent.com/81119854/208244179-88bf3ab3-7b7d-4bbf-a6e2-2aa7591dbf57.png">

3. Agora vamos fazer uma união de colunas da tabela de produtos com a tabela fato.

<img width="1575" alt="image" src="https://user-images.githubusercontent.com/81119854/208244350-e03be604-e41a-435c-88d2-ac3fdd14238d.png">

4. Vamos fazer mais uma limpeza de campos. Agora da tabela resultante acima. Revemos: marca, tamanho, sabor, codigo_produto-1 e nome_produto.

<img width="1575" alt="image" src="https://user-images.githubusercontent.com/81119854/208244806-85a3758a-e91e-41f1-aa25-1b992d8246b1.png">

<img width="314" alt="image" src="https://user-images.githubusercontent.com/81119854/208244912-ec298f36-4e5d-4f0e-b38d-c28d68ee3ed8.png">
