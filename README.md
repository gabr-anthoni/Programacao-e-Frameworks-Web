
__📌 O que é o protocolo HTTP?__

- __🌐 HTTP (_HyperText Transfer Protocol_)__ é o protocolo usado na __World Wide Web (_WWW_)__ para a __distribuição e recuperação de informações.__

- 🧭 Toda vez que você acessa um site no navegador (como Chrome, Firefox ou Safari), está usando o __HTTP__ para se __comunicar com servidores web__ e __receber dados__, como páginas HTML, imagens, vídeos, etc.

- 💬 A troca de informações entre o __navegador (_cliente_)__ e o servidor web é feita totalmente por esse protocolo — ele foi criado __especificamente para a web!__

- 📜 A versão mais utilizada atualmente é a __HTTP/1.1__, que está definida pela especificação __RFC 2616.__

- 🧑‍💻 Os clientes de uma conexão HTTP geralmente são os __navegadores (_browsers_)__ — são eles que fazem as __requisições ao servidor__ para acessar páginas e conteúdos da web.

  🌐 Principais browsers utilizados atualmente:
  - <img width="15" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/chrome/chrome-original.svg" /> Google Chrome
  - <img width="15" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/firefox/firefox-original.svg" /> Firefox
  - <img width="15" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/ie10/ie10-original.svg" /> Microsoft Edge
  - <img width="15" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/opera/opera-original.svg" /> Opera
  - <img width="15" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/safari/safari-original.svg" /> Safari

<hr>

<h3 align="center">🌐 Comunicação entre Cliente e Servidor</h3>

<p align="center">
  <img width="500" src="./.imgs/HTTP.png">
</p>

1. __🧑‍💻 Cliente faz a requisição__<br>
   O __cliente (_normalmente um navegador, app ou outro software_)__ solicita um recurso (_como uma página HTML, imagem, vídeo, etc._) __enviando uma requisição HTTP para o servidor.__

   __📌 A requisição contém:__
   - __Método HTTP__
   - __URI__ (_identificador do recurso solicitado_)
   - __Cabeçalhos__ (_Headers_) com informações como idioma, tipo de conteúdo aceito, autenticação, etc.

> [!NOTE]
> __📌 Nota: URI__ significa _Uniform Resource Identifier_ — ou seja, _Identificador Uniforme de Recursos._<br>
> É uma __string__ (_sequência de caracteres_) que __identifica um <ins>recurso</ins>__ na internet ou em qualquer __sistema de informação.__<br><br>
> __Um <ins>recurso</ins> pode ser uma:__
> - Uma página da web
> - Um arquivo de imagem
> - Um vídeo e etc...
>
> __URL__ é um __tipo específico de URI__ que localiza o recurso, ou seja, diz onde ele está e como acessá-lo.

2. __🖥️ Servidor recebe e processa__<br>
   O servidor web recebe a __requisição, interpreta os dados, e:__
   - __Encontra o recurso solicitado__ (_ou gera dinamicamente, como em sites que usam banco de dados_)
   - Processa __lógica de negócio, autenticação, etc.__
   - Prepara uma __resposta HTTP__

3. __📦 Servidor envia a resposta__<br>
   A resposta __HTTP__ do servidor é enviada de volta ao __cliente.__
   
   __📌 A resposta contém:__
   - __Código de status__ ( _indicando sucesso ou falha do pedido._ )
   - __Cabeçalhos__ (_Headers_) com informações sobre o __conteúdo__ (_tipo, tamanho, cache, cookies, etc._)
   - __Corpo da resposta__ (_com o conteúdo solicitado: HTML, JSON, imagem, vídeo, etc._)

4. __🔍 Cliente interpreta a resposta__<br>
   O __navegador__ ou __app__ interpreta o conteúdo e o exibe ao usuário:
   - Se for uma página __HTML__, renderiza no __navegador.__
   - Se for um __JSON__, pode ser tratado por um __aplicativo frontend (_como React ou Angular_).__
   - Se for um __arquivo__, pode ser __baixado ou aberto diretamente.__

> [!NOTE]
> __📌 Nota:__ 🖥️ Quem são os Servidores?<br>
> Um servidor web é um computador que tem __software__ e __hardware__ em que vai permitir que os usuários solicitem páginas web.

<hr>

<h3 align="center">✉️ Métodos de requisição HTTP</h3>

Os métodos de requisição __HTTP__ são comandos usados para indicar qual ação deve ser realizada em um recurso (_como um dado, uma página ou um arquivo_) em uma aplicação __web__ ou __API.__

<table align="center">
  <thead>
    <tr>
      <th>Método</th>
      <th>Função</th>
      <th>Exemplo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>GET</code></td>
      <td><strong>Solicitar</strong> dados</td>
      <td>"Me mostra essa receita"</td>
    </tr>
    <tr>
      <td><code>HEAD</code></td>
      <td><strong>Verificar</strong> dados</td>
      <td>"Esse arquivo tá aí? Qual o tamanho?"</td>
    </tr>
    <tr>
      <td><code>POST</code></td>
      <td><strong>Criar</strong> algo novo</td>
      <td>"Aqui está uma nova receita"</td>
    </tr>
    <tr>
      <td><code>PUT</code></td>
      <td><strong>Substituir</strong> algo</td>
      <td>"Atualiza toda essa receita"</td>
    </tr>
    <tr>
      <td><code>DELETE</code></td>
      <td><strong>Remover</strong> algo</td>
      <td>"Apaga essa receita"</td>
    </tr>
    <tr>
      <td><code>PATCH</code></td>
      <td><strong>Editar parcialmente</strong></td>
      <td>"Muda só o nome da receita"</td>
    </tr>
  </tbody>
</table>

O tipo de __URI__ utilizada pelo protocolo __HTTP__ é chamada de __URL__ (_Uniform Resourde Locator_) e contém três partes:

📦 Estrutura básica de uma URL:
```txt
protocolo://host/caminho
```

1. `Protocolo`: Indica qual protocolo usar para acessar o recurso (_ex: http, https_).
2. `Host`: O domínio ou endereço do servidor onde o recurso está hospedado (_ex: `www.exemplo.com`_).
3. `Caminho` (_Path_): Localização do recurso dentro do servidor (_ex: /pagina/index.html_).

<h3 align="center">📩 Códigos de status</h3>

A __resposta do servidor__ com o conteúdo solicitado e um __código de status__ que explica o que aconteceu.

<table align="center">
  <tr>
    <th>Código</th>
    <th>Significado</th>
    <th>Descrição resumida</th>
  </tr>
  <tr>
    <td><strong>200</strong></td>
    <td>OK</td>
    <td>Requisição bem-sucedida, resposta com o recurso.</td>
  </tr>
  <tr>
    <td><strong>201</strong></td>
    <td>Recurso criado</td>
    <td>Recurso criado com sucesso após a requisição.</td>
  </tr>
  <tr>
    <td><strong>204</strong></td>
    <td>Resposta vazia</td>
    <td>Requisição bem-sucedida, mas sem conteúdo para retornar.</td>
  </tr>
  <tr>
    <td><strong>400</strong></td>
    <td>Erro no pedido</td>
    <td>Pedido mal formatado, erro do cliente.</td>
  </tr>
  <tr>
    <td><strong>401</strong></td>
    <td>Falta autenticação</td>
    <td>Não autorizado, falta de autenticação válida.</td>
  </tr>
  <tr>
    <td><strong>403</strong></td>
    <td>Acesso negado</td>
    <td>Acesso negado, mesmo com autenticação.</td>
  </tr>
  <tr>
    <td><strong>404</strong></td>
    <td>Página não achada</td>
    <td>Recurso solicitado não encontrado no servidor.</td>
  </tr>
  <tr>
    <td><strong>422</strong></td>
    <td>Erro de validação nos dados enviados</td>
    <td>Requisição bem formada, mas com erros de validação.</td>
  </tr>
  <tr>
    <td><strong>500</strong></td>
    <td>Erro Interno do Servidor</td>
    <td>Erro interno no servidor, algo deu errado lá.</td>
  </tr>
</table>



