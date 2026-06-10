# Relatório do Projeto: ValerPhotos - Portefólio Multimédia

## 1. Project Presentation – Apresentação do projeto
O projeto **ValerPhotos** consiste no desenvolvimento de um website estático focado na área temática de "Multimédia", especificamente um portefólio premium para fotografia de casamentos e *elopements* com uma estética cinemática, nostálgica e analógica.

**Proposta de Trabalho:**
O objetivo principal foi criar uma experiência web imersiva de 4 páginas estruturadas com HTML5 semântico, estilizadas com CSS3 avançado (Mobile First) e com interatividade garantida através de JavaScript no lado do cliente. O projeto visa demonstrar a aplicação prática de marcação semântica, manipulação do Box Model, *media queries* para responsividade, leitura assíncrona de ficheiros XML (validados por XSD) e validação estrita segundo as normas do W3C.

---

## 2. User Interface – Interface com o utilizador

### Sitemap (Mapa do Site)
A navegação do site está dividida em 4 páginas principais, acessíveis através de um menu *overlay* de ecrã inteiro:
1. **Homepage (`index.html`):** Introdução, Hero Image, Área de Cliente (Login simulado) e destaques.
2. **Behind the Lens (`sobre.html`):** História da fotógrafa, vídeo de bastidores e lista de equipamento.
3. **Investment (`servicos.html`):** Tabela de preços dinâmicos carregados via XML e opção de download de dados.
4. **Inquire (`contactos.html`):** Formulário completo para marcações e detalhes de contacto.

### Estudo da Interface (Wireframes)
*(Insere aqui as imagens dos teus rascunhos em papel ou wireframes feitos no Figma/Balsamiq)*
![Wireframe Homepage](link_para_a_tua_imagem_wireframe.png)

### Resultado Final vs Estudo Inicial
O resultado final manteve-se altamente fiel ao planeamento inicial. A paleta de cores foca-se em tons quentes (bege `#eaddcb` e vermelho bordeaux `#7a1f1e`), e o uso de tipografia com serifa garante o aspeto clássico de "revista de moda". A maior evolução deu-se na implementação do menu *fullscreen* através do CSS *Checkbox Hack*, que substituiu a necessidade de um menu clássico e desorganizado em ecrãs móveis.

*(Insere aqui 2 ou 3 capturas de ecrã do site final)*
![Screenshot Homepage Final](link_para_a_tua_imagem_final1.png)
![Screenshot Menu Final](link_para_a_tua_imagem_final2.png)

---

## 3. Product - Produto

### Descrição do Produto
A ValerPhotos é uma plataforma web estática de apresentação de serviços fotográficos. Destaca-se por uma interface minimalista e interativa, possuindo um carregamento dinâmico de pacotes de preços através de XML e uma "Área de Cliente" simulada para visualização de galerias privadas.

### Ligação para o site no Netlify
🌐 **[Inserir aqui o teu link, ex: https://valerphotos-projeto.netlify.app]**

### Instruções de Instalação e Configuração
**Instalação Local:**
1. Fazer o clone do repositório: `git clone https://github.com/exemploTrabalho/report_inf-ti.git`
2. Navegar até à pasta do projeto e abrir o ficheiro `index.html` em qualquer navegador web moderno (recomenda-se Google Chrome ou Firefox). *Nota: Para o carregamento do XML funcionar localmente em alguns navegadores (devido à política CORS), pode ser necessário abrir o projeto via Live Server no VS Code.*

**Instalação no Netlify (Automática):**
1. Aceder a netlify.com e fazer login via GitHub.
2. Clicar em "Add new site" -> "Import an existing project".
3. Selecionar o repositório deste projeto no GitHub.
4. Deixar as definições de *Build command* e *Publish directory* em branco (pois é um site estático) e clicar em "Deploy Site".

### Regras de Utilização
* **Acesso Público:** A navegação, preçário e formulário de contacto estão abertos a todos os utilizadores.
* **Autenticação Simulada:** Na Homepage, existe uma área de cliente. É possível testar o acesso com as seguintes credenciais:
  * **Username:** `cesar` | **Password:** `fabamaq123`
  * Este login consulta um ficheiro `clientes.xml` usando JavaScript (sem servidor) para demonstrar a manipulação do DOM e exibição de galerias ocultas.

### Ajuda à Navegação
* **Menu Overlay Interativo:** A navegação principal está oculta atrás do botão oval "View The Menu". Ao clicar, um ecrã sobreposto aparece de forma animada (usando CSS transition e `transform`), focando a atenção do utilizador apenas nas opções de navegação.
* **Links Ativos/Hover:** Todos os botões e links possuem efeitos de `:hover` com transição suave de cores e alteração de formato do cursor (`cursor: pointer`).

### Validações de Formulários
A página `contactos.html` utiliza os mecanismos nativos do HTML5 para validação no lado do cliente:
* Atributo `required` para impedir submissões vazias em campos essenciais (Nome, Email, Mensagem).
* Atributo `type="email"` garante que o utilizador insere um formato de correio eletrónico válido.
* Atributo `type="date"` disponibiliza um calendário nativo (Datepicker) para evitar erros de formatação de datas.

### Validação do HTML e CSS
Todo o código fonte foi testado recorrendo aos validadores oficiais do W3C. Não foram encontrados erros de sintaxe ou estrutura no HTML e o CSS passou na totalidade no validador de CSS nível 3.
* **Validador HTML:** https://validator.w3.org/
* **Validador CSS:** https://jigsaw.w3.org/css-validator/

*(Insere aqui as capturas de ecrã das faixas verdes do W3C que geraste anteriormente)*
![Validação HTML](link_para_print_w3c_html.png)
![Validação CSS](link_para_print_w3c_css.png)

### Detalhes de Implementação (Cumprimento dos Requisitos Mínimos)
O projeto cumpriu e ultrapassou os requisitos exigidos:
1. **Páginas e Estrutura:** 4 páginas estáticas focadas em Multimédia utilizando tags semânticas HTML5 (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<figure>`, `<footer>`).
2. **Dados XML/XSD:** Criação de `pacotes.xml` e validação pelo seu `pacotes.xsd`. O ficheiro pode ser descarregado na página `servicos.html`.
3. **Tabelas Complexas:** Utilização de `thead`, `tbody`, `tfoot`, `colspan` e `rowspan` na página de serviços.
4. **Listas Aninhadas:** Criação de uma `<ol>` contendo uma `<ul>` no equipamento fotográfico (`sobre.html`).
5. **Marcações de Texto:** Uso intensivo de `<strong>`, `<em>` e `<mark>` (com formatação CSS alterada).
6. **Formulário Complexo:** Uso de `<fieldset>`, `<legend>`, botões `<radio>` e `<select>`.
7. **Integração CSS3:** Uso de *Media Queries* (Mobile First), formatações avançadas de listas, pseudo-classes (`:hover`, `:checked`), seletor combinador (`~`) no menu overlay, flutuação e posicionamento combinados (`float` + `position: relative` no `<aside>`) e imagens de fundo para caixas HTML.
8. **Valorização Extra (JavaScript e Multimédia):**
    * Uso da tag `<video>` (`sobre.html`).
    * Leitura assíncrona (`XMLHttpRequest`) do `pacotes.xml` transformando dados em linhas para a Tabela HTML.
    * Sistema de Login simulado usando JavaScript para manipular o DOM (esconder/mostrar div da galeria e alterar texto).

---

## 4. Presentation – Apresentação
🔗 **[Insere aqui o link para o teu PowerPoint, Vídeo no Youtube, Canva ou ficheiro PDF da apresentação do projeto]**
