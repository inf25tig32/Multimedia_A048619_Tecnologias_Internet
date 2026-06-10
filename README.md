# Relatório do Projeto: ValerPhotos - Portefólio Multimédia

## 1. Project Presentation – Apresentação do projeto
O projeto **FilmbyMia** consiste no desenvolvimento de um website estático focado na área temática de "Multimédia", especificamente um portfólio para fotografia de casamentos e *sessões em casal* com uma estética cinemática, nostálgica e analógica.

**Proposta de Trabalho:**
O objetivo principal foi criar uma experiência web de 4 páginas estruturadas com HTML5 semântico, estilizadas com CSS3 e com interatividade garantida através de JavaScript no lado do cliente. O projeto visa demonstrar a aplicação prática de marcação semântica, leitura assíncrona de ficheiros XML (validados por XSD) e validação estrita segundo as normas do W3C.

---

## 2. User Interface – Interface com o utilizador

### Sitemap (Mapa do Site)
A navegação do site está dividida em 4 páginas principais, acessíveis através de um menu *overlay* de ecrã inteiro:
1. **Homepage (`index.html`):** Introdução, Hero Image, Área de Cliente (Login simulado) e destaques.
2. **Behind the Lens (`sobre.html`):** História da fotógrafa, vídeo de bastidores e lista de equipamentos.
3. **Investment (`servicos.html`):** Tabela de preços dinâmicos carregados via XML e opção de download de dados.
4. **Inquire (`contactos.html`):** Formulário completo para marcações e detalhes de contacto.

### Resultado Final vs Estudo Inicial
O resultado final manteve-se altamente fiel ao planeamento inicial. A paleta de cores foca-se em tons quentes (bege `#eaddcb` e vermelho bordeaux `#7a1f1e`), e o uso de tipografia com serif garante o aspeto clássico de "revista de moda".



## 3. Product - Produto

### Descrição do Produto
A FimbyMia é uma plataforma web estática de apresentação de serviços fotográficos. Destaca-se por uma interface minimalista e interativa, possuindo um carregamento dinâmico de pacotes de preços através de XML e uma "Área de Cliente" simulada para visualização de galerias privadas.

### Ligação para o site no Netlify
🌐 **https://inf25tig32.netlify.app/**


### Regras de Utilização
* **Acesso Público:** A navegação, preçário e formulário de contacto estão abertos a todos os utilizadores.
* **Autenticação Simulada:** Na Homepage, existe uma área de cliente. É possível testar o acesso com as seguintes credenciais:
  * **Username:** `ruben` | **Password:** `ruben123`
  * Este login consulta um ficheiro `clientes.xml` usando JavaScript para demonstrar a manipulação do DOM e exibição de galerias ocultas.

### Ajuda à Navegação
* **Menu Overlay Interativo:** A navegação principal está oculta atrás do botão oval "View The Menu". Ao clicar, um ecrã sobreposto aparece de forma animada (usando CSS transition e `transform`), focando a atenção do utilizador apenas nas opções de navegação.
* **Links Ativos/Hover:** Todos os botões e links possuem efeitos de `:hover` com transição suave de cores e alteração de formato do cursor (`cursor: pointer`).

### Validações de Formulários
A página `contactos.html` utiliza os mecanismos nativos do HTML5 para validação no lado do cliente:
* Atributo `required` para impedir submissões vazias em campos essenciais (Nome, Email, Mensagem).
* Atributo `type="email"` garante que o utilizador insere um formato de correio eletrónico válido.
* Atributo `type="date"` disponibiliza um calendário nativo (Datepicker) para evitar erros de formatação de datas.

### Validação do HTML e CSS
Todo o código fonte foi testado recorrendo aos validadores oficiais do W3C.
* **Validador HTML:** https://validator.w3.org/
* **Validador CSS:** https://jigsaw.w3.org/css-validator/


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
    * Leitura assíncrona (`XMLHttpRequest`) do `pacotes.xml` transformando dados em linhas para a Tabela HTML.
    * Sistema de Login simulado usando JavaScript para manipular o DOM (esconder/mostrar div da galeria e alterar texto).
