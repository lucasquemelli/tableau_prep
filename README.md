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

