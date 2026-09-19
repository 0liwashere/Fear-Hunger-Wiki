# Fear & Hunger Wiki

Site informativo (fã-wiki) sobre a série de RPGs de horror Fear & Hunger, desenvolvido como projeto acadêmico. O site reúne informações sobre a história do jogo, personagens e os mapas/áreas da masmorra, com navegação responsiva entre as páginas.

![Preview do projeto](imagens/home.jpg)
<!-- Substitua pelo caminho real do print da Home -->

## Funcionalidades

- Navegação entre páginas temáticas: Início, Personagens, História e Mapas
- Menu responsivo com animação, adaptado para dispositivos móveis
- Conteúdo estruturado com tabelas (temas, facções) e mídia incorporada (imagens, vídeo do YouTube)
- Aviso de conteúdo sensível (classificação etária) na página inicial
- Seções de mapas com descrição individual de cada área da masmorra

## Tecnologias

- **HTML5** — estruturação semântica do conteúdo
- **CSS3** — estilização visual e responsividade (`style.css`)
- **JavaScript** — lógica do menu mobile (`mobile-navbar.js`)

## Como rodar

Por ser um site estático, não é necessário nenhum servidor ou instalação:

1. Baixe ou clone o repositório.
2. Abra o arquivo `index.html` diretamente no navegador.

*(Opcional: usar a extensão "Live Server" do VS Code para recarregamento automático durante edições.)*

## Arquitetura

O projeto segue uma estrutura simples de site multi-página estático:

- **Páginas** (`index.html`, `personagens.html`, `historia.html`, `mapas.html`) — cada uma representa uma seção da wiki, compartilhando o mesmo cabeçalho de navegação e rodapé.
- **`style.css`** — estilos globais compartilhados entre todas as páginas: navbar, menu mobile, rodapé e responsividade.
- **`mobile-navbar.js`** — classe `MobileNavbar`, responsável por controlar a abertura/fechamento do menu em telas pequenas e animar a entrada dos links.
- Cada página também contém estilos específicos inline (`<style>` no `<head>`), usados para o plano de fundo e o layout do conteúdo daquela seção em particular.

## Decisões técnicas

- **Menu mobile reutilizável:** a classe `MobileNavbar` foi construída de forma genérica (recebendo seletores como parâmetro), permitindo reaproveitar a mesma lógica em todas as páginas sem duplicar código JS.
- **Aviso de conteúdo:** a Home inclui um aviso de classificação etária, já que o jogo retratado possui temática adulta e violenta.
- **Avisos de conteúdo incompleto:** as páginas de História e Mapas incluem um alerta visual (via SVG) informando que o conteúdo do segundo jogo da franquia ("Termina") ainda não foi adicionado à wiki.
- **Estilização repetida por página:** por ainda não ter um sistema de componentes, cada página repete parte do CSS de layout (como `.box-model3`) — um ponto de melhoria futura seria centralizar essas classes no `style.css` global.

## ✅ Status

Páginas de Início, História e Mapas implementadas e funcionais. A página de Personagens também está disponível no projeto.
