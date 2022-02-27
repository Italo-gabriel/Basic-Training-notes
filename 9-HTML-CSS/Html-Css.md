**ESTRUTURA DO HTML - NOÇÕES BASICAS**

*Anatomia HTML*

HTML é composto de elementos . Esses elementos estruturam a página da Web e definem seu conteúdo. Vamos dar uma olhada em como eles são escritos.

O diagrama do elemento parágrafo é composto por:

Uma tag de abertura ( <p>)
O conteúdo (texto “Hello World!”)
Uma tag de fechamento ( </p>)
Uma tag e o conteúdo entre ela é chamado de elemento HTML. Existem muitas tags que podemos usar para organizar e exibir texto e outros tipos de conteúdo, como imagens.

Vamos revisar rapidamente cada parte do elemento retratado:

    Elemento HTML (ou simplesmente, elemento) — uma unidade de conteúdo em um documento HTML formado por tags HTML e o texto ou mídia que ele contém.

    Tag HTML — o nome do elemento, cercado por um colchete angular de abertura ( <) e fechamento ( ).>

    Tag de Abertura — a primeira tag HTML usada para iniciar um elemento HTML. O tipo de tag é cercado por colchetes angulares de abertura e fechamento.

    Conteúdo — As informações (texto ou outros elementos) contidas entre as tags de abertura e fechamento de um elemento HTML.

    Tag de fechamento — a segunda tag HTML usada para encerrar um elemento HTML. As tags de fechamento têm uma barra ( /) dentro delas, logo após o colchete esquerdo.

*O corpo do HTML*

Um dos principais elementos HTML que usamos para construir uma página da web é o elemento body . Somente o conteúdo dentro das tags de corpo de abertura e fechamento pode ser exibido na tela. 
Veja como são as tags de corpo de abertura e fechamento:

<body>
    <p>...</p>  ---- aqui vai todo o conteudo do paragrafo
</body>

*Estrutura HTML*

HTML é organizado como uma coleção de relacionamentos de árvores genealógicas. Como você viu no último exercício, colocamos <p>tags dentro de <body>tags. Quando um elemento está contido em outro elemento, ele é considerado filho desse elemento. Diz-se que o elemento filho está aninhado dentro do elemento pai .

<body>
<p>This paragraph is a child of the body</p>
</body>

No exemplo acima, o <p>elemento está aninhado dentro do <body>elemento. O <p>elemento é considerado filho do <body>elemento e o <body>elemento é considerado pai. Você também pode ver que adicionamos dois espaços de recuo (usando a spacebarra) para melhor legibilidade.

Como pode haver vários níveis de aninhamento, essa analogia pode ser estendida a netos, bisnetos e além. A relação entre os elementos e seus elementos ancestrais e descendentes é conhecida como hierarquia .

Vamos considerar um exemplo mais complicado que usa algumas novas tags:

<body>
  <div>
    <h1>Sibling to p, but also grandchild of body</h1>
    <p>Sibling to h1, but also grandchild of body</p>
  </div>
</body>

Neste exemplo, o <body>elemento é o pai do <div>elemento. Ambos os elementos <h1>e <p>são filhos do <div>elemento. Como os elementos <h1>e <p>estão no mesmo nível, eles são considerados irmãos e são ambos netos do <body>elemento.

Compreender a hierarquia HTML é importante porque os elementos filho podem herdar o comportamento e o estilo de seu elemento pai. Você aprenderá mais sobre hierarquia de páginas da Web quando começar a explorar CSS.

`Exemplo`
<body>
  <h1>Hello World</h1>
  <p>This paragraph is a child of the body element</p>
  <div>
    <p>This paragraph is a child of the div element and a grandchild of the body element</p>
  </div> 
</body>

*Títulos*

Os títulos em HTML são semelhantes aos títulos em outros tipos de mídia. Por exemplo, em jornais, títulos grandes são normalmente usados para capturar a atenção do leitor. Outras vezes, os títulos são usados para descrever o conteúdo, como o título de um filme ou um artigo educacional.

O HTML segue um padrão semelhante. Em HTML, existem seis títulos diferentes , ou elementos de título . Os títulos podem ser usado para diversos fins, como títulos de seções, artigos ou outras formas de conteúdo.

A seguir está a lista de elementos de cabeçalho disponíveis em HTML. Eles são ordenados do maior para o menor em tamanho.

<h1>— usado para títulos principais. Todos os outros títulos menores são usados para subtítulos.
<h2>
<h3>
<h4>
<h5>
<h6>
O código de exemplo a seguir usa um título destinado a capturar a atenção do leitor. Ele usa o maior título disponível, o elemento de título principal:

<h1>BREAKING NEWS</h1>

`Exemplo`
<body>
<h1>BREAKING NEWS</h1>
  <h2>About Brown Bears</h2>
  <h3>Species</h3>
<h3>Features</h3>
  <h2>Habitat</h2>
  <h3>Countries with Large Brown Bear Populations</h3>
  <h3>Countries with Small Brown Bear Populations</h3>
<h2>Media</h2>  
</body>

*Divs*

Um dos elementos mais populares em HTML é o <div>elemento. <div>é a abreviação de "divisão" ou um contêiner que divide a página em seções. Essas seções são muito úteis para agrupar elementos em seu HTML.

<body>
  <div>
    <h1>Why use divs?</h1>
    <p>Great for grouping elements!</p>
  </div>
</body>
<div>

As divs não têm uma representação visual inerente, mas são muito úteis quando queremos aplicar estilos personalizados aos nossos elementos HTML. <div>s nos permitem agrupar elementos HTML para aplicar os mesmos estilos para todos os elementos HTML internos. Também podemos estilizar o <div>elemento como um todo. Você pode ver como isso pode ser feito no curso Aprenda CSS .

<div>s podem conter qualquer texto ou outros elementos HTML, como links, imagens ou vídeos. Lembre-se de sempre adicionar dois espaços de recuo ao aninhar elementos dentro de <div>s para melhor legibilidade.

`Exemplo`
<body>
  <h1>The Brown Bear</h1>
  <div>
    <h2>About Brown Bears</h2>
    <h3>Species</h3>
    <h3>Features</h3>
  </div>
  <div>
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <h3>Countries with Small Brown Bear Populations</h3>
  </div>
  <div>
    <h2>Media</h2>
  </div>
</body>

*Atributos*

Se quisermos expandir a tag de um elemento, podemos fazê-lo usando um atributo. Atributos são conteúdos adicionados à tag de abertura de um elemento e podem ser usados ​​de várias maneiras diferentes, desde fornecer informações até alterar o estilo. Os atributos são compostos das duas partes a seguir:

  O nome do atributo
  O valor do atributo

Um atributo comumente usado é o id. Podemos usar o id atributo para especificar conteúdo diferente (como <div>s) e é muito útil quando você usa um elemento mais de uma vez. ids têm vários propósitos diferentes em HTML, mas, por enquanto, vamos nos concentrar em como eles podem nos ajudar a identificar o conteúdo em nossa página.

Quando adicionamos um ida a <div>, colocamos na tag de abertura:

<div id="intro">
  <h1>Introduction</h1>
</div>

`Exemplo`
<body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <h3>Species</h3>
    <h3>Features</h3>
  </div>
  <div id="Habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <h3>Countries with Small Brown Bear Populations</h3>
  </div>
  <div id="Media">
    <h2>Media</h2>
  </div>
</body>

*Exibindo texto*

Se você deseja exibir texto em HTML, você pode usar um parágrafo ou uma extensão :

Os parágrafos ( <p>) contêm um bloco de texto simples.
<span>contém pequenos pedaços de texto ou outro HTML. Eles são usados ​​para separar pequenos pedaços de conteúdo que estão na mesma linha de outros conteúdos.

Dê uma olhada em cada um desses elementos em ação abaixo:

<div>
  <h1>Technology</h1>
</div>
<div>
  <p><span>Self-driving cars</span> are anticipated to replace up to 2 million jobs over the next two decades.</p>
</div>

No exemplo acima, existem dois arquivos <div>. O segundo <div>contém um <p>com <span>Self-driving cars</span>. Esse <span>elemento separa “Carros autônomos” do restante do texto do parágrafo.

É melhor usar um <span>elemento quando você deseja segmentar um conteúdo específico que está embutido ou na mesma linha de outro texto. Se você quiser dividir seu conteúdo em blocos , é melhor usar um arquivo <div>.

`Exemplo`
<body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
      <p>“The brown bear (Ursus arctos) is native to parts of northern Eurasia and North America. Its conservation status is currently Least Concern. There are many subspecies within the brown bear species, including the Atlas bear and the Himalayan brown bear.”</p>
    <h3>Species</h3>
    <h3>Features</h3>
      <p>“Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.”</p>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <h3>Countries with Small Brown Bear Populations</h3>
      <p>“Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.”</p>
  </div>
  <div id= "media">
    <h2>Media</h2>
  </div>
</body>

*Texto de estilo*

Você também pode estilizar o texto usando tags HTML. A <em>tag enfatiza o texto, enquanto a <strong>tag destaca o texto importante.

Mais tarde, quando você começar a estilizar sites, você decidirá como deseja que os navegadores exibam o conteúdo <em>e as <strong>tags. Os navegadores, no entanto, têm folhas de estilo internas que geralmente estilizam essas tags das seguintes maneiras:

A <em>tag geralmente será renderizada como ênfase em itálico .
O <strong>geralmente será renderizado como ênfase em negrito .

Dê uma olhada em cada estilo em ação:

<p><strong>The Nile River</strong> is the <em>longest</em> river in the world, measuring over 6,850 kilometers long (approximately 4,260 miles).</p>

Neste exemplo, as tags <strong>e <em>são usadas para enfatizar o texto para produzir o seguinte:

The Nile River is the longest river in the world, measuring over 6,850 kilometers long (approximately 4,260 miles).

Como podemos ver, “The Nile River” está em negrito e “longest” está em itálico.

`Exemplo`
<body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear <em>(Ursus arctos)</em> is native to parts of northern Eurasia and North America. Its conservation status is currently ,<strong>Least Concern.</strong> There are many subspecies within the brown bear species, including the Atlas bear and the Himalayan brown bear.</p>
    <h3>Species</h3>
    <h3>Features</h3>
    <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <h3>Countries with Small Brown Bear Populations</h3>
    <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
  </div>
  <div id="media">
    <h2>Media</h2>
  </div>
</body>

*Quebras de linha*

O espaçamento entre o código em um arquivo HTML não afeta o posicionamento dos elementos no navegador. Se estiver interessado em modificar o espaçamento no navegador, você pode usar o elemento de quebra de linha<br> do HTML: .

O elemento de quebra de linha é único porque é composto apenas por uma tag inicial. Você pode usá-lo em qualquer lugar dentro do seu código HTML e uma quebra de linha será mostrada no navegador.

<p>The Nile River is the longest river <br> in the world, measuring over 6,850 <br> kilometers long (approximately 4,260 <br> miles).</p>

O código no exemplo acima resultará em uma saída semelhante à seguinte:

The Nile River is the longest river              --<br>
in the world, measuring over 6,850               --<br> Essas tags <br> fazem a quebra de linha como no texto do exemplo
kilometers long (approximately 4,260             --<br>
miles).

*Listas não ordenadas*

Além de organizar o texto em forma de parágrafo, você também pode exibir o conteúdo em uma lista de fácil leitura.

Em HTML, você pode usar uma tag de lista não ordenada<ul> ( ) para criar uma lista de itens em nenhuma ordem específica. Uma lista não ordenada descreve itens de lista individuais com um marcador.

O <ul>elemento não deve conter texto bruto e não formatará automaticamente o texto bruto em uma lista não ordenada de itens. Itens de lista individuais devem ser adicionados à lista não ordenada usando a <li>tag. A <li>tag de item ou lista é usada para descrever um item em uma lista.

<ul>
  <li>Limes</li>
  <li>Tortillas</li>
  <li>Chicken</li>
</ul>

No exemplo acima, a lista foi criada usando a <ul>tag e todos os itens da lista individual foram adicionados usando <li>tags.

A saída ficará assim:

  Limes
  Tortillas
  Chicken

`Exemplo`
<body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>. <br><br> There are many subspecies within the brown bear species, including the Atlas bear and the Himalayan brown bear.</p>
    <h3>Species</h3>
      <ul>
        <li>Arctos</li>
        <li>Collarus</li>
        <li>Horribilis</li>
        <li>Nelsoni (extinct)</li>
      </ul>
    <h3>Features</h3>
    <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <h3>Countries with Small Brown Bear Populations</h3>
    <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
  </div>
  <div id="media">
    <h2>Media</h2>
  </div>
</body>

*Listas ordenadas*

Listas ordenadas ( <ol>) são como listas não ordenadas, exceto que cada item da lista é numerado. Eles são úteis quando você precisa listar diferentes etapas em um processo ou classificar itens do primeiro ao último.

Você pode criar a lista ordenada com a <ol>tag e adicionar itens de lista individuais à lista usando <li>tags.

<ol>
  <li>Preheat the oven to 350 degrees.</li>
  <li>Mix whole wheat flour, baking soda, and salt.</li>
  <li>Cream the butter, sugar in separate bowl.</li>
  <li>Add eggs and vanilla extract to bowl.</li>
</ol>

A saída ficará assim:

1. Preheat the oven to 350 degrees.
2. Mix whole wheat flour, baking soda, and salt.
3. Cream the butter, sugar in separate bowl.
4. Add eggs and vanilla extract to bowl.

`Exemplo`
<body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the Atlas bear and the Himalayan brown bear.</p>
    <h3>Species</h3>
    <ul>
      <li>Arctos</li>
      <li>Collarus</li>
      <li>Horribilis</li>
      <li>Nelsoni (extinct)</li>
    </ul>
    <h3>Features</h3>
    <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <ol>
      <li>Russia</li>
      <li>United States</li>
      <li>Canada</li>
    </ol>
    <h3>Countries with Small Brown Bear Populations</h3>
    <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
  </div>
  <div id="media">
    <h2>Media</h2>
  </div>
</body>

*Imagens*

Todos os elementos que você aprendeu até agora (títulos, parágrafos, listas e extensões) compartilham uma coisa em comum: eles são compostos inteiramente de texto! E se você quiser adicionar conteúdo à sua página da web que não seja composto de texto, como imagens ?

A <img>tag permite que você adicione uma imagem a uma página da web. A maioria dos elementos requer tags de abertura e fechamento, mas a <img>tag é uma tag de fechamento automático . Observe que o final da <img>tag tem uma barra /. As tags de fechamento automático podem incluir ou omitir a barra final — ambas serão renderizadas corretamente.

<img src="image-location.jpg" />
A <img>tag tem um atributo obrigatório chamado src. O srcatributo deve ser definido para a origem da imagem ou o local da imagem. Nesse caso, o valor de srcdeve ser o localizador uniforme de recursos (URL) da imagem. Um URL é o endereço da web ou endereço local onde um arquivo está armazenado.

`Exemplo`
<body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the Atlas bear and the Himalayan brown bear.</p>
    <h3>Species</h3>
    <ul>
      <li>Arctos</li>
      <li>Collarus</li>
      <li>Horribilis</li>
      <li>Nelsoni (extinct)</li>
    </ul>
    <h3>Features</h3>
    <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <ol>
      <li>Russia</li>
      <li>United States</li>
      <li>Canada</li>
    </ol>
    <h3>Countries with Small Brown Bear Populations</h3>
    <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
  </div>
  <div id="media">
    <h2>Media</h2>
      <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" />
  </div>
</body>

*Alts da imagem*

Parte de ser um desenvolvedor web excepcional é tornar seu site acessível a usuários de todas as origens. Para tornar a Web mais inclusiva, precisamos considerar o que acontece quando tecnologias assistivas, como leitores de tela, encontram tags de imagem.

O alt atributo, que significa texto alternativo, traz significado às imagens em nossos sites. O alt atributo pode ser adicionado à tag de imagem assim como o src atributo. O valor de alt deve ser uma descrição da imagem.

<img src="#" alt="A field of yellow sunflowers" />
O alt atributo também serve para os seguintes propósitos:

  Se uma imagem não carregar em uma página da Web, o usuário pode passar o mouse sobre a área originalmente destinada à imagem e ler uma breve descrição da imagem. Isso é possível pela descrição que você fornece no alt atributo.

  Usuários com deficiência visual costumam navegar na web com o auxílio de softwares de leitura de tela. Quando você inclui o alt atributo, o software de leitura de tela pode ler a descrição da imagem em voz alta para o usuário com deficiência visual.

  O alt atributo também desempenha um papel na otimização de mecanismos de pesquisa (SEO), porque os mecanismos de pesquisa não podem “ver” as imagens nos sites enquanto rastreiam a Internet. Ter alt atributos descritivos pode melhorar a classificação do seu site.

  Se a imagem na página da web não transmitir qualquer informação significativa para um usuário (deficiente visual ou não), o alt atributo deve ser deixado em branco.
  
  `Exemplo`
  <body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the Atlas bear and the Himalayan brown bear.</p>
    <h3>Species</h3>
    <ul>
      <li>Arctos</li>
      <li>Collarus</li>
      <li>Horribilis</li>
      <li>Nelsoni (extinct)</li>
    </ul>
    <h3>Features</h3>
    <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <ol>
      <li>Russia</li>
      <li>United States</li>
      <li>Canada</li>
    </ol>
    <h3>Countries with Small Brown Bear Populations</h3>
    <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
  </div>
  <div id="media">
    <h2>Media</h2>
    <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" alt="brown bear in the forest"/>
  </div>
</body>

*Videos*

Além das imagens, o HTML também suporta a exibição de vídeos . Assim como a <img>tag, a <video>tag requer um srcatributo com um link para a fonte de vídeo. Ao contrário da <img>tag, no entanto, o <video>elemento requer uma tag de abertura e uma tag de fechamento.

<video src="myVideo.mp4" width="320" height="240" controls>
  Video not supported
</video>

Neste exemplo, a origem do vídeo ( src) é myVideo.mp4 A origem pode ser um arquivo de vídeo hospedado ao lado de sua página da Web ou um URL que aponta para um arquivo de vídeo hospedado em outra página da Web.

Após o src atributo, os atributos width e height são usados para definir o tamanho do vídeo exibido no navegador. O controls atributo instrui o navegador a incluir controles básicos de vídeo: pausar, reproduzir e pular.

O texto “Vídeo não suportado”, entre as tags de abertura e fechamento do vídeo, só será exibido se o navegador não conseguir carregar o vídeo.

`Exemplo`
<body>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the Atlas bear and the Himalayan brown bear.</p>
    <h3>Species</h3>
    <ul>
      <li>Arctos</li>
      <li>Collarus</li>
      <li>Horribilis</li>
      <li>Nelsoni (extinct)</li>
    </ul>
    <h3>Features</h3>
    <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <ol>
      <li>Russia</li>
      <li>United States</li>
      <li>Canada</li>
    </ol>
    <h3>Countries with Small Brown Bear Populations</h3>
    <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
  </div>
  <div id="media">
    <h2>Media</h2>
    <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" alt="A Brown Bear"/>
    <video src="https://content.codecademy.com/courses/freelance-1/unit-1/lesson-2/htmlcss1-vid_brown-bear.mp4" width="320" height="240" controls> Video not supported</video>
  </div>
</body>
  
**PADRÕES DE DOCUMENTOS HTML**

*Preparando-se para HTML*

Agora que aprendemos sobre alguns dos elementos HTML mais comuns, é hora de aprender como configurar um arquivo HTML.

Os arquivos HTML requerem certos elementos para configurar o documento corretamente. Podemos informar aos navegadores que estamos usando HTML iniciando nosso documento com uma declaração de tipo de documento .

A declaração fica assim:

<!DOCTYPE html>
Esta declaração é uma instrução e deve ser a primeira linha de código em seu documento HTML. Ele informa ao navegador que tipo de documento esperar, junto com qual versão do HTML está sendo usada no documento. Por enquanto, o navegador assumirá corretamente que o htmlin <!DOCTYPE html>está se referindo ao HTML5, pois é o padrão atual.

No futuro, no entanto, um novo padrão substituirá o HTML5. Para garantir que seu documento seja sempre interpretado corretamente, sempre inclua <!DOCTYPE html>no início de seus documentos HTML.

Por fim, o código HTML é sempre salvo em um arquivo com extensão .html

*A tag html*

A <!DOCTYPE html>declaração fornece ao navegador duas informações (o tipo de documento e a versão HTML esperada), mas na verdade não adiciona nenhuma estrutura ou conteúdo HTML.

Para criar estrutura e conteúdo HTML, devemos adicionar <html>tags de abertura e fechamento após declarar <!DOCTYPE html>:

<!DOCTYPE html>
<html>
 
</html>
Qualquer coisa entre as tags de abertura <html>e fechamento </html>será interpretada como código HTML. Sem essas tags, é possível que os navegadores interpretem incorretamente seu código HTML.


*A cabeça*

Até agora você fez duas coisas para configurar o arquivo corretamente:

Declarou ao navegador que seu código é HTML com <!DOCTYPE html>
Adicionado o elemento HTML ( <html>) que conterá o restante do seu código.
Adicionamos esses elementos à página Brown Bears que você criou anteriormente. Agora, vamos também fornecer ao navegador algumas informações sobre a própria página. Podemos fazer isso adicionando um <head>elemento.

Lembra da <body>etiqueta? O <head>elemento faz parte dessa metáfora HTML. Ele vai acima do nosso <body>elemento.

O <head>elemento contém os metadados de uma página da web. Metadados são informações sobre a página que não são exibidas diretamente na página da web. Ao contrário das informações dentro da <body>tag, os metadados no cabeçalho são informações sobre a própria página. Você verá um exemplo disso no próximo exercício.

As tags head de abertura e fechamento geralmente aparecem como o primeiro item após sua primeira tag HTML:

<head>
</head>

`Exemplo`
<!DOCTYPE html>           >>>>    *Configurações do HTML - especifica a versão do HTML para o navegador**
<html>
  <head>                  >>>>    **Cabeça - contém os metadados de uma página da Web**
  </head>
  <body>                  >>>>    **Corpo -  Toda e estrutura do HTML**
    <h1>The Brown Bear</h1>
    <div id="introduction">
      <h2>About Brown Bears</h2>
      <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the
        Atlas bear and the Himalayan brown bear.</p>
      <h3>Species</h3>
      <ul>
        <li>Arctos</li>
        <li>Collarus</li>
        <li>Horribilis</li>
        <li>Nelsoni (extinct)</li>
      </ul>
      <h3>Features</h3>
      <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
    </div>
    <div id="habitat">
      <h2>Habitat</h2>
      <h3>Countries with Large Brown Bear Populations</h3>
      <ol>
        <li>Russia</li>
        <li>United States</li>
        <li>Canada</li>
      </ol>
      <h3>Countries with Small Brown Bear Populations</h3>
      <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
    </div>
    <div id="media">
      <h2>Media</h2>
      <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" />
      <video src="https://content.codecademy.com/courses/freelance-1/unit-1/lesson-2/htmlcss1-vid_brown-bear.mp4" width="320" height="240" controls>Video not supported</video>
    </div>
  </body>
</html>

*Títulos de página*

Que tipo de metadados sobre a página da web o <head>elemento pode conter?

Se você navegar até o catálogo da Codecademy e olhar na parte superior do seu navegador, você notará as palavras All Courses & Tutorials | Codecademy, que é o título da página da web.

A guia de um navegador exibe o título especificado na <title>tag. A <title>tag está sempre dentro do <head>.

<!DOCTYPE html>
<html>
  <head>
    <title>My Coding Journal</title>
  </head>
</html>
Se abrissemos um arquivo contendo o código HTML do exemplo acima, o navegador exibiria as palavras My Coding Journalna barra de título (ou no título da guia).

`Exemplo`
<!DOCTYPE html>
<html>
  <head>
     <title>Brown Bears</title>
	</head>
  <body>
    <h1>The Brown Bear</h1>
    <div id="introduction">
      <h2>About Brown Bears</h2>
      <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the
        Atlas bear and the Himalayan brown bear.</p>
      <h3>Species</h3>
      <ul>
        <li>Arctos</li>
        <li>Collarus</li>
        <li>Horribilis</li>
        <li>Nelsoni (extinct)</li>
      </ul>
      <h3>Features</h3>
      <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
    </div>
    <div id="habitat">
      <h2>Habitat</h2>
      <h3>Countries with Large Brown Bear Populations</h3>
      <ol>
        <li>Russia</li>
        <li>United States</li>
        <li>Canada</li>
      </ol>
      <h3>Countries with Small Brown Bear Populations</h3>
      <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
    </div>
    <div id="media">
      <h2>Media</h2>
      <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" />
      <video src="https://content.codecademy.com/courses/freelance-1/unit-1/lesson-2/htmlcss1-vid_brown-bear.mp4" width="320" height="240" controls>Video not supported</video>
    </div>
  </body>
</html>

*Link para outras páginas da web*

Um dos aspectos poderosos do HTML (e da Internet) é a capacidade de vincular a outras páginas da web.

Você pode adicionar links a uma página da Web adicionando um elemento âncora<a> e incluindo o texto do link entre as tags de abertura e fechamento.

<a>This Is A Link To Wikipedia</a>
Espere um minuto! Tecnicamente, o link no exemplo acima está incompleto. Como exatamente o link acima deve funcionar se não houver um URL que leve os usuários à página real da Wikipedia?

O elemento âncora no exemplo acima está incompleto sem o href atributo. Esse atributo significa referência de hiperlink e é usado para vincular a um caminho ou ao endereço de onde um arquivo está localizado (seja no seu computador ou em outro local). Os caminhos fornecidos para o href atributo geralmente são URLs.

<a href="https://www.wikipedia.org/">This Is A Link To Wikipedia</a>
No exemplo acima, o href atributo foi definido com o valor da URL https://www.wikipedia.org/. O exemplo agora mostra o uso correto de um elemento âncora.

Ao ler a documentação técnica, você pode se deparar com o termo hyperlink . Não se preocupe, este é simplesmente o termo técnico para link. Esses termos são frequentemente usados de forma intercambiável.

`Exemplo`
<!DOCTYPE html>
<html>
  <head>
		<title>Brown Bears</title>
	</head>
  <body>
    <h1>The Brown Bear</h1>
    <div id="introduction">
      <h2>About Brown Bears</h2>
      <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the
        Atlas bear and the Himalayan brown bear.</p>
      <a href="https://en.wikipedia.org/wiki/Brown_bear">Learn More</a> 
      <h3>Species</h3>
      <ul>
        <li>Arctos</li>
        <li>Collarus</li>
        <li>Horribilis</li>
        <li>Nelsoni (extinct)</li>
      </ul>
      <h3>Features</h3>
      <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
    </div>
    <div id="habitat">
      <h2>Habitat</h2>
      <h3>Countries with Large Brown Bear Populations</h3>
      <ol>
        <li>Russia</li>
        <li>United States</li>
        <li>Canada</li>
      </ol>
      <h3>Countries with Small Brown Bear Populations</h3>
      <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
    </div>
    <div id="media">
      <h2>Media</h2>
      <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" />
      <video src="https://content.codecademy.com/courses/freelance-1/unit-1/lesson-2/htmlcss1-vid_brown-bear.mp4" width="320" height="240" controls>Video not supported</video>
    </div>
  </body>
</html>

*Abrindo links em uma nova janela*

Você já clicou em um link e observou a página da Web resultante aberta em uma nova janela do navegador? Se sim, você pode agradecer ao atributo <a> do elemento .target

O target atributo especifica como um link deve ser aberto.

É possível que um ou mais links em sua página da Web levem a um site totalmente diferente. Nesse caso, você pode querer que os usuários leiam o site vinculado, mas espere que eles retornem à sua página da web. Isso é exatamente quando o target atributo é útil!

Para que um link seja aberto em uma nova janela, o target atributo requer um valor de _blank. O target atributo pode ser adicionado diretamente na tag de abertura do elemento âncora, assim como o href atributo.

<a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank">The Brown Bear</a>
No exemplo acima, definir o target atributo para "_blank" instrui o navegador a abrir a página relevante da Wikipedia em uma nova janela.

Neste exercício, usamos a terminologia “abrir em uma nova janela”. É provável que você esteja usando um navegador moderno que abre sites em novas guias , em vez de novas janelas. Antes do advento dos navegadores com guias, janelas adicionais do navegador precisavam ser abertas para visualizar mais sites. O target="_blank" atributo, quando usado em navegadores modernos, abrirá novos sites em uma nova aba.

`Exemplo`
<!DOCTYPE html>
<html>
  <head>
		<title>Brown Bears</title>
	</head>
  <body>
    <h1>The Brown Bear</h1>
    <div id="introduction">
      <h2>About Brown Bears</h2>
      <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the
        Atlas bear and the Himalayan brown bear.</p>
      <a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank">Learn More</a>
      <h3>Species</h3>
      <ul>
        <li>Arctos</li>
        <li>Collarus</li>
        <li>Horribilis</li>
        <li>Nelsoni (extinct)</li>
      </ul>
      <h3>Features</h3>
      <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
    </div>
    <div id="habitat">
      <h2>Habitat</h2>
      <h3>Countries with Large Brown Bear Populations</h3>
      <ol>
        <li>Russia</li>
        <li>United States</li>
        <li>Canada</li>
      </ol>
      <h3>Countries with Small Brown Bear Populations</h3>
      <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
    </div>
    <div id="media">
      <h2>Media</h2>
      <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" />
      <video src="https://content.codecademy.com/courses/freelance-1/unit-1/lesson-2/htmlcss1-vid_brown-bear.mp4" width="320" height="240" controls>Video not supported</video>
    </div>
  </body>
</html>

*Vinculação à página relativa*

Até agora, você aprendeu como criar links para páginas da web externas. Muitos sites também possuem links para páginas da Web internas, como Home, About e Contact.

Antes de aprendermos como vincular páginas internas, vamos estabelecer onde nossos arquivos são armazenados. Ao criar sites estáticos de várias páginas, os desenvolvedores da Web geralmente armazenam arquivos HTML no diretório raiz ou em uma pasta principal onde todos os arquivos do projeto são armazenados. À medida que o tamanho dos projetos que você cria aumenta, você pode usar pastas adicionais dentro da pasta principal do projeto para organizar seu código.

project-folder/
|—— about.html
|—— contact.html
|—— index.html

O exemplo acima mostra três arquivos diferentes — about.html , contact.html e index.html em uma pasta.

Os arquivos HTML geralmente são armazenados na mesma pasta, conforme mostrado no exemplo acima. Se o navegador estiver exibindo index.html , ele também saberá que about.html e contact.html estão na mesma pasta. Como os arquivos são armazenados na mesma pasta, podemos vincular páginas da Web usando um caminho relativo .

<a href="./contact.html">Contact</a>
Neste exemplo, a <a>tag é usada com um caminho relativo para vincular do arquivo HTML atual ao contact.htmlarquivo na mesma pasta. Na página da web, Contact aparecerá como um link.

Um caminho relativo é um nome de arquivo que mostra o caminho para um arquivo local (um arquivo no mesmo site, como ./index.html) versus um caminho absoluto (um URL completo, como o https://www.codecademy.com/learn/learn-htmlque é armazenado em uma pasta diferente). O ./in ./index.html diz ao navegador para procurar o arquivo na pasta atual.

`Exemplo`
<!DOCTYPE html>
<html>
  <head>
		<title>Brown Bears</title>
	</head>
  <body>
    <a href="./index.html">Brown Bear</a>         >>>>> Duas Estruturas para direcionar
    <a href="./aboutme.html">About Me</a>           >>>>> entre as paginas HTML de um projeto
    <h1>The Brown Bear</h1>
    <div id="introduction">
      <h2>About Brown Bears</h2>
      <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the
        Atlas bear and the Himalayan brown bear.</p>
      <a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank">Learn More</a>
      <h3>Species</h3>
      <ol>
        <li>Arctos</li>
        <li>Collarus</li>
        <li>Horribilis</li>
        <li>Nelsoni (extinct)</li>
      </ol>
      <h3>Features</h3>
      <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
    </div>
    <div id="habitat">
      <h2>Habitat</h2>
      <h3>Countries with Large Brown Bear Populations</h3>
      <ol>
        <li>Russia</li>
        <li>United States</li>
        <li>Canada</li>
      </ol>
      <h3>Countries with Small Brown Bear Populations</h3>
      <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
    </div>
    <div id="media">
      <h2>Media</h2>
      <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" />
      <video src="https://content.codecademy.com/courses/freelance-1/unit-1/lesson-2/htmlcss1-vid_brown-bear.mp4" width="320" height="240" controls>Video not supported</video>
    </div>
  </body>
</html>

*Linking At Will -Ligando à vontade*

Você provavelmente já visitou sites onde nem todos os links eram compostos de texto. Talvez os links em que você clicou fossem imagens ou alguma outra forma de conteúdo.

Até agora, adicionamos links compostos apenas de texto, como o seguinte:

<a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank">Prickly Pear</a>
Links somente de texto, no entanto, diminuiriam significativamente sua flexibilidade como desenvolvedor web!

Felizmente, o HTML permite que você transforme praticamente qualquer elemento em um link envolvendo esse elemento com um elemento âncora. Com esta técnica, é possível transformar imagens em links simplesmente envolvendo o <img>elemento com um <a>elemento.

<a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank"><img src="https://www.Prickly_Pear_Closeup.jpg" alt="A red prickly pear fruit"/></a>

No exemplo acima, uma imagem de uma pera espinhosa foi transformada em um link envolvendo a parte externa do <img>elemento com um <a>elemento.

`Exemplo`
<!DOCTYPE html>
<html>

<head>
  <title>Brown Bears</title>
</head>

<body>
  <a href="./index.html">Brown Bear</a>
  <a href="./aboutme.html">About Me</a>
  <h1>The Brown Bear</h1>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the
      Atlas bear and the Himalayan brown bear.</p>
    <a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank">Learn More</a>
    <h3>Species</h3>
    <ul>
      <li>Arctos</li>
      <li>Collarus</li>
      <li>Horribilis</li>
      <li>Nelsoni (extinct)</li>
    </ul>
    <h3>Features</h3>
    <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <ol>
      <li>Russia</li>
      <li>United States</li>
      <li>Canada</li>
    </ol>
    <h3>Countries with Small Brown Bear Populations</h3>
    <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
  </div>
  <div id="media">
    <h2>Media</h2>
    <a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank">
    <img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" alt="Brown Bears in Florest"/></a>
    <video src="https://content.codecademy.com/courses/freelance-1/unit-1/lesson-2/htmlcss1-vid_brown-bear.mp4" height="240" width="320" controls>Video not supported</video>
  </div>
</body>

</html>

*Link para a mesma página*

Neste ponto, temos todo o conteúdo que queremos em nossa página. Como temos tanto conteúdo, nem tudo cabe na tela. Como tornamos mais fácil para um usuário pular para diferentes partes da nossa página?

Quando os usuários visitam nosso site, queremos que eles possam clicar em um link e fazer com que a página role automaticamente para uma seção específica.

Para vincular a um destino na mesma página, devemos fornecer ao destino um id , como este:

<p id="top">This is the top of the page!</p>
<h1 id="bottom">This is the bottom! </h1>
Neste exemplo, o <p>elemento é atribuído como id“top” e o <h1>elemento é atribuído como “bottom”. Um id pode ser adicionado à maioria dos elementos em uma página da web.

Um id deve ser descritivo para facilitar a memorização da finalidade de um link. O link de destino é uma string contendo o #caractere e o id.

<ol>
  <li><a href="#top">Top</a></li>
  <li><a href="#bottom">Bottom</a></li>
</ol>
No exemplo acima, os links para <p id="top">e <h1 id="bottom">são incorporados em uma lista ordenada. Esses links aparecem no navegador como uma lista numerada de links. Um idé especialmente útil para organizar o conteúdo pertencente a um div!


`Exemplo`
<!DOCTYPE html>
<html>

<head>
  <title>Brown Bears</title>
</head>

<body>
  <a href="./index.html">Brown Bear</a>
  <a href="./aboutme.html">About Me</a>
  <h1>The Brown Bear</h1>
  <ul>
    <li><a href="#introduction">Introduction</a></li>
    <li><a href="#habitat">Habitat</a></li>
    <li><a href="#media">Media</a></li>
  </ul>
  <div id="introduction">
    <h2>About Brown Bears</h2>
    <p>The brown bear (<em>Ursus arctos</em>) is native to parts of northern Eurasia and North America. Its conservation status is currently <strong>Least Concern</strong>.<br /><br /> There are many subspecies within the brown bear species, including the
      Atlas bear and the Himalayan brown bear.</p>
    <a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank">Learn More</a>
    <h3>Species</h3>
    <ul>
      <li>Arctos</li>
      <li>Collarus</li>
      <li>Horribilis</li>
      <li>Nelsoni (extinct)</li>
    </ul>
    <h3>Features</h3>
    <p>Brown bears are not always completely brown. Some can be reddish or yellowish. They have very large, curved claws and huge paws. Male brown bears are often 30% larger than female brown bears. They can range from 5 feet to 9 feet from head to toe.</p>
  </div>
  <div id="habitat">
    <h2>Habitat</h2>
    <h3>Countries with Large Brown Bear Populations</h3>
    <ol>
      <li>Russia</li>
      <li>United States</li>
      <li>Canada</li>
    </ol>
    <h3>Countries with Small Brown Bear Populations</h3>
    <p>Some countries with smaller brown bear populations include Armenia, Belarus, Bulgaria, China, Finland, France, Greece, India, Japan, Nepal, Poland, Romania, Slovenia, Turkmenistan, and Uzbekistan.</p>
  </div>
  <div id="media">
    <h2>Media</h2>
    <a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank"><img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg"/></a>
    <video src="https://content.codecademy.com/courses/freelance-1/unit-1/lesson-2/htmlcss1-vid_brown-bear.mp4" height="240" width="320" controls>Video not supported</video>
  </div>
</body>

</html>

*Espaço em branco*

O restante desta lição se concentrará em algumas ferramentas que os desenvolvedores usam para tornar o código mais fácil de interpretar.

À medida que o código em um arquivo HTML cresce, fica cada vez mais difícil acompanhar como os elementos estão relacionados. Os programadores usam duas ferramentas para visualizar a relação entre os elementos: espaço em branco e recuo .

Ambas as ferramentas tiram vantagem do fato de que a posição dos elementos em um navegador é independente da quantidade de espaço em branco ou recuo no arquivo index.html .

Por exemplo, se você quiser aumentar o espaço entre dois parágrafos em sua página da Web, não poderá fazer isso adicionando espaço entre os elementos de parágrafo no arquivo index.html . O navegador ignora espaços em branco em arquivos HTML quando renderiza uma página da Web, para que possa ser usado como uma ferramenta para tornar o código mais fácil de ler e seguir.

O que torna o exemplo abaixo difícil de ler?

<body><p>Paragraph 1</p><p>Paragraph 2</p></body>
Você tem que ler a linha inteira para saber quais elementos estão presentes. Compare o exemplo acima com este:

<body>
    <p>Paragraph 1</p>
    <p>Paragraph 2</p>
</body>

Este exemplo é mais fácil de ler, pois cada elemento está em sua própria linha. Enquanto o primeiro exemplo exigia que você lesse toda a linha de código para identificar os elementos, este exemplo facilita a identificação da tag body e dois parágrafos.

Um navegador renderiza os dois exemplos acima da mesma maneira:

Paragraph 1
Paragraph 2

`Exemplo`
<!DOCTYPE html>
<html>

<body>
  <h1>Whitespace</h1>
    <p> Whitespace and indentation make html documents easier to read</p>
</body>

</html>

*Recuo -indentation*

A segunda ferramenta que os desenvolvedores da Web usam para tornar a estrutura do código mais fácil de ler é a indentação . Os espaços são inseridos usando as barras space e no teclado.tab

O World Wide Web Consortium [](https://www.w3.org/Consortium/), ou W3C, é responsável por manter os padrões de estilo do HTML. No momento da escrita, o W3C recomenda 2 espaços de recuo ao escrever código HTML. Embora seu código funcione sem exatamente dois espaços, esse padrão é seguido pela maioria dos desenvolvedores web profissionais. A indentação é usada para visualizar facilmente quais elementos estão aninhados em outros elementos.

<body>
  <p>Paragraph 1</p>
  <div>
    <p>Paragraph 2</p>
  </div>
</body>

No exemplo acima, Paragraph 1 e a <div> tag está aninhada dentro da <body> tag, então elas são recuadas em dois espaços. O Paragraph 2 elemento está aninhado dentro da <div>tag, portanto, é recuado dois espaços adicionais.

`Exemplo`
<body>
  <h1>Whitespace</h1>    
  <div>
    <p>Whitespace and indentation make html documents easier to read.</p>
  </div>  
</body>

*Comentários*

Os arquivos HTML também permitem que você adicione comentários ao seu código.

Os comentários começam com <!--e terminam com -->. Quaisquer caracteres intermediários serão ignorados pelo seu navegador.

<!-- This is a comment that the browser will not display. -->
Incluir comentários em seu código é útil por vários motivos:

Eles ajudam você (e outras pessoas) a entender seu código se você decidir voltar e revisá-lo muito mais tarde.
Eles permitem que você experimente um novo código, sem precisar excluir o código antigo.
<!-- Favorite Films Section -->
<p>The following is a list of my favorite films:</p>
Neste exemplo, o comentário é usado para indicar que o texto a seguir compõe uma seção específica da página.

<!-- <p> Test Code </p> -->
No exemplo acima, um elemento HTML válido (um elemento de parágrafo) foi "comentado". Essa prática é útil quando há um código que você deseja experimentar ou ao qual deseja retornar no futuro.

`Exemplo`
<!DOCTYPE html>
<!-- <html> 
  <head>
    <title>Favorite Quotes</title>
  </head>
  <body>
    <p>Feet, what do I need you for when I have wings to fly?</p>
    <p>- Frida Kahlo</p>
  </body>
</html> -->

*Tags HTML*

Agora você conhece todos os elementos básicos e a configuração necessária para estruturar uma página HTML e adicionar diferentes tipos de conteúdo. Com a ajuda do CSS, muito em breve você estará criando belos sites!

Embora algumas tags tenham um propósito muito específico, como tags de imagem e vídeo, a maioria das tags é usada para descrever o conteúdo que elas cercam, o que nos ajuda a modificar e estilizar nosso conteúdo posteriormente. Há um número aparentemente infinito de tags para usar (muito mais do que ensinamos). Saber quando usar cada um é baseado em como você deseja descrever o conteúdo do seu HTML. Tags descritivas e bem escolhidas são uma chave para o desenvolvimento web de alta qualidade. Uma lista completa de tags HTML disponíveis pode ser encontrada na documentação do Mozilla .[](https://developer.mozilla.org/en-US/docs/Web/HTML)

Vamos rever o que você aprendeu nesta lição:

A <!DOCTYPE html>declaração deve ser sempre a primeira linha de código em seus arquivos HTML. Isso permite que o navegador saiba qual versão do HTML esperar.

O <html>elemento conterá todo o seu código HTML.

As informações sobre a página da Web, como o título, pertencem <head>à página.

Você pode adicionar um título à sua página da Web usando o <title>elemento, dentro do cabeçalho.

O título de uma página da Web aparece na guia de um navegador.

As tags de âncora ( <a>) são usadas para vincular a páginas internas, páginas externas ou conteúdo na mesma página.

Você pode criar seções em uma página da Web e pular para elas usando <a>tags e adicionando ids aos elementos para os quais deseja pular.

O espaço em branco entre os elementos HTML ajuda a facilitar a leitura do código sem alterar a forma como os elementos aparecem no navegador.

A indentação também ajuda a tornar o código mais fácil de ler. Isso torna as relações pai-filho visíveis.

Os comentários são escritos em HTML usando a seguinte sintaxe: <!-- comment -->.


**TABELAS HTML**

*Criar uma tabela*

Antes de exibir os dados, devemos primeiro criar a tabela que conterá os dados usando o <table>elemento.

<table>
 
</table>

O <table> elemento conterá todos os dados tabulares que planejamos exibir.

`Exemplo`
<!DOCTYPE html>
<html>
<head>
  <title>Ship To It - Company Packing List</title>
  <link href="https://fonts.googleapis.com/css?family=Lato: 100,300,400,700|Luckiest+Guy|Oxygen:300,400" rel="stylesheet">
  <link href="style.css" type="text/css" rel="stylesheet">
</head>
<body>

  <ul class="navigation">
    <li><img src="https://content.codecademy.com/courses/web-101/unit-9/htmlcss1-img_logo-shiptoit.png" height="20px;"></li>
    <li class="active">Action List</li>
    <li>Profiles</li>
    <li>Settings</li>
  </ul>

  <div class="search">Search the table</div>
<table>

</table>


</body>
</html>

*Linhas da tabela*

Em muitos programas que usam tabelas, a tabela já está predefinida para você, o que significa que ela contém as linhas, colunas e células que conterão os dados . Em HTML, todos esses componentes devem ser criados.

A primeira etapa para inserir dados na tabela é adicionar linhas usando o elemento linha da tabela : <tr>.

<table>
  <tr>
  </tr>
  <tr>
  </tr>
</table>

No exemplo acima, duas linhas foram adicionadas à tabela.

`Exemplo`
<!DOCTYPE html>
<html>
<head>
  <title>Ship To It - Company Packing List</title>
  <link href="https://fonts.googleapis.com/css?family=Lato: 100,300,400,700|Luckiest+Guy|Oxygen:300,400" rel="stylesheet">
  <link href="style.css" type="text/css" rel="stylesheet">
</head>
<body>

  <ul class="navigation">
    <li><img src="https://content.codecademy.com/courses/web-101/unit-9/htmlcss1-img_logo-shiptoit.png" height="20px;"></li>
    <li class="active">Action List</li>
    <li>Profiles</li>
    <li>Settings</li>
  </ul>

  <div class="search">Search the table</div>
<table>
  <tr>
  </tr>        <--> Final da 1 linha 
  <tr>
  </tr>        <--> Final da segunda linha
</table>


</body>
</html>

*Dados da Tabela*

As linhas não são suficientes para adicionar dados a uma tabela. Cada elemento de célula também deve ser definido. Em HTML, você pode adicionar dados usando o elemento de dados da tabela : <td>.

<table>
  <tr>
    <td>73</td>
    <td>81</td>
  </tr>
</table>

No exemplo acima, dois pontos de dados ( 73 e 81) foram inseridos na linha existente. Ao adicionar dois pontos de dados, criamos duas células de dados.

Se a tabela fosse exibida no navegador, mostraria uma tabela com uma linha e duas colunas.

`Exemplo`
<!DOCTYPE html>
<html>
<head>
  <title>Ship To It - Company Packing List</title>
  <link href="https://fonts.googleapis.com/css?family=Lato: 100,300,400,700|Luckiest+Guy|Oxygen:300,400" rel="stylesheet">
  <link href="style.css" type="text/css" rel="stylesheet">
</head>
<body>

  <ul class="navigation">
    <li><img src="https://content.codecademy.com/courses/web-101/unit-9/htmlcss1-img_logo-shiptoit.png" height="20px;"></li>
    <li class="active">Action List</li>
    <li>Profiles</li>
    <li>Settings</li>
  </ul>

  <div class="search">Search the table</div>
<table>
  <tr>
  </tr>
  <tr>
    <td>Greenworks de Adam</td>
    <td>14</td>
    <td>Itens do pacote</td>
  </tr>
</table>


</body>
</html>

*Cabeçalhos de Tabela*

Os dados da tabela não fazem muito sentido sem títulos para descrever o que os dados representam.

Para adicionar títulos a linhas e colunas, você pode usar o elemento de cabeçalho da tabela : <th>.

O elemento de cabeçalho da tabela é usado exatamente como um elemento de dados da tabela, exceto com um título relevante. Assim como os dados da tabela, um cabeçalho de tabela deve ser colocado em uma linha da tabela.

<table>
  <tr>
    <th></th>
    <th scope="col">Saturday</th>
    <th scope="col">Sunday</th>
  </tr>
  <tr>
    <th scope="row">Temperature</th>
    <td>73</td>
    <td>81</td>
  </tr>
</table>

O que aconteceu no código acima?

Primeiro, uma nova linha foi adicionada para conter os três títulos: um título em branco, um Saturday título e um Sunday título. O cabeçalho em branco cria a célula de tabela extra necessária para alinhar os cabeçalhos de tabela corretamente sobre os dados aos quais correspondem.

Na segunda linha, um cabeçalho de tabela foi adicionado como título de linha: Temperature.

Quando renderizado, este código aparecerá semelhante à imagem abaixo:

------------------------------------------------------------
'               '     saturday      '       sunday          '
'---------------'-------------------'-----------------------'
' temperature   '        73         '        81             '
'---------------'-------------------'-----------------------'


Observe, também, o uso do scope atributo, que pode assumir um de dois valores:

row - este valor deixa claro que o título é para uma linha.
col - este valor deixa claro que o cabeçalho é para uma coluna.

O código HTML para tabelas pode parecer um pouco estranho no começo, mas analisá-lo peça por peça ajuda a tornar o código mais compreensível.

`Exemplo`
<!DOCTYPE html>
<html>
<head>
  <title>Ship To It - Company Packing List</title>
  <link href="https://fonts.googleapis.com/css?family=Lato: 100,300,400,700|Luckiest+Guy|Oxygen:300,400" rel="stylesheet">
  <link href="style.css" type="text/css" rel="stylesheet">
</head>
<body>

  <ul class="navigation">
    <li><img src="https://content.codecademy.com/courses/web-101/unit-9/htmlcss1-img_logo-shiptoit.png" height="20px;"></li>
    <li class="active">Action List</li>
    <li>Profiles</li>
    <li>Settings</li>
  </ul>

  <div class="search">Search the table</div>
<table>
  <tr>
    <th scope="col">Company Name</th>
    <th scope="col">Number of Items to Ship</th>
    <th scope="col">Next Action
</th>
  </tr>
  <tr>
    <td>Greenworks de Adam</td>
    <td>14</td>
    <td>Itens do pacote</td>
  </tr>
</table>


</body>
</html>

*Bordas da tabela*

Até agora, as tabelas que você criou foram um pouco difíceis de ler porque não têm bordas.

Em versões mais antigas do HTML, uma borda pode ser adicionada a uma tabela usando o border atributo e definindo-a como um número inteiro. Este inteiro representaria a espessura da borda.

<table border="1">
  <tr>
    <td>73</td>
    <td>81</td>
  </tr>
</table>

O código no exemplo acima está obsoleto , portanto, não o use. Destina-se a ilustrar convenções mais antigas que você pode encontrar ao ler o código de outros desenvolvedores.

O navegador provavelmente ainda interpretará seu código corretamente se você usar o border atributo, mas isso não significa que o atributo deva ser usado.

`Usamos CSS para adicionar estilo a documentos HTML,` porque isso nos ajuda a separar a estrutura de uma página de sua aparência. Você pode aprender mais sobre CSS em nossos cursos de CSS.

Você pode obter o mesmo efeito de borda de tabela usando CSS.

table, td {
  border: 1px solid black;
}

O código no exemplo acima usa CSS em vez de HTML para mostrar as bordas da tabela.

`Exemplo`
<!DOCTYPE html>
<html>
<head>
  <title>Ship To It - Company Packing List</title>
  <link href="https://fonts.googleapis.com/css?family=Lato: 100,300,400,700|Luckiest+Guy|Oxygen:300,400" rel="stylesheet">
  <link href="style.css" type="text/css" rel="stylesheet">
</head>
<body>

  <ul class="navigation">
    <li><img src="https://content.codecademy.com/courses/web-101/unit-9/htmlcss1-img_logo-shiptoit.png" height="20px;"></li>
    <li class="active">Action List</li>
    <li>Profiles</li>
    <li>Settings</li>
  </ul>

  <div class="search">Search the table</div>
<table>
  <tr>
    <th scope="col">Company Name</th>
    <th scope="col">Number of Items to Ship</th>
    <th scope="col">Next Action
</th>
  </tr>
  <tr>
    </tr>
<tr>
  <td>Baker's Bike Shop</td>
  <td>3</td>
  <td>Send Invoice</td>
</tr>
<tr>
  <td>Miss Sally's Southern</td>
  <td>4</td>
  <td>Ship</td>
</tr>
<tr>
  <td>Summit Resort Rentals</td>
  <td>4</td>
  <td>Ship</td>
</tr>
<tr>
  <td>Strike Fitness</td>
  <td>1</td>
  <td>Enter Order</td>
  </tr>
</table>


</body>
</html>

*Colunas de abrangência*

E se a tabela contiver dados que abrangem várias colunas?

Por exemplo, um calendário pessoal pode ter eventos que abrangem várias horas ou até vários dias.

Os dados podem abranger colunas usando o colspan atributo. O atributo aceita um número inteiro (maior ou igual a 1) para indicar o número de colunas que ele abrange.

<table>
  <tr>
    <th>Monday</th>
    <th>Tuesday</th>
    <th>Wednesday</th>
  </tr>
  <tr>
    <td colspan="2">Out of Town</td>
    <td>Back in Town</td>
  </tr>
</table>

No exemplo acima, os dados Out of Townabrangem os cabeçalhos da tabela Mondaye usando o valor (duas colunas). Os dados aparecem apenas sob o título.Tuesday2Back in TownWednesday

`Exemplo`
<!DOCTYPE html>
<html>
<head>
  <title>Ship To It - Company Packing List</title>
  <link href="https://fonts.googleapis.com/css?family=Lato: 100,300,400,700|Luckiest+Guy|Oxygen:300,400" rel="stylesheet">
  <link href="style.css" type="text/css" rel="stylesheet">
</head>
<body>

  <ul class="navigation">
    <li><img src="https://content.codecademy.com/courses/web-101/unit-9/htmlcss1-img_logo-shiptoit.png" height="20px;"></li>
    <li class="active">Action List</li>
    <li>Profiles</li>
    <li>Settings</li>
  </ul>

  <div class="search">Search the table</div>
  
  <table>
    <tr>
      <th>Company Name</th>
      <th>Number of Items to Ship</th>
      <th>Next Action</th>
    </tr>
    <tr>
      <td colspan="2">Adam's Greenworks</td>    
      <td>14</td>
      <td>Package Items</td>
    </tr>
    <tr>
      <td>Davie's Burgers</td>
      <td>2</td>
      <td>Send Invoice</td>
    </tr>
    <tr>
      <td>Baker's Bike Shop</td>
      <td>3</td>
      <td>Send Invoice</td>
    </tr>
    <tr>
      <td>Miss Sally's Southern</td>
      <td>4</td>
      <td>Ship</td>
    </tr>
    <tr>
      <td>Summit Resort Rentals</td>
      <td>4</td>
      <td>Ship</td>
    </tr>
    <tr>
      <td>Strike Fitness</td>
      <td>1</td>
      <td>Enter Order</td>
    </tr>
  </table>


</body>
</html>

*Abrangendo Linhas*

Os dados também podem abranger várias linhas usando o rowspanatributo.

O rowspanatributo é usado para dados que abrangem várias linhas (talvez um evento continue por várias horas em um determinado dia). Ele aceita um número inteiro (maior ou igual a 1) para denotar o número de linhas que abrange.

<table>
  <tr> <!-- Row 1 -->     
    <th></th>
    <th>Saturday</th>
    <th>Sunday</th>
  </tr>
  <tr> <!-- Row 2 -->
    <th>Morning</th>
    <td rowspan="2">Work</td>
    <td rowspan="3">Relax</td>
  </tr>
  <tr> <!-- Row 3 -->
    <th>Afternoon</th>
  </tr>
  <tr> <!-- Row 4 -->
    <th>Evening</th>
    <td>Dinner</td>
  </tr>
</table>
No exemplo acima, há quatro linhas:

A primeira linha contém uma célula vazia e os dois cabeçalhos de coluna.
A segunda linha contém o Morningcabeçalho da linha, juntamente com Work, que abrange duas linhas abaixo da Saturdaycoluna. A entrada “Relax” abrange três linhas sob a Sundaycoluna.
A terceira linha contém apenas o Afternoontítulo da linha.
A quarta linha contém apenas a Dinnerentrada, já que “Relax” se estende até a célula próxima a ela.

`Exemplo`
<!DOCTYPE html>
<html>
<head>
  <title>Ship To It - Company Packing List</title>
  <link href="https://fonts.googleapis.com/css?family=Lato: 100,300,400,700|Luckiest+Guy|Oxygen:300,400" rel="stylesheet">
  <link href="style.css" type="text/css" rel="stylesheet">
</head>
<body>

  <ul class="navigation">
    <li><img src="https://content.codecademy.com/courses/web-101/unit-9/htmlcss1-img_logo-shiptoit.png" height="20px;"></li>
    <li class="active">Action List</li>
    <li>Profiles</li>
    <li>Settings</li>
  </ul>

  <div class="search">Search the table</div>
  
  <table>
    <tr>
      <th>Company Name</th>
      <th>Number of Items to Ship</th>
      <th>Next Action</th>
    </tr>
    <tr>
      <td colspan="2">Adam's Greenworks</td>
      <td>14</td>
      <td>Package Items</td>
    </tr>
    <tr>
      <td rowspan="2">Davie's Burgers</td>
      <td>2</td>
      <td>Send Invoice</td>
    </tr>
    <tr>
      <td>Baker's Bike Shop</td>
      <td>3</td>
      <td>Send Invoice</td>
    </tr>
    <tr>
      <td>Miss Sally's Southern</td>
      <td>4</td>
      <td>Ship</td>
    </tr>
    <tr>
      <td>Summit Resort Rentals</td>
      <td>4</td>
      <td>Ship</td>
    </tr>
    <tr>
      <td>Strike Fitness</td>
      <td>1</td>
      <td>Enter Order</td>
    </tr>
  </table>


</body>
</html>

*Bordas da tabela*

Até agora, as tabelas que você criou foram um pouco difíceis de ler porque não têm bordas.

Em versões mais antigas do HTML, uma borda pode ser adicionada a uma tabela usando o borderatributo e definindo-a como um número inteiro. Este inteiro representaria a espessura da borda.

<table border="1">
  <tr>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
O código no exemplo acima está obsoleto , portanto, não o use. Destina-se a ilustrar convenções mais antigas que você pode encontrar ao ler o código de outros desenvolvedores.

O navegador provavelmente ainda interpretará seu código corretamente se você usar o borderatributo, mas isso não significa que o atributo deva ser usado.

Usamos CSS para adicionar estilo a documentos HTML, porque isso nos ajuda a separar a estrutura de uma página de sua aparência. Você pode aprender mais sobre CSS em nossos cursos de CSS.

Você pode obter o mesmo efeito de borda de tabela usando CSS.

table, td {
  border: 1px solid black;
}
O código no exemplo acima usa CSS em vez de HTML para mostrar as bordas da tabela.

  <tr>
    <td>Davie's Burgers</td>
    <td>2</td>
    <td>Send Invoice</td>
  </tr>
  <tr>
    <td>Baker's Bike Shop</td>
    <td>3</td>
    <td>Send Invoice</td>
  </tr>
  <tr>
    <td>Miss Sally's Southern</td>
    <td>4</td>
    <td>Ship</td>
  </tr>
  <tr>
    <td>Summit Resort Rentals</td>
    <td>4</td>
    <td>Ship</td>
  </tr>
  <tr>
    <td>Strike Fitness</td>
    <td>1</td>
    <td>Enter Order</td>
  </tr>

Instruções
Vamos precisar de mais alguns dados na tabela. Adicione os seguintes dados à tabela. Certifique-se de colocá-lo após a segunda linha da tabela.

`Exemplo`
<!DOCTYPE html>
<html>
<head>
  <title>Ship To It - Company Packing List</title>
  <link href="https://fonts.googleapis.com/css?family=Lato: 100,300,400,700|Luckiest+Guy|Oxygen:300,400" rel="stylesheet">
  <link href="style.css" type="text/css" rel="stylesheet">
</head>
<body>

  <ul class="navigation">
    <li><img src="https://content.codecademy.com/courses/web-101/unit-9/htmlcss1-img_logo-shiptoit.png" height="20px;"></li>
    <li class="active">Action List</li>
    <li>Profiles</li>
    <li>Settings</li>
  </ul>

  <div class="search">Search the table</div>
  
  <table>
    <tr>
      <th>Company Name</th>
      <th>Number of Items to Ship</th>
      <th>Next Action</th>
    </tr>
    <tr>
      <td colspan="2">Adam's Greenworks</td>
      <td>14</td>
      <td>Package Items</td>
      <td ></td>
    </tr>
    <tr>
  <td>Davie's Burgers</td>
  <td>2</td>
  <td>Send Invoice</td>
</tr>
<tr>
  <td>Baker's Bike Shop</td>
  <td>3</td>
  <td>Send Invoice</td>
</tr>
<tr>
  <td>Miss Sally's Southern</td>
  <td>4</td>
  <td>Ship</td>
</tr>
<tr>
  <td>Summit Resort Rentals</td>
  <td>4</td>
  <td>Ship</td>
</tr>
<tr>
  <td>Strike Fitness</td>
  <td>1</td>
  <td>Enter Order</td>
</tr>
    
  </table>


</body>
</html>

`CONTINUAR DAQUII`





**Revisão**

Elements and Structure
<em> Emphasis Element
The <em> emphasis element emphasizes text and browsers will usually italicize the emphasized text by default.

<p>This <em>word</em> will be emphasized in italics.</p>
HTML
HTML (HyperText Markup Language) is used to give content to a web page and instructs web browsers on how to structure that content.

Element Content
The content of an HTML element is the information between the opening and closing tags of an element.

<h1>Codecademy is awesome! 🙂</h1>
<li> List Item Element
The <li> list item element create list items inside:

Ordered lists <ol>
Unordered lists <ul>
<ol>
  <li>Head east on Prince St</li>
  <li>Turn left on Elizabeth</li>
</ol>
 
<ul>
  <li>Cookies</li>
  <li>Milk</li>
</ul>
<video> Video Element
The <video> element embeds a media player for video playback. The src attribute will contain the URL to the video. Adding the controls attribute will display video controls in the media player.

Note: The content inside the opening and closing tag is shown as a fallback in browsers that don’t support the element.

<video src="test-video.mp4" controls>
  Video not supported
</video>
<ol> Ordered List Element
The <ol> ordered list element creates a list of items in sequential order. Each list item appears numbered by default.

<ol>
  <li>Preheat oven to 325 F 👩‍🍳</li>
  <li>Drop cookie dough 🍪</li>
  <li>Bake for 15 min ⏰</li>
</ol>
<div> Div Element
The <div> element is used as a container that divides an HTML document into sections and is short for “division”. <div> elements can contain flow content such as headings, paragraphs, links, images, etc.

<div>
  <h1>A section of grouped elements</h1>
  <p>Here’s some text for the section</p>
</div>
<div>
  <h1>Second section of grouped elements</h1>
  <p>Here’s some text</p>
</div>
HTML Structure
HTML is organized into a family tree structure. HTML elements can have parents, grandparents, siblings, children, grandchildren, etc.

<body>
  <div>
    <h1>It's div's child and body's grandchild</h1>
    <h2>It's h1's sibling</h2>
  </div>
</body>
Closing Tag
An HTML closing tag is used to denote the end of an HTML element. The syntax for a closing tag is a left angle bracket < followed by a forward slash / then the element name and a right angle bracket to close >.

<body>
  ...
</body>
Attribute Name and Values
HTML attributes consist of a name and a value using the following syntax: name="value" and can be added to the opening tag of an HTML element to configure or change the behavior of the element.

<elementName name="value"></elementName>
<br> Line Break Element
The <br> line break element will create a line break in text and is especially useful where a division of text is required, like in a postal address. The line break element requires only an opening tag and must not have a closing tag.

A line break haiku.<br>
Poems are a great use case.<br>
Oh joy! A line break.
<img> Image Element
HTML image <img> elements embed images in documents. The src attribute contains the image URL and is mandatory. <img> is an empty element meaning it should not have a closing tag.

<img src="image.png">
<h1>-<h6> Heading Elements
HTML can use six different levels of heading elements. The heading elements are ordered from the highest level <h1> to the lowest level <h6>.

<h1>Breaking News</h1>
<h2>This is the 1st subheading</h2>
<h3>This is the 2nd subheading</h3>
...
<h6>This is the 5th subheading</h6>
<p> Paragraph Element
The <p> paragraph element contains and displays a block of text.

<p>This is a block of text! Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
HTML Attributes
HTML attributes are values added to the opening tag of an element to configure the element or change the element’s default behavior. In the provided example, we are giving the <p> (paragraph) element a unique identifier using the id attribute and changing the color of the default text using the style attribute.

<p id="my-paragraph" style="color: green;">Here’s some text for a paragraph that is being altered by HTML attributes</p>
<ul> Unordered List Element
The <ul> unordered list element is used to create a list of items in no particular order. Each individual list item will have a bullet point by default.

<ul>
  <li>Play more music 🎸</li>
  <li>Read more books 📚</li>
</ul>
alt Attribute
An <img> element can have alternative text via the alt attribute. The alternative text will be displayed if an image fails to render due to an incorrect URL, if the image format is not supported by the browser, if the image is blocked from being displayed, or if the image has not been received from the URL.

The text will be read aloud if screen reading software is used and helps support visually impaired users by providing a text descriptor for the image content on a webpage.

<img src="path/to/image" alt="text describing image" />
Unique ID Attributes
In HTML, specific and unique id attributes can be assigned to different elements in order to differentiate between them.

When needed, the id value can be called upon by CSS and JavaScript to manipulate, format, and perform specific instructions on that element and that element only. Valid id attributes should begin with a letter and should only contain letters (a-Z), digits (0-9), hyphens (-), underscores (_), and periods (.).

<h1 id="A1">Hello World</h1>
<body> Body Element
The <body> element represents the content of an HTML document. Content inside <body> tags are rendered on the web browsers.

Note: There can be only one <body> element in a document.

<body>
  <h1>Learn to code with Codecademy :)</h1>
</body>
<span> Span Element
The <span> element is an inline container for text and can be used to group text for styling purposes. However, as <span> is a generic container to separate pieces of text from a larger body of text, its use should be avoided if a more semantic element is available.

<p><span>This text</span> may be styled differently than the surrounding text.</p>
<strong> Strong Element
The <strong> element highlights important, serious, or urgent text and browsers will normally render this highlighted text in bold by default.

<p>This is <strong>important</strong> text!</p>
HTML Element
An HTML element is a piece of content in an HTML document and uses the following syntax: opening tag + content + closing tag. In the code provided:

<p> is the opening tag.
Hello World! is the content.
</p> is the closing tag.
<p>Hello World!</p>
HTML Tag
The syntax for a single HTML tag is an opening angle bracket < followed by the element name and a closing angle bracket >. Here is an example of an opening <div> tag.

<div>
<a> Anchor Element
The <a> anchor element is used to create hyperlinks in an HTML document. The hyperlinks can point to other webpages, files on the same server, a location on the same page, or any other URL via the hyperlink reference attribute, href. The href determines the location the anchor element points to.

<!-- Creating text links -->
<a href="http://www.codecademy.com">Visit this site</a>
 
<!-- Creating image links -->
<a href="http://www.codecademy.com">
    <img src="logo.jpg">Click this image
</a>
<head> Head Element
The <head> element contains general information about an HTML page that isn’t displayed on the page itself. This information is called metadata and includes things like the title of the HTML document and links to stylesheets.

<!DOCTYPE html>
<html>
  <head>
    <!-- Metadata is contained in this element-->
  </head>
</html>
<target> Target Attribute
The target attribute on an <a> anchor element specifies where a hyperlink should be opened. A target value of "_blank" will tell the browser to open the hyperlink in a new tab in modern browsers, or in a new window in older browsers or if the browser has had settings changed to open hyperlinks in a new window.

<a href="https://www.google.com" target="_blank">This anchor element links to google and will open in a new tab or window.</a>
Indentation
HTML code should be formatted such that the indentation level of text increases once for each level of nesting.

It is a common convention to use two or four space per level of nesting.

<div>
  <h1>Heading</h1>
 
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
  </ul>
</div>
Link to a Different Part of the Page #
The anchor element <a> can create hyperlinks to different parts of the same HTML document using the href attribute to point to the desired location with # followed by the id of the element to link to.

<div>
  <p id="id-of-element-to-link-to">A different part of the page!</p>
</div>
 
<a href="#id-of-element-to-link-to">Take me to a different part of the page</a>
<html> HTML Element
The <html> element, the root of an HTML document, should be added after the !DOCTYPE declaration. All content/structure for an HTML document should be contained between the opening and closing <html> tags.

<!DOCTYPE html>
<html>
  <!-- I'm a comment -->
</html>
Comments
In HTML, comments can be added between an opening <!-- and closing -->. Content inside of comments will not be rendered by browsers, and are usually used to describe a part of code or provide other details.

Comments can span single or multiple lines.

<!-- Main site content -->
<div>Content</div>
 
<!--
  Comments can be 
  multiple lines long.
-->
Whitespace
Whitespace, such as line breaks, added to an HTML document between block-level elements will generally be ignored by the browser and are not added to increase spacing on the rendered HTML page. Rather, whitespace is added for organization and easier reading of the HTML document itself.

<p>Test paragraph</p>
 
<!-- The whitespace created by this line, and above/below this line is ignored by the browser-->
 
<p>Another test paragraph, this will sit right under the first paragraph, no extra space between.</p>
Document Type Declaration
The document type declaration <!DOCTYPE html> is required as the first line of an HTML document. The doctype declaration is an instruction to the browser about what type of document to expect and which version of HTML is being used, in this case it’s HTML5.

<!DOCTYPE html>
<title> Title Element
The <title> element contains a text that defines the title of an HTML document. The title is displayed in the browser’s title bar or tab in which the HTML page is displayed. The <title> element can only be contained inside a document’s <head> element.

<!DOCTYPE html>
<html>
  <head>
    <title>Title of the HTML page</title>
  </head>
</html>
File Path
URL paths in HTML can be absolute paths, like a full URL, for example: https://developer.mozilla.org/en-US/docs/Learn or a relative file path that links to a local file in the same folder or on the same server, for example: ./style.css. Relative file paths begin with ./ followed by a path to the local file. ./ tells the browser to look for the file path from the current folder.

<a href="https://developer.mozilla.org/en-US/docs/Web">The URL for this anchor element is an absolute file path.</a>
 
<a href="./about.html">The URL for this anchor element is a relative file path.</a>