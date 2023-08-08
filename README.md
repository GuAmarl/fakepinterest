# Recriação do site Pinterest - Python Impressionador

## Sobre

Recriação do site Pinterest e algumas de suas funções, utilizando o framework do Python, Flask, e um pouco de CSS e HTML.
Nesse projeto, cria-se um conta, que fica armazenada em um banco de dados, e ao fazer login, possui um perfil no site, sendo possível fazer upload de fotos para a plataforma, que ficam visíveis em um feed de imagens de todos os perfis criados. Dessa forma, ao clicar em uma imagem, é possível visitar o perfil de quem fez o upload.

## Organização dos arquivos e observações

O projeto é organizado de forma a facilitar a integração com o Flask, portanto, é criado uma pasta do projeto, onde seu "__init__" é responsável por conter todas as configurações necessárias e criação do app. Dentro dessa pasta também temos algumas outras pastas e arquivos.

- A pasta "static" contém as imagens que foram utilizadas de exemplo na criação e teste do site, bem como a imagem de fundo do site, e o arquivo de estilização CSS.

- A pasta de templates contém os templates em HTML renderizados por cada rota. É importante ressaltar que para esse projeto o template "homepage.html" foi utilizado como base para todos os outros, ou seja, somente ele tem a estrutura completa de HTML, e os demais são uma extensão dele, com a excessão do "navbar.html" que contém somente a estrutura da barra de navegação, incluida em alguns templates.

- O arquivo de forms contém todos os formulários utilizados nos templates, em que, utilizando as bibliotecas "wtforms" e "flask_wtf" facilitaram sua criação, validação dos campos, emissão de erros e integração com o framework Flask.

- O arquivo "models.py" contém as classes responsáveis pela criação das tabelas do banco de dados. Dessa forma, utiliza-se de um banco de dados PostgreSQL, cujas tabelas foram criadas a partir do arquivo "criar_banco.py" e com a ajuda da biblioteca SQLALCHEMY.

- O arquivo "routes.py" contém todas as rotas do site, bem como, algumas validações e outras funções em python necessárias para que cada rota funcione como deveria.

- Por fim, o arquivo "main.py" somente importa o app criado e efetivamente o executa.