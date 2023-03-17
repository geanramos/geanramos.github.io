
# sem estilo, por favor!
traduzido para **pt_BR** por [https://github.com/geanramos](@geanramos)

[![](https://i.imgur.com/gsYDjHP.pngwq)](https://i.imgur.com/gsYDjHP.png)[Um tema Jekyll](https://jekyllrb.com/) (quase) sem CSS, rápido e minimalista . Inspirado no [site da elly](http://tilde.town/~elly/) , criado expressamente para [o meu blog pessoal](https://riggraz.dev/) .

### [](#try-the-demo-out)[Experimente a demonstração!](https://riggraz.dev/no-style-please/)

[![](https://i.imgur.com/4eqXO4G.png)](https://i.imgur.com/4eqXO4G.png)

## [](#features)Características

-   Rápido ( **1kb de CSS!** Para obter mais informações sobre desempenho e muito mais, consulte [o relatório Page Speed ​​Insights](https://i.imgur.com/ob7e9zh.png) e [o relatório Lighthouse](https://i.imgur.com/ob7e9zh.png) )
-   Modos claro, escuro e automático
-   Responsivo
-   Conteúdo primeiro (tipografia otimizada para máxima legibilidade)
-   SEO otimizado (usa [Jekyll SEO Tag](https://github.com/jekyll/jekyll-seo-tag) )
-   RSS feed (usa o [Jekyll Feed](https://github.com/jekyll/jekyll-feed) )
-   Totalmente compatível com o [GitHub Pages](https://pages.github.com/) (consulte [a instalação do GitHub Pages](#github-pages-installation) )

## [](#installation)Instalação

Se você ainda não criou seu blog usando o Jekyll, siga as [instruções](https://jekyllrb.com/docs/) para fazê-lo na documentação do Jekyll.

NOTA: se você estiver usando o Jekyll com o GitHub Pages, consulte a [seção de instalação do GitHub Pages](#github-pages-installation) .

Em seguida, para estilizar seu blog com este tema, adicione esta linha ao seu site Jekyll `Gemfile`:

gem "no-style-please"

E adicione esta linha ao seu site Jekyll `_config.yml`:

theme: no-style-please

E então execute:

```
$ bundle

```

Ou instale você mesmo como:

```
$ gem install no-style-please

```

### [](#github-pages-installation)Instalação do GitHub Pages

Se você quiser usar este tema para o site do Jekyll implantado no [GitHub Pages](https://pages.github.com/) , siga as instruções [nesta página](https://docs.github.com/en/github/working-with-github-pages/adding-a-theme-to-your-github-pages-site-using-jekyll#adding-a-theme) .

## [](#usage)Uso

Você pode editar `_config.yml`o arquivo para personalizar seu blog. Você pode alterar coisas como o nome do blog, o autor, a aparência do tema (claro, escuro ou automático), como as datas são formatadas etc. Os campos personalizáveis ​​devem ser fáceis de entender. Ainda assim, `_config.yml`contém alguns comentários para ajudar você a entender o que cada campo faz.

Para maior personalização (por exemplo, layout, CSS), consulte a [documentação oficial do Jekyll](https://jekyllrb.com/docs/themes/#overriding-theme-defaults) sobre personalização de temas baseados em gem.

### [](#customize-the-menu)Personalize o cardápio

Para adicionar/editar/excluir entradas do menu principal, você deve editar o `menu.yml`arquivo dentro `_data`da pasta. Através desse arquivo você pode definir a estrutura do menu. Dê uma olhada na configuração padrão para ter uma ideia de como ela funciona e continue lendo para uma explicação mais abrangente.

O `menu.yml`arquivo aceita os seguintes campos:

-   `entries`definir uma nova lista não ordenada que conterá as entradas do menu
-   cada entrada é marcada por um `-`no início da linha
-   cada entrada pode ter os seguintes atributos:
    -   `title`, que define o texto a ser renderizado para esta entrada de menu ( **NB: você também pode especificar HTML!** )
    -   `url`, que pode ser usado para especificar um URL para esta entrada. Se não for especificado, `title`será processado como está; caso contrário, `title`será cercado por uma tag de link apontando para o URL especificado. Observe que a URL pode ser relativa ou absoluta. Observe também que você pode obter o mesmo resultado colocando uma `<a>`tag no `title`campo.
    -   `post_list`, que pode ser definido para `true`ou para um objeto. Se for verdadeiro, a entrada terá uma lista de todas as postagens como subentradas. Isso é usado para renderizar sua lista de postagens. Se você deseja personalizar quais postagens renderizar (por exemplo, por categoria), pode adicionar um ou mais dos seguintes atributos em `post_list`:
        -   `category`, que pode ser definido como uma cadeia de caracteres. Ele é usado para renderizar apenas uma lista de postagens da categoria especificada. Se você não definir, as postagens de todas as categorias serão renderizadas.
        -   `limit`, que pode ser definido como um número. Ele especifica o número de postagens a serem exibidas. Se não for definido, todas as postagens serão renderizadas.
        -   `show_more`, o que pode ser verdade. Se for true e se o número de postagens a serem exibidas for maior que o especificado `limit`, renderize um link para outra página. Para especificar a URL e o texto do link, você pode definir `show_more_url`e `show_more_text`atributos, que estão documentados abaixo.
        -   `show_more_url`, que pode ser uma string. Ele especifica a URL para o link mostrar mais. Use somente se for `show_more`verdadeiro. Isso geralmente redirecionará para uma página contendo todas as postagens, que você pode criar facilmente usando uma página de arquivo (consulte a seção [criar páginas de arquivo](#create-archive-pages) )
        -   `show_more_text`, que pode ser uma string. Ele especifica o texto para o link mostrar mais. Use somente se for `show_more`verdadeiro.
    -   `entries`, sim, você pode ter entradas dentro de entradas. Desta forma, você pode criar sublistas aninhadas!

### [](#create-archive-pages)Criar páginas de arquivo

A chamada página de arquivo é uma página que mostra uma lista de postagens (veja [um](https://riggraz.dev/no-style-please/all-posts) exemplo). Você pode criar uma página de arquivo criando uma página e colocando o seguinte frontmatter:

```
---
layout: archive
title: The title of the page here
which_category: name-of-category
---

```

`which_category`é opcional: se você não colocar, todos os posts do blog serão listados; por outro lado, se você especificar uma categoria, apenas os posts dessa categoria serão exibidos.

Esse recurso é particularmente útil se usado junto com o `show_more`atributo no menu. Por exemplo, se você deseja limitar o número de postagens mostradas na página inicial para 5, mas adicionar um link para visualizá-las todas, então você pode criar uma página de arquivo usando o método mostrado acima e vinculá-la usando o atributo `show_more_url`em `menu.yml`. Veja [este exemplo](https://github.com/riggraz/no-style-please/blob/master/_data/menu.yml) se estiver em dúvida.

### [](#customize-the-index-page)Personalize a página de índice

A `index.md`página deve usar layout `home`, que é o layout que exibe o menu. Se você quiser ter algum conteúdo após o menu, basta adicionar esse conteúdo no `index.md`arquivo e ele será exibido automaticamente no menu.

Outra coisa que você pode fazer para personalizar a página de índice é mostrar a descrição do seu blog entre o título e o menu. Para fazer isso, basta editar `_config.yml`e alterar `theme_config.show_description`para `true`.

### [](#pro-tips)dicas profissionais

#### [](#dark-mode-for-images)Modo escuro para imagens

Este tema fornece o modo escuro invertendo todas as cores do modo claro através da `invert()`função CSS. Essa abordagem também inverteria a cor de todas as imagens, mas, como esse não é o comportamento esperado, as imagens não são invertidas por padrão.

No entanto, se você quiser forçar a inversão de cores em uma imagem específica, pode fazê-lo aplicando `class="ioda"`a essa imagem ("ioda" significa "inverter na aparência escura"). Veja a imagem na [postagem de visão geral](https://github.com/riggraz/no-style-please/blob/master/_posts/2020-07-07-overview-post.md) para obter um exemplo dessa abordagem. Observe que a inversão de cores ocorrerá apenas quando o tema tiver uma aparência escura!

Por exemplo, se você tiver uma imagem em preto e branco, pode fazer sentido invertê-la no modo escuro. Por outro lado, uma imagem colorida provavelmente ficará ruim se for invertida.

## [](#contributing)Contribuindo

Relatórios de bugs e solicitações pull são bem-vindos no GitHub em [https://github.com/riggraz/no-style-please](https://github.com/riggraz/no-style-please) . Este projeto pretende ser um espaço seguro e acolhedor para colaboração, e espera-se que os colaboradores sigam o código de conduta [do Pacto do Colaborador](http://contributor-covenant.org/) .

## [](#development)Desenvolvimento

Para configurar seu ambiente para desenvolver este tema, execute `bundle install`.

Seu tema é configurado como um site Jekyll normal! Para testar seu tema, execute `bundle exec jekyll serve`e abra seu navegador em `http://localhost:4000`. Isso inicia um servidor Jekyll usando seu tema. Adicione páginas, documentos, dados, etc. normalmente para testar o conteúdo do seu tema. À medida que você faz modificações em seu tema e em seu conteúdo, seu site será regenerado e você deverá ver as alterações no navegador após uma atualização, como de costume.

Quando seu tema for lançado, apenas os arquivos em `_layouts`, `_includes`e rastreados com Git serão agrupados. Para adicionar um diretório personalizado ao seu tema-gem, edite o regexp de acordo.`_sass``assets``no-style-please.gemspec`

## [](#license)Licença

O tema está disponível como código aberto sob os termos da [licença MIT](https://opensource.org/licenses/MIT) .
