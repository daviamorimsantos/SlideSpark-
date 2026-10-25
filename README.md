# SlideSpark Studio — estúdio interno

O SlideSpark Studio é a ferramenta privada de criação de apresentações. O site público para clientes continua sendo **NotaPronta — Apoio Escolar**: https://daviamorimsantos.github.io/NotaPronta-Apoio-Escolar-/

## Incluído
- Sem checkout ou endpoints de pagamento neste projeto. Os pagamentos são combinados diretamente no privado.
- Acesso direto, sem tela de código ou login.
- 12 temas visuais, incluindo desenho à mão/doodles, cartoon, quadrinhos, aquarela, infográfico, caderno, minimalista, premium escuro, claro, verde, retrô e ciência.
- Geração via Gemini e exportação para PowerPoint e PDF.

## Configuração obrigatória
1. Publique o projeto na Vercel para que as funções `api/auth.js` e `api/generate.js` sejam executadas. GitHub Pages não executa essas funções.
2. Nas variáveis de ambiente da Vercel, configure `GEMINI_API_KEY`. `GEMINI_MODEL` é opcional.
3. Edite `config.js` e substitua `https://SEU-BACKEND.vercel.app` pela URL real do projeto na Vercel.
4. Publique os arquivos estáticos do estúdio no GitHub Pages. O backend permite chamadas do domínio `https://daviamorimsantos.github.io`.
5. Teste a geração e a exportação.

## Privacidade — importante
O bloqueio de geração é validado no backend, e a senha não fica escrita no JavaScript. Porém, GitHub Pages comum publica o HTML/CSS/JS na internet; a tela de entrada não torna os arquivos do site privados. Para garantir que só duas contas tenham acesso até à própria página, hospede a interface em uma plataforma com autenticação real e controle de acesso. Não coloque senhas ou chaves de API no repositório.

## Sobre os desenhos
Os temas ilustrados adicionam paletas, formas vetoriais e instruções visuais específicas. A IA fornece também sugestões de desenhos/diagramas por slide, exibidas na prévia e nos arquivos. Esta versão não cria automaticamente imagens bitmap completas; o visual é composto por layouts, formas e sugestões de ilustração.


**Aviso:** esta versão remove o login. Como o site está no GitHub Pages público, qualquer pessoa com o link pode abrir o estúdio. Se a geração estiver conectada a uma chave de IA, terceiros também poderão tentar usar a API e gerar custos. Para restringir o acesso de verdade sem digitar código, hospede o site atrás de autenticação da plataforma (por exemplo, controle de acesso privado na hospedagem).
