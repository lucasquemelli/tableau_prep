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

