# Rede Semente — plataforma para uma organização social

## Sobre o site

A Rede Semente é um protótipo acadêmico de presença digital para uma ONG fictícia. A ideia é mostrar como um site pode ajudar uma organização social a se apresentar ao público, divulgar suas iniciativas e aproximar pessoas que desejam contribuir.

O site foi pensado para diferentes visitantes: quem quer conhecer a organização e seu impacto, quem procura oportunidades de voluntariado, quem deseja apoiar financeiramente uma causa e quem precisa encontrar informações de contato e transparência. A identidade visual usa o tema de sementes e cultivo como metáfora para o impacto que cresce quando a comunidade participa.

As páginas formam um percurso simples: a página inicial apresenta a missão e os destaques; a página de projetos detalha as iniciativas, formas de participação e apoio; e o cadastro permite demonstrar como alguém manifesta interesse em fazer parte da rede.

Este projeto também serve como exercício de desenvolvimento front-end com HTML semântico, CSS responsivo, JavaScript, formulários acessíveis, validação no navegador e organização de recursos locais.

## O que você encontra

- **Início:** apresentação da Rede Semente, missão, visão e valores, indicadores ilustrativos de impacto, projetos em destaque, transparência e formas de contato.
- **Projetos:** iniciativas sociais organizadas por categoria, filtro interativo, oportunidades de voluntariado e uma área demonstrativa de doação.
- **Cadastro:** formulário de interesse para pessoas voluntárias, apoiadores ou possíveis parceiros, com campos de contato e endereço, validação HTML5 e máscaras de CPF, telefone e CEP.
- **Navegação responsiva:** menu adaptado a celulares, links para as principais áreas e acesso às páginas pelo menu e pelas chamadas de ação.

## Importante: protótipo demonstrativo

A Rede Semente, seus contatos, documentos, projetos, números e demais dados institucionais são fictícios. O site não representa uma ONG real.

O cadastro, a newsletter e a doação são demonstrações de interface: **não enviam nem armazenam dados e não processam pagamentos**. Não informe dados pessoais reais. Para transformar o protótipo em um serviço real, seria necessário substituir as informações de exemplo, implementar um backend seguro, integrar serviços de pagamento e newsletter e publicar políticas de privacidade e tratamento de dados.

## Estrutura

- `index.html` — página inicial e apresentação institucional.
- `projetos.html` — iniciativas, voluntariado, apoio e transparência.
- `cadastro.html` — formulário demonstrativo de interesse.
- `style.css` — identidade visual, estilos responsivos e estados de foco.
- `script.js` — menu móvel, filtro de projetos, máscaras e validação demonstrativa dos formulários.
- `assets/` — ilustrações SVG usadas pelo site.

## Executar

Abra `index.html` em um navegador ou sirva a pasta com qualquer servidor web estático. Não há dependências de build nem recursos externos obrigatórios.

## Acessibilidade e desempenho

As páginas incluem landmarks HTML5, hierarquia de títulos, link para pular ao conteúdo, rótulos de formulário, foco visível, mensagens de estado com `aria-live` e suporte a `prefers-reduced-motion`. As ilustrações SVG são locais, algumas imagens usam carregamento tardio e o layout se adapta a diferentes larguras de tela. Esses recursos apoiam a acessibilidade, mas não equivalem a uma certificação WCAG 2.1 AA.

As máscaras ajudam a formatar CPF, telefone e CEP durante a digitação, e o navegador verifica os dígitos do CPF. Essas verificações são apenas demonstrativas; validação no cliente não substitui validação no servidor.

Recursos como processamento real de doações, newsletter conectada, área administrativa, emissão de certificados, relatórios para download e seleção persistente de voluntários não fazem parte deste protótipo e exigem serviços adicionais.

## Publicar no GitHub Pages

Este projeto é HTML, CSS e JavaScript estáticos; não usa Jekyll nem precisa de etapa de build. O arquivo `.nojekyll` na raiz sinaliza isso ao GitHub Pages quando a publicação é configurada por branch.

1. Crie um repositório público no GitHub e envie **o conteúdo desta pasta** para a raiz do repositório. Confira que `index.html`, `projetos.html`, `cadastro.html`, `.nojekyll`, `style.css`, `script.js` e `assets/` estão na raiz.
2. Em **Settings → Pages → Build and deployment**, selecione **Deploy from a branch**, escolha a branch publicada (por exemplo, `main`) e a pasta `/(root)`.
3. Se o repositório usa um workflow em **GitHub Actions** que executa `jekyll-build-pages`, altere-o para publicação estática ou remova essa etapa; `.nojekyll` não corrige um template inválido dentro de um workflow Jekyll que foi configurado explicitamente.
4. Acesse o endereço fornecido pelo GitHub Pages e verifique as três páginas em desktop e celular.
5. Antes de divulgar, substitua os dados demonstrativos, configure domínio/HTTPS se necessário e conecte serviços reais de forma segura.

Se o log ainda mencionar `/_layouts/default.html`, o GitHub está tentando compilar Jekyll a partir de outra branch/pasta ou por um workflow que não corresponde ao conteúdo deste projeto. Confira **Actions → execução com falha** e **Settings → Pages → Build and deployment** para identificar a origem selecionada.

## Validação HTML

Valide cada página publicada ou o código copiado no [W3C Nu HTML Checker](https://validator.w3.org/nu/). Revise também a acessibilidade e contraste com testes automatizados e navegação manual por teclado/leitor de tela; a estrutura de um protótipo não representa, por si só, certificação WCAG 2.1 AA.
