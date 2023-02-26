---
layout: post
title: Convertendo WordPress em html estatístico
slug: 
category: WordPress
---

[Ir para o conteúdo](https://wptavern.com/jamstacks-growing-popularity-brings-increase-in-wordpress-plugins-for-deploying-to-netlify#wp--skip-link--target)

![Taverna WP](https://wptavern.com/wp-content/uploads/2021/12/WPTLogo.svg)

11 de julho de 2019S por Sarah Gooding

### A crescente popularidade do JAMstack traz aumento nos plug-ins do WordPress para implantação no Netlify

Uma das tendências mais interessantes deste ano é que os desenvolvedores do WordPress estão começando a explorar as configurações do JAMstack para seus sites. JAMstack é um termo cunhado pelo CEO da [Netlify](https://www.netlify.com/) , Mathias Biilmann, para descrever a arquitetura de desenvolvimento que inclui JavaScript do lado do cliente, APIs reutilizáveis ​​e marcação pré-construída, os três pilares de um site estático moderno.

Sites estáticos estão fazendo um grande retorno agora, talvez como uma reação aos frameworks PHP lentos e inchados que rodam grandes porções da web hoje. A velocidade, segurança e escalabilidade desses sites, muitas vezes disponíveis a um custo menor, são algumas das razões mais convincentes pelas quais os desenvolvedores se juntam à crescente comunidade JAMstack. Ele também fornece um fluxo de trabalho de desenvolvimento compatível com git e CLI e permite que os desenvolvedores experimentem facilmente as tecnologias de front-end mais recentes, sem prescrever nenhuma estrutura ou ferramenta específica.

A maioria dos sites JAMstack são construídos usando Jekyll, Hugo, Nuxt, Next, Gatsby ou outro [gerador de site estático](https://www.staticgen.com/) . A marcação e os ativos gerados geralmente são servidos por meio de um CDN para carregamentos de página quase instantâneos.

[A Netlify](https://www.netlify.com/) foi pioneira na hospedagem JAMstack e inspirou a criação de uma infinidade de ferramentas que permitem implantações rápidas e convenientes. 

Os plug-ins que permitem aos desenvolvedores obter conteúdo do WordPress e hospedá-lo com o Netlify estão começando a aparecer com mais frequência. 

O nível gratuito do Netlify é um dos principais motivos de sua popularidade ter crescido tão rapidamente, pois fornece uma maneira rápida de hospedar um site pessoal ou um pequeno projeto com suporte a domínio personalizado, **HTTPS**, integração com Git e implantação contínua incluída.

[O Tiny Pixel Collective](https://tinypixel.dev/) criou um plug-in chamado [Netlify Deploy](https://github.com/pixelcollective/netlify-deploy) que automatiza as compilações do Netlify em eventos de publicação e atualização do WordPress. 

A empresa o construiu para tornar mais fácil para os desenvolvedores reconstruir os frontends Gatsby hospedados no Netlify usando o WordPress como ferramenta de publicação.

Ele funciona em segundo plano para manter um front-end estático em sincronia com o banco de dados de postagens, reconstruindo o site quando os usuários fazem atualizações em postagens e páginas. 

O plug-in aciona o webhook Netlify sempre que os tipos de postagem padrão do WordPress e a página sofrem uma alteração no status de publicação, mas também pode ser modificado para funcionar com tipos de postagem personalizados e ganchos de publicação personalizados.

[O JAMstack Deployments](https://wordpress.org/plugins/wp-jamstack-deployments/) , criado por [Christopher Geary](https://crgeary.com/) , um desenvolvedor e aficionado do JAMstack, é um plugin WordPress semelhante que facilita as implantações no Netlify, bem como em outras plataformas. 

A página de configurações do plug-in permite que os usuários configurem o URL do webhook no admin e inclui opções para limitá-lo a ser acionado em taxonomias e tipos de postagem específicos. 

JAMstack Deployments também está convenientemente disponível gratuitamente no WordPress.org.

[Deploy Netlify Webhook](https://wordpress.org/plugins/webhook-netlify-deploy/) é um plug-in semelhante de [Luke Secomb](https://lukesecomb.digital/) que parece funcionar manualmente por meio de um botão “Build” no administrador do WordPress. 

Ele tem o benefício adicional de permitir que os desenvolvedores verifiquem o status da compilação mais recente para ver se foi bem-sucedida, sem precisar sair do WordPress.

![](https://149611589.v2.pressablecdn.com/wp-content/uploads/2019/06/netlify-webhook-deploy.png)

[Justin Hall](https://justinwhall.com/) , autor de plugins e desenvolvedor web sênior no SendGrid, publicou seu [esqueleto inicial Gatsby + Headless WordPress + Netlify](https://github.com/justinwhall/gatsby-wordpress-netlify-starter) no GitHub. 

Essa configuração específica requer que o plug- [in LittleBot Netlify](https://github.com/justinwhall/littlebot-netlify) acione os ganchos de compilação do Netlify ao salvar ou atualizar, com uma opção adicional que permite que os usuários do WordPress publiquem em sites de teste ou produção.

![](https://149611589.v2.pressablecdn.com/wp-content/uploads/2019/06/stage-production.png)

[WP2Static](https://wordpress.org/plugins/static-html-output-plugin/) é um plugin popular que gera arquivos HTML estáticos a partir de um site WordPress. Os usuários têm a opção de implantar automaticamente em uma pasta no servidor, **um arquivo ZIP, servidor FTP, S3, GitHub, Netlify, BunnyCDN, BitBucket ou GitLab**. Atualmente, o plug-in Theh possui mais de 10.000 instalações ativas.

Estas são apenas uma pequena amostra das ferramentas que os desenvolvedores estão criando para permitir que os usuários do WordPress mantenham os recursos de uma plataforma de publicação dinâmica enquanto a constroem estaticamente para aproveitar os ganhos de velocidade, segurança e desempenho.

A tendência de usar um CMS headless combinado com geradores de sites estáticos é uma configuração fortemente voltada para desenvolvedores no momento.

[Traduzir todo o jargão](https://bejamas.io/blog/jamstack-for-clients/) para proprietários de sites e empresas não técnicos é um novo desafio para quem procura vender serviços para configurar a arquitetura JAMstack.

É aí que plataformas de hospedagem mais fáceis de usar, como [Strattic](https://www.strattic.com/) , [Shifter](https://www.getshifter.io/) e [HardyPress](https://www.hardypress.com/) , estão fazendo incursões no marketing da tecnologia JAMstack para um público menos técnico. 

Eles fornecem soluções de arquitetura “sem servidor” completas que geram arquivos estáticos de sites WordPress e os fornecem via CDN.

Uma das principais desvantagens de buscar uma configuração estática do WordPress é que muitos recursos dinâmicos não funcionam nesse ambiente. Adicionar formulários de contato pode ser um desafio. 

Sites que exigem comentários nativos do WordPress ou qualquer coisa mais complexa e interativa não funcionarão. 

Isso inclui funcionalidades oferecidas por WooCommerce, bbPress, BuddyPress e plugins de associação, para citar alguns exemplos. 

Por enquanto, o fervor do JAMstack é limitado principalmente ao público de desenvolvedores DIY que procura hospedar sites mais simples.

Tags: JAMstack , Netlify