# 1- Iniciando projeto



Já temos o cadastro da conta e configuramos o idioma da ferramenta para o português. Agora, vamos começar a entender o que são os comandos que estão no campo à esquerda, dentro do editor de código do  `p5.js`.

Mesmo após definir a linguagem para o  **“Português”**  a área de código, à esquerda da tela, permanece em  **“Inglês”**. Isso acontece pois os códigos em linguagens de programação não podem ser traduzidos. Eles sempre devem estar em inglês para que o computador entenda.

```scss
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}

```

## Função  `setup()`

Na primeira linha, temos a  **função**  chamada  `setup()`. Podemos traduzir  **setup**  como  **”configurar”**. Neste contexto, é a função que inicializa o código. É aqui que definimos o que deve acontecer primeiro.

```csharp
function setup() {

```

> A função  `setup()`  roda primeiro que as outras funções do código e executa o que tiver dentro dela apenas uma vez.

Na segunda linha podemos identificar que a função inicializa um  _canvas_  de 400 por 400, com o código:  `createCanvas(400, 400);`.

```scss
function setup() {
  createCanvas(400, 400);
}

```

Clicando no botão  **Executar**, no canto superior esquerdo, podemos testar o código. Ele irá desenhar um quadrado ao lado, com o tamanho de 400 de largura e 400 de altura, conforme o código.

O primeiro  _parâmetro_  dentro dos parênteses é sempre a largura (**x**), enquanto o segundo representa a altura (**y**).

```scss
  createCanvas(x, y);

```

Podemos modificar esses valores, por exemplo, para  `createCanvas(600, 400);`. Ao testar, veremos um quadrado com a largura maior. Faça mais testes com outros valores e veja como o quadro muda.

> Nosso exemplo seguirá com os valores originais, mas você pode usar os valores que gostar mais.

## Conhecendo a função  `draw()`

No segundo bloco de código, temos a  **função**  `draw()`. Em português, a tradução seria  **”desenhar”**. Ou seja, todos os códigos de formas que serão desenhadas na tela para formar a nossa imagem, ficarão na  **função**  `draw()`.

```csharp
function draw() {

```

Veja que as duas funções (draw e setup) possuem  **chaves**  (`{}`) abrindo logo após o nome e fechando ao final. Isso é muito importante para que o computador entenda onde cada uma começa e termina.

```scss
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
}

```

> As  **chaves**  (`{}`) dentro da linguagem  **JavaScript**  definem o  _escopo_  das funções, assim como em várias outras linguagens. Esse  _escopo_  é um espaço determinado para que os códigos se organizem dentro de cada função e podem ser aumentados de acordo com a necessidade de cada programa.

Dentro das  **chaves**  da  **função**  `draw()`, temos o código  `background(220);`. Ele representa uma tela que será desenhada com uma  **cor de fundo 220**. O parâmetro de cor também pode ser alterado, experimente. Falaremos mais sobre parâmetros de cor e como conseguir mais cores em breve.

```scss
function draw() {
  background(220);
}

```

Vamos criar uma nova linha, dentro da  **função**  `draw()`, clicando ao final da linha 6 e teclando  **enter**. Lembre-se de deixar a  **chave**  que encerra a função sempre no final do código.

![alt text: O gif apresenta a área de código do p5.js, localizada à esquerda da tela, com um fundo cinza e o código inicial pré-estabelecido pela plataforma.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF1g.1.gif)

Nessa linha nova vamos criar nossa primeira forma, que será um círculo para fazer o rosto do personagem. Como o código deve ser escrito em  _inglês_, escreveremos  `circle()`.

Seguindo as regras da linguagem  **JavaScript**, no  **p5.js**, sempre que um código fica em negrito e azul, precisamos adicionar  **parênteses**  (`()`) ao final do código. Assim como acontece com a  **função**  `draw()`  e  `background()`, a  **função**  `circle()`  deve seguir o mesmo padrão.

No comando  `circle()`, dentro dos  **parênteses**, precisamos adicionar três informações (parâmetros).

> A posição de  **largura**. A posição de  **altura**. O  **diâmetro**, ou seja, o tamanho do círculo.

As duas primeiras informações são  **coordenadas de um plano cartesiano**:  `x`  e  `y`. A terceira informação será o  **diâmetro**. Sendo assim, a função ficaria como:  `circle(x, y, d)`, sempre separando cada valor por um  **vírgula**  (`,`).

Vamos adicionar os valores de  **largura**  e  **altura**  como  `200`, para que fique no centro do  `createCanvas()`, que é  `400`. Para o  **diâmetro**, vamos usar um valor um pouco menos que o total, para que fique dentro a área pintada pelo canvas. Pode ser  `300`.

> Lembre-se de adicionar o  **ponto e vírgula**  (`;`) ao final da linha da função.

Feito isso, seu código ficará como o indicado abaixo:

```scss
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  circle(200,200,300);
}

```

> Se o seu canvas for diferente, tente usar sempre a metade de cada valor. Por exemplo, para um  `createCanvas(600,400)`, podemos usar  `circle(300, 200, 300)`.

Feito isso, podemos executar o código. Teremos um círculo branco com borda preta à direita, na seção “Prévia”.

![Captura de tela do navegador na página do projeto, mostrando o código à esquerda e a “Prévia”, à direita. Na imagem gerada, vemos um fundo quadrado em cinza claro, com um círculo de borda preta e preenchido em branco, posicionado no meio da área cinza.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF1.1.png)

## Explorando outros comandos

Talvez você queira explorar outras formas geométricas e, em vez de um círculo, fazer um quadrado, triângulo ou retângulo. Existem várias possibilidades.

Para conhecer mais sobre essas possibilidades, podemos clicar no botão  **”Ajuda”**  no menu superior. Depois, clique em  **”Referência”**.

![Captura de tela do navegador na página do projeto. No topo da imagem, temos o menu superior com as opções: “Arquivo”, “Editar”, “Esboço” e “Ajuda”. A opção ”Ajuda” está selecionada e, em destaque no submenu, o botão “Referência”. Na parte inferior da imagem, temos o código do projeto.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF1.2.png)

Uma nova página se abrirá. Novamente, temos uma página em inglês. Na parte superior esquerda, temos a opção de alterar a linguagem, porém, não temos a opção para o português.

Desta vez, podemos usar a  **tradução do navegador**. No  **google Chrome**, basta clicar em “Traduzir esta página” no canto direito da barra de navegação. Desta forma, conseguimos traduzir todo o código, inclusive os nomes dos comandos. Precisamos ter cuidado com isso!

![ Captura de tela do navegador na página do projeto. No canto esquerdo da página, temos o título “p5.js” em negrito. Abaixo do título, algumas opções: “Referência”, “Tutoriais”, “Exemplos”, “Contribuir”, “Comunidade”, “Sobre”, “Comece a codificar”, “Doar”, “Pular para”, “Forma”, “Cor”, “Tipografia”, “Imagem”, “Transformar”. No centro da página temos o título “Referência” e abaixo dele a frase “Encontre explicações fáceis para cada parte do código p5”. No canto superior direito, uma seta vermelha indica o botão de “tradução do navegador” e um quadro vermelho destaca o idiomo “Portuguese”.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF1.3.png)

Encontre o nome do comando  `círculo()`, na área de  **Primitivos 2D**. Veja que o comando também foi traduzido para o português.

Clicando no comando, vamos para uma página com uma breve explicação e alguns exemplos. Note que o comando não estará traduzido nos exemplos, pois o código não pode ser traduzido.

> **Lembre-se!**  Não traduzimos os comandos nos códigos, mas para ler e entender o que significa cada um deles, podemos usar o recurso de tradução automática do navegador.

Um pouco mais abaixo nesta página, encontramos o  **sintaxe**  do comando:

```scss
circle(x, y, d)

```

Conforme visto anteriormente,  `circle()`  recebe os parâmetros  `x`,  `y`  e  `d`.

De volta à página de referência, podemos procurar por outros exemplos de formas geométricas. Temos, por exemplo, a  **elipse**  (`ellipse()`), o  **retângulo**  (`rect()`), entre vários outros comandos. Recomendamos que você explore essa documentação!

> Na página de desenvolvimento do código, se aplicarmos a tradução do navegador, a linguagem de programação no bloco de código também será traduzida, o que não pode acontecer. Não podemos traduzir uma linguagem de programação, ou seja, não podemos traduzir nenhuma linha de código do JavaScript, pois ele foi programado em inglês. Sendo assim, podemos manter o idioma da página como "inglês". A única opção que podemos manter como idioma "Português" é no menu suspenso da parte superior direita, onde temos vários outros idiomas. Dessa forma, todos os comandos de menus, como "Arquivo", "Editar", "Esboço" e "Ajuda", estão traduzidos, mas o código continua em inglês.

## Adicionando mais círculos para os olhos

Continuando o desenho do nosso personagem, vamos adicionar mais dois círculos para os olhos. Para cada um deles, usaremos novamente o comando  `circle()`. Mas você pode usar as referências e adicionar quadrados ou triângulos, por exemplo. Use a  **criatividade!**

Começaremos criando um olho do lado esquerdo. Para isso, vamos testar alguns valores. Por exemplo: adicionaremos um  `circle()`  com os valores  `150, 150, 60`.

> Dica: para executar o código, você pode clicar no ícone de play (“Executar esboço”) no canto superior esquerdo, ou usar o atalho de teclado “**Ctrl + Enter**”.

Execute o código e veja o desenho se formar. Se não gostar do resultado, mude os valores até que fique satisfeito.

Em seguida, adicionaremos o olho direito. Para isso, basta adicionar outro comando  `circle()`, recebendo os mesmo parâmetros, mas com valores diferentes. Se queremos o círculo mais para a direita, o primeiro valor (`x`), deverá ser maior. Vamos testar com  `250`.

Como os olhos devem ter a mesma altura, vamos manter o valor de  `y`  como  `150`. Seguindo essa lógica, queremos o mesmo tamanho de  `60`  para o  **diâmetro**.

```scss
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  circle(200,200,300);
  circle(150,150,60);
  circle(250,150,60);
}

```

Ao executar, temos dois círculos menores representando os olhos, dentro de um círculo maior representando o rosto. Experimente outros valores e teste os comandos até encontrar o valor ideal para posicionar cada elemento do seu desenho.

> Antes de finalizar, lembre-se de  **salvar o projeto**, clicando na opção “**Arquivo**”, no menu superior e depois em  **”Salvar**”. Ou use o atalho de teclado “**Ctrl + S**”.

Na próxima aula, pensaremos qual será a forma geométrica que precisamos para continuar o desenho!

# 2- Desenhando mais formas geométricas



Olá estudante!

Vamos continuar o projeto iniciado na aula anterior.

## Abrindo o projeto

Para iniciar, abra o navegador e, na barra de navegação, digite:  `editor.p5js.org`  e tecle  **enter**.

> p5.js Web Editor

Ao acessar o site, veremos o código padrão, sem os comandos que fizemos na aula anterior. Para voltar ao projeto, precisamos entrar na conta que criamos.

No canto superior direito da tela, clique em  **Log in**  (**Entrar**, se o site já estiver em português), digite seu nome de usuário, a senha e clique no botão abaixo para  **Log in**  (**Entrar**).

Após voltar para a página do projeto, podemos ver o nome de usuário no canto superior direito. Clique nele e depois em  **”Meus Esboços”**.

![Captura de tela do navegador na página do p5.js. A linguagem “Português” está selecionada. Temos um menu com o título “Olá, startmarcelo!”. Logo abaixo, as opções: “Meus Esboços”, “Minhas Coleções”, “Meus Recursos” e “Configuração”. A opção “Meus Esboços” está selecionada.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF2.1.png)

Na página de esboços encontraremos o projeto salvo na última aula com um nome aleatório. Clique nele para encontrar seu código. Faça um teste e confira se o projeto funciona, clicando no botão de  **“Play”**  que está logo acima do código.

Próximo ao botão de  **“Play”**  você encontrará o nome do projeto, que está com o nome aleatório criado pelo site.

![Captura de tela do navegador na página do p5.js onde vemos o nome do projeto. Está escrito: “Merciful wallaby por startmarcelo”.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF2.2.png)

Clique no nome para renomeá-lo e digite o nome que preferir. No exemplo, vamos chamá-lo de  **“Monalisa”**.

![Captura de tela do navegador na página do p5.js onde vemos o nome do projeto. Está escrito: “Monalisa por startmarcelo”.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF2.3.png)

## Adicionando novos elementos visuais

Vamos continuar desenhando o rosto do nosso personagem.

Podemos, por exemplo, adicionar uma  **boca**. Vamos usar o comando  `line()`, que significa  **”linha”**. O comando  `line()`  recebe  **quatro parâmetros**, ou seja, quatro números dentro dos parênteses.

> Para mais detalhes e exemplos de como funciona o comando, vá até o botão  **”Ajuda”**  no menu superior. Depois, clique em  **”Referência”**, como vimos na primeira aula.

Para desenhar essa linha, precisamos indicar 2 pontos dentro do plano cartesiano. Por isso, vamos digitar o comando  `line()`  e digitar 4 valores dentro dos parênteses, sempre separados por vírgula (`,`), apenas para teste. Por exemplo:

```scss
function draw() {
    background(220);
    circle(200, 200, 300);
    circle(150, 150, 60);
    circle(250, 150, 60);
    line(300, 150, 300, 250);
}

```

Esses valores farão uma linha, mas não é onde deveria ficar a boca. Para ajudar a encontrar os pontos corretos, vamos criar uma funcionalidade que consiga nos mostrar os valores de  `x`  e  `y`  quando clicarmos na tela com o mouse.

Ainda dentro da função  `draw()`, vamos adicionar o comando  `if()`  seguido de parênteses e chaves. Veja a estrutura:

```scss

if() {

}

```

> O termo  `if`  significa  **”se”**, em português.  **Se**  algo for verdadeiro, faça isso.  **Se**  for falso, não faz nada.

Dentro dos parênteses do  `if`, vamos adicionar o comando  `mouseIsPressed`  com as letras  **”I”**  e  **”P”**  maiúsculas. Esse comando significa que o mouse está pressionado.

O comando  `mouseIsPressed`  deve ficar com um tom de vermelho ou rosa, significando que o p5.js entendeu. Se ele não ficar com esse tom, confira se foi escrito corretamente, sem espaços e com todas as letras maiúsculas e minúsculas corretamente.

```scss
function draw() {
    background(220);
    circle(200, 200, 300);
    circle(150, 150, 60);
    circle(250, 150, 60);
    line(300, 150, 300, 250);
    
    if (mouseIsPressed) {

    }
}

```

Queremos que, ao clicar com o mouse, o site nos mostre a posição desse clique em coordenadas (`x, y`). Para isso, temos o comando  `console.log()`.

Dentro dos parênteses desse comando, vamos adicionar os parâmetros do mouse para  `x`  e para  `y`.

```scss
function draw() {
    background(220);
    circle(200, 200, 300);
    circle(150, 150, 60);
    circle(250, 150, 60);
    line(300, 150, 300, 250);
    
    if (mouseIsPressed) {
        console.log(mouseX, mouseY);
    }
}

```

> Lembre-se de finalizar a linha com  `;`.

> > As linhas que começam com  `function`  e a linha do  `if`  não recebem o  `;`  pois não são linhas de execução de comando.

Podemos executar o código e, ao clicar com o mouse em uma posição dentro do canvas (área cinza), aparecerão dois valores na área do  **”Terminal”**, abaixo do código.

> Caso o seu terminal não esteja visível, procure por um botão com uma “seta” para cima no rodapé do site.

Agora, vamos escolher o ponto inicial e o ponto final onde queremos que a boca seja desenhada. Precisamos de quatro valores: dois para o ponto inicial e dois para o ponto final.

Estes são os valores que encontramos:

```scss
function draw() {
    background(220);
    circle(200, 200, 300);
    circle(150, 150, 60);
    circle(250, 150, 60);
    line(150, 270, 250, 270);
    
    if (mouseIsPressed) {
        console.log(mouseX, mouseY);
    }
}

```

Quando executamos o código, a linha aparece na horizontal, na parte de baixo do rosto do personagem.

Agora ficou muito mais fácil localizar as posições do plano cartesiano com a ajuda do clique do mouse.

Você pode ajustar a posição da boca, mudando os valores do  `line()`. Se quiser posicioná-la na diagonal, basta colocar o ponto final mais para cima. Por exemplo:

```scss
function draw() {
    background(220);
    circle(200, 200, 300);
    circle(150, 150, 60);
    circle(250, 150, 60);
    line(150, 270, 250, 235);
    
    if (mouseIsPressed) {
        console.log(mouseX, mouseY);
    }
}

```

> Se ainda tiver dificuldades para entender qual número deve mudar, faça experimentos, mudando um dos números e executando o código para ver o resultado!

Explore formas de bocas diferentes e use sua imaginação!

## Desenhando um triângulo para o nariz

Agora, queremos adicionar um  **nariz**  ao rosto. Mais uma vez, vá até a opção  **”Ajuda”**  no menu superior e clique em  **”Referência”**. Podemos encontrar o comando  `triangle()`. Se a sua página estiver traduzida, estará escrito  **triângulo**.

Neste caso, o comando precisa receber  **três pontos**  para desenhar o triângulo. Portanto, precisaremos de  **seis parâmetros**  dentro dos parênteses (duas coordenadas para cada ponto).

Novamente, vamos clicar com o botão do mouse na posição do rosto onde queremos que fique a primeira ponta do triângulo. Quando as coordenadas aparecem no  **Terminal**, vamos clicar mais duas vezes, para ter os valores da segunda e da terceira ponta do triângulo.

No nosso caso, conseguimos os valores  `(200, 180, 170, 220, 220, 220)`.

Não se esqueça de digitar o  **ponto e vírgula**  (`;`) no final da linha.

```scss
function draw() {
    background(220);
    circle(200, 200, 300);
    circle(150, 150, 60);
    circle(250, 150, 60);
    line(150, 270, 250, 270);
    triangle(200, 180, 170, 220, 220, 220);

    if (mouseIsPressed) {
        console.log(mouseX, mouseY);
    }
}

```

Ao executar o código, desenhamos um triângulo no centro do rosto, como se fosse o nariz do personagem. Se precisar fazer algum ajuste, basta alterar os valores, como fizemos com os anteriores, até que o código desenhe tudo do seu jeito.


# 3- Pintando nosso desenho



Agora que já temos as formas iniciais e os principais elementos do personagem, exploraremos algumas opções de cores para dar mais vida ao projeto.

## Adicionando cores ao projeto

Nas aulas anteriores, conhecemos o comando  `background()`, que pinta o fundo do nosso projeto. Esse comando recebe um valor (dentro dos parênteses). Em nosso caso, usamos  `220`  para criar um fundo  **cinza**. Se esse valor for alterado, por exemplo, por  `0`, o fundo ficará  **preto**.

O comando  `background()`  pode receber valores entre  `0`  e  `255`, correspondendo a uma escala que começa no  **preto**  (com  `0`) e vai clareando, passando por tons de  **cinza**, até o  **branco**( com  `255`).

> Qualquer valor acima de  `255`  será interpretado como  **branco**.

Como esses valores só permitem tons de  **cinza**,  **preto**  ou  **branco**, precisamos usar outro tipo de parâmetro para gerar cores variadas. Vamos trabalhar com  **palavras**.

Apagaremos o número e digitaremos  **aspas simples**(`’’`) dentro dos parênteses. Veja que, ao clicar apenas uma vez no botão de aspas, o  **p5.js**  já entende e digita a outra para você. Tome cuidado para não teclar duas vezes e escrever mais de uma vez.

Dentro das  **aspas simples**(`’’`), escreveremos  `orange`  (laranja, em inglês). Ao executar o projeto, o fundo mudará para a cor  **laranja**.

![Gif mostrando parte do código no p5.js. O comando *background(220)* é substituído pelo comando *background(‘orange’)*.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF3g.1.gif)

> A linguagem  **JavaScript**  não faz distinção entre  **aspas simples**  e  **aspas duplas**. Nesse caso, optamos por usar as simples. Apenas tenha certeza de não misturá-las. Mantenha seu código sempre organizado e coeso.

```scss
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background('orange');
  circle(200, 200, 300);
  circle(150, 150, 60);
  circle(250, 150, 60);
  line(150, 270, 250, 235);
  triangle(200, 180, 170, 220, 220, 220);

  if (mouseIsPressed) {
    console.log(mouseX, mouseY);
  }
}

```

![Captura de tela do navegador na página do p5.js mostrando o desenho do projeto. Um círculo grande e branco com as bordas pretas, forma o rosto. Dois círculos menores, brancos e com as bordas pretas formam os olhos. Um triângulo branco com as bordas pretas forma o nariz e uma linha preta da esquerda para a direita forma a boca, levemente inclinada para cima. O fundo, atrás do rosto, está laranja claro.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF3.1.png)

Se observar o código, ao lado da palavra  `’orange’`, apareceu um quadrado na cor  **laranja**. Se clicarmos sobre ele, uma paleta de cores se abrirá, com muitas outras opções de cores e tonalidades que podemos explorar.

![Captura de tela do navegador na página do p5.js mostrando parte do código. Uma seta vermelha indica o quadrado com a cor escolhida que, quando clicado, mostra uma janela com a paleta de cores e muitas opções de cores e tonalidades.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF3.7.png)

Por exemplo, se clicarmos em outro tom de laranja, veremos uma mudança no código. A palavra  `’orange’`  desaparecerá e, no lugar, teremos um código. No meu caso, o código é  `#FF5722`. Se o seu for diferente, não tem problema.

```scss
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background('#FF5722');
  circle(200, 200, 300);
  circle(150, 150, 60);
  circle(250, 150, 60);
  line(150, 270, 250, 235);
  triangle(200, 180, 170, 220, 220, 220);

  if (mouseIsPressed) {
    console.log(mouseX, mouseY);
  }
}

```

> O código  `#FF5722`  representa uma das cores predefinidas, localizada na parte inferior da paleta de cores. Outra forma de representar essa cor é usando os valores  **RGB**  (Red, Green e Blue ou Vermelho, Verde e Azul, em português). Para essa mesma cor, os valores em RGB seriam 'rgb(255,87,34)'.

Ao executar o código, veremos uma mudança na cor de fundo. Vale lembrar que as tonalidades podem ser percebidas de formas diferentes por cada pessoa. Por exemplo, alguém pode considerar essa cor como laranja, enquanto outra pessoa pode vê-la como um vermelho claro.

Para especificarmos uma cor de maneira precisa, usamos esse código com a  **hashtag**  (`#`), conhecida como  **código hexadecimal**.

Dependendo da cor e do tom escolhido, o código mudará. Escolha a cor e a tonalidade que mais lhe agradar!

## Colorindo as formas geométricas

Vamos agora colorir as formas geométricas, como o rosto do personagem.

Primeiro, adicionaremos uma linha logo após o comando  `background()`, pressionando  **Enter**. Nessa linha, antes de todos os comandos de formas, vamos adicionar um novo comando:  `fill()`.

Dentro dos parênteses, com  **aspas simples**, digitamos o nome da cor desejada em inglês, como fizemos com o  `background()`. Desta vez, usaremos  `’blue’`.

```scss
//código escondido

function draw() {
  background('#FF5722');
  fill('blue');
  circle(200, 200, 300);
  circle(150, 150, 60);
  circle(250, 150, 60);
  line(150, 270, 250, 235);
  triangle(200, 180, 170, 220, 220, 220);
    
//código escondido
}

```

> Como da primeira vez, aparecerá um quadrado com a cor escolhida ao lado do nome da cor. Se quiser ajustar a cor usando a paleta, clique no quadrado e selecione a cor de sua preferência.

Ao executar o código novamente, veremos todo o personagem pintado. Todas as formas que desenhamos ficarão da mesma cor, deixando apenas o fundo laranja.

![Captura de tela do navegador na página do p5.js mostrando o desenho do projeto. Um círculo grande e azul com as bordas pretas, forma o rosto. Dois círculos menores, azuis e com as bordas pretas formam os olhos. Um triângulo azul com as bordas pretas forma o nariz e uma linha preta da esquerda para a direita forma a boca, levemente inclinada para cima. O fundo, atrás do rosto, está laranja.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF3.2.png)

Vamos ajustar um pouco o tom da cor azul, como fizemos com o laranja. No meu caso, o código da cor ficou  `#03A9F4`.

Para colorir as outras formas corretamente, adicionaremos outro comando  `fill()`, logo após o primeiro  `circle()`  (o comando que desenha o rosto).

Neste caso, abriremos uma nova linha depois do comando  `circle(200, 200, 300);`, que está na linha 9, pressionando  **Enter**. Na nova linha, digitamos  `fill(‘white’)`  para preencher as outras formas com branco.

```scss
//código escondido

function draw() {
  background('#FF5722');
  fill('#03A9F4');
  circle(200, 200, 300);
  fill('white');
  circle(150, 150, 60);
  circle(250, 150, 60);
  line(150, 270, 250, 235);
  triangle(200, 180, 170, 220, 220, 220);

//código escondido
}

```

Ao executar o código, veremos que os olhos e o triângulo ficaram brancos, mas o rosto permaneceu azul, e o fundo, laranja.

Observe que, sempre que um comando  `fill()`  é adicionado acima de uma forma geométrica, todas as formas que vêm depois desse comando estarão na cor escolhida.

> Na programação, os comandos sempre são lidos em ordem, de cima para baixo. Podemos entender que o comando  `fill()`  seleciona a cor que será usada para preencher a forma geométrica a ser criada, como se estivéssemos escolhendo uma cor com um pincel. Cada vez que digitamos o comando  `fill()`  com uma nova cor, mudamos a cor desse pincel.

Se quisermos escolher a cor do triângulo, por exemplo, para um tom de azul, basta digitar o comando  `fill(‘blue’)`  antes do  `triangle()`  . Desta vez, vou escolher um tom mais escuro de azul. Veja como ficou:

```scss
//código escondido

function draw() {
  background('#FF5722');
  fill('#03A9F4');
  circle(200, 200, 300);
  fill('white');
  circle(150, 150, 60);
  circle(250, 150, 60);
  line(150, 270, 250, 235);
    fill('#3F51B5');
  triangle(200, 180, 170, 220, 220, 220);

//código escondido
}

```

![Captura de tela do navegador na página do p5.js mostrando o desenho do projeto. Um círculo grande e azul claro com as bordas pretas, forma o rosto. Dois círculos menores, brancos e com as bordas pretas formam os olhos. Um triângulo azul com as bordas pretas forma o nariz e uma linha preta da esquerda para a direita forma a boca, levemente inclinada para cima. O fundo, atrás do rosto, está laranja.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF3.3.png)

Dessa forma, podemos explorar diversas cores e tonalidades para cada forma geométrica no desenho.

# 4-  Adicionando mais formas geométricas

Adicionaremos mais alguns detalhes ao projeto. Por exemplo, para adicionar uma sobrancelha, podemos usar o nosso  `if`  para coletar as coordenadas no plano cartesiano, como fizemos anteriormente, e desenhar uma linha sobre os olhos, uma para cada olho.

Clicando de um lado e do outro, um pouco acima do olho esquerdo, encontrei os valores  `(123, 115, 178, 113)`. Encontre os valores que funcionem melhor para o seu personagem.

> Lembre-se: o comando  `line()`  deve receber dois pontos - o ponto inicial e o ponto final da linha. Portanto, são necessários quatro valores:  `x`  e  `y`  para o primeiro ponto e, novamente,  `x`  e  `y`  para o segundo ponto.

Agora, abaixo da linha  `triangle()`, escreveremos o comando  `line()`  com os quatro valores que encontramos no  **Terminal**.

```scss
//código escondido

function draw() {
  background('#FF5722');
  fill('#03A9F4');
  circle(200, 200, 300);
  fill('white');
  circle(150, 150, 60);
  circle(250, 150, 60);
  line(150, 270, 250, 235);
  fill('#3F51B5');
  triangle(200, 180, 170, 220, 220, 220);
  line(123,115,178,113);
    
    if(mouseIsPressed){
        console.log(mouseX,mouseY);
    }
}

```

Ao executar o código, teremos uma sobrancelha criada sobre o olho esquerdo. Repetiremos o processo para fazer a segunda sobrancelha, criando uma nova linha com mais um comando  `line()`, desta vez, com os valores correspondentes ao olho direito.

```scss
//código escondido

function draw() {
  background('#FF5722');
  fill('#03A9F4');
  circle(200, 200, 300);
  fill('white');
  circle(150, 150, 60);
  circle(250, 150, 60);
  line(150, 270, 250, 235);
  fill('#3F51B5');
  triangle(200, 180, 170, 220, 220, 220);
  line(123,115,178,113);
  line(225,116,279,106);
    
    if(mouseIsPressed){
        console.log(mouseX,mouseY);
    }
}

```

![Captura de tela do navegador na página do p5.js mostrando o desenho do projeto. Um círculo grande e azul claro com as bordas pretas, forma o rosto. Dois círculos menores, brancos e com as bordas pretas formam os olhos. Acima dos olhos, duas linhas horizontais e pretas, uma para cada olho, formam as sobrancelhas. Um triângulo azul com as bordas pretas forma o nariz e uma linha preta da esquerda para a direita forma a boca, levemente inclinada para cima. O fundo, atrás do rosto, está laranja.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF3.4.png)

Agora, adicionaremos as pupilas dos olhos, que estão apenas com o fundo branco.

> As pupilas são as “bolinhas” dos olhos. São pequenas aberturas no centro dos nossos olhos que permitem a entrada de luz, essencial para que possamos enxergar o que está ao nosso redor.

Desta vez, criaremos pequenos círculos dentro de cada olho. Quando criamos o olho esquerdo, usamos as coordenadas  `150,150`. Podemos reutilizar essas coordenadas e apenas diminuir o diâmetro do círculo para criar um círculo menor, centralizado dentro do círculo maior.

```scss
//código escondido

function draw() {
  background('#FF5722');
  fill('#03A9F4');
  circle(200, 200, 300);
  fill('white');
  circle(150, 150, 60);
  circle(250, 150, 60);
  line(150, 270, 250, 235);
  fill('#3F51B5');
  triangle(200, 180, 170, 220, 220, 220);
  line(123,115,178,113);
  line(225,116,279,106);
  circle(150, 150, 10);
    
    if(mouseIsPressed){
        console.log(mouseX,mouseY);
    }
}

```

Ao executar o código, vemos a pupila no centro do olho esquerdo. Repetiremos o processo para a pupila do olho direito. Desta vez, as coordenadas são  `250, 150`. Vamos usar o mesmo diâmetro,  `10`. Não se esqueça do  **ponto e vírgula**  (`;`) no final de cada linha de comando.

```scss
//código escondido

function draw() {
  background('#FF5722');
  fill('#03A9F4');
  circle(200, 200, 300);
  fill('white');
  circle(150, 150, 60);
  circle(250, 150, 60);
  line(150, 270, 250, 235);
  fill('#3F51B5');
  triangle(200, 180, 170, 220, 220, 220);
  line(123,115,178,113);
  line(225,116,279,106);
  circle(150, 150, 10);
  circle(250, 150, 10);
    
    if(mouseIsPressed){
        console.log(mouseX,mouseY);
    }
}

```

![Captura de tela do navegador na página do p5.js mostrando o desenho do projeto. Um círculo grande e azul claro com as bordas pretas, forma o rosto. Dois círculos menores, brancos e com as bordas pretas formam os olhos. Acima dos olhos, duas linhas horizontais e pretas, uma para cada olho, formam as sobrancelhas. No centro de cada olho, círculos menores em azul formam as pupilas. Um triângulo azul com as bordas pretas forma o nariz e uma linha preta da esquerda para a direita forma a boca, levemente inclinada para cima. O fundo, atrás do rosto, está laranja.](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF3.5.png)

> As pupilas seguem o último comando de cor, portanto, estão em azul, como o nariz.

> > As sobrancelhas são linhas, como a boca, por isso não possuem preenchimento, apenas o traço preto.

## Organizando o código

Concluímos a arte do nosso projeto! Você também pode criar outras formas, adicionando ainda mais detalhes ao personagem. Neste ponto, já temos muitos comandos, por isso é essencial organizá-lo para manter a clareza na leitura do código.

Para tornar a leitura mais fácil e facilitar futuros ajustes, vamos adicionar  **comentários**  que nos ajudarão a entender o que cada parte do código faz.

Com os comentários, conseguimos documentar informações na nossa própria linguagem (ou em qualquer outra). Para isso, usamos  **duas barras**  (`//`). Podemos adicionar qualquer texto após o uso das  `//`  e o código irá ignorar essa parte.

Por exemplo, sabemos que a primeira forma geométrica que desenhamos foi um círculo para formar o rosto. Podemos escrever  `// rosto`  no final da linha e executar o código. Veremos que nada mudou.

```scss
//código escondido

function draw() {
  background('#FF5722');
  fill('#03A9F4');
  circle(200, 200, 300); // rosto
  fill('white');
  circle(150, 150, 60);
  circle(250, 150, 60);
  line(150, 270, 250, 235);
  fill('#3F51B5');
  triangle(200, 180, 170, 220, 220, 220);
  line(123,115,178,113);
  line(225,116,279,106);
  circle(150, 150, 10);
  circle(250, 150, 10);
    
    if(mouseIsPressed){
        console.log(mouseX,mouseY);
    }
}

```

Não temos nenhum problema, pois qualquer informação após as duas barras fica  **oculta**, como um comentário. Assim, podemos usar as duas barras para identificar todas as partes do rosto.

```scss
//código escondido

function draw() {
  background('#FF5722');
  fill('#03A9F4');
  circle(200, 200, 300); // rosto
  fill('white');
  circle(150, 150, 60); // olho esquerdo
  circle(250, 150, 60); // olho direito
  line(150, 270, 250, 235); // boca
  fill('#3F51B5');
  triangle(200, 180, 170, 220, 220, 220); // nariz
  line(123,115,178,113); // sobrancelha esquerda
  line(225,116,279,106); // sobrancelha direita
  circle(150, 150, 10); // pupila esquerda
  circle(250, 150, 10); // pupila direita
    
    if(mouseIsPressed){
        console.log(mouseX,mouseY);
    }
}

```

> O comando  `//`  pode ser inserido em qualquer parte do código. Mas cuidado! Tudo o que estiver depois das duas barras será ignorado pelo computador. Isso significa que, se digitarmos  `//`  na frente de um comando, este comando não será executado.

Esses comentários ajudam a organizar o código, mas não alteram nada no comportamento do projeto.

> Antes de finalizar, lembre-se de  **salvar o projeto**, clicando na opção  **”Arquivo”**, no menu superior e depois em  **”Salvar**”. Ou use o atalho de teclado “**Ctrl + S**”.

![Captura de tela do navegador na página do p5.js mostrando o canto superior esquerdo. O título do editor “p5*” está destacado no canto esquerdo. Ao lado, temos as opções do menu: “Arquivo”, “Editar” e “Esboço”. Uma seta vermelha aponta para a opção “Arquivo”, que está selecionada. Abaixo dela, temos a opção “Novo” e a opção “Salvar”, destacada em vermelho. ](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF3.6.png)


Nesta aula, vamos implementar a pupila que pode seguir o cursor do mouse.

## Utilizando a função  `map()`.

Imagine o seu projeto sendo criado em uma folha de papel ou em uma tela de pintura. Ele poderia ser reproduzido perfeitamente. No entanto, uma coisa que não poderia ser feita é animar o desenho.

Queremos que as pupilas dos dois olhos possam  **”olhar para o cursor do mouse”**, acompanhando a direção do movimento.

A analogia que faremos para construir essa animação é inspirada na  **Monalisa**, de Leonardo da Vinci. Você já ouviu falar dela?

Uma curiosidade sobre essa pintura é justamente a  **ilusão de ótica**  que faz com que a  **Monalisa**  pareça estar sempre olhando para nós, não importa de que ângulo você olhe para ela.

Vamos pensar em como construir isso em nosso projeto?

## Criando uma nova pupila esquerda

O primeiro passo será criar uma  **nova pupila**. Vamos comentar a linha da pupila esquerda, pois essa nova pupila irá substituí-la.

> Adicionar o comando de comentário  `//`  no começo de alguma linha de código é uma prática muito comum na programação, permitindo testar funcionalidades novas sem precisar apagar o código anterior.

Adicionaremos um  `circle()`  abaixo da pupila direita, com as coordenadas  `mouseX`  e  `mouseY`, e o diâmetro  `10`, conforme fizemos anteriormente. Lembre-se de que as letras  `X`  e  `Y`  devem estar  **maiúsculas**.

```scss
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background("#FF5722");
  fill("#03A9F4");
  circle(200, 200, 300); // rosto
  fill("white");
  circle(150, 150, 60); // olho esquerdo
  circle(250, 150, 60); // olho direito
  line(150, 270, 250, 235); // boca
  fill("#3F51B5");
  triangle(200, 180, 170, 220, 220, 220); // nariz
  line(123, 115, 178, 113); // sobrancelha esquerda
  line(225, 116, 279, 106); // sobrancelha direita
  // circle(150, 150, 10); // pupila esquerda
  circle(250, 150, 10); // pupila direita
  circle(mouseX, mouseY, 10); // nova pupila esquerda

  if (mouseIsPressed) {
    console.log(mouseX, mouseY);
  }
}

```

> O  **p5.js**  é capaz de encontrar as coordenadas X e Y do nosso mouse com as variáveis  `mouseX`  e  `mouseY`. Esse código pode não funcionar da mesma forma em outras plataformas.

Ao executar o código, vemos que a pupila segue o mouse. Porém, a ideia é que ela fique no olho e não saia do projeto.

Nesse caso, precisamos trabalhar com um novo  **conceito de programação**.

## Entendendo o conceito de variável

Com o código parado, criaremos uma nova informação para armazenar a nova posição da pupila. Em programação, chamamos isso de  **variável**, ou seja, algo que pode variar ao longo do projeto.

A ideia é que o cursor do mouse pode se mover para qualquer lugar da tela, mas a pupila precisa se mover apenas dentro do olho. Sendo assim, precisaremos  **remapear**  as coordenadas onde o ponto da pupila pode se posicionar. Para isso, usaremos a função  `map()`.

## Usando a função  `map()`  para estabelecer limites

Vamos criar essa nova variável com o nome de  `olhoX`. É importante que ela seja criada  **antes**  do comando que cria a  **nova pupila esquerda**, pois sua posição será usada para criar a nova pupila.

Após definir o nome da variável, atribuímos o valor  `map()`  a ela, usando o sinal de  **igual**  (`=`).

```javascript
function setup() {
  createCanvas(400, 400);
}

function draw() {
  background("#FF5722");
  fill("#03A9F4");
  circle(200, 200, 300); // rosto
  fill("white");
  circle(150, 150, 60); // olho esquerdo
  circle(250, 150, 60); // olho direito
  line(150, 270, 250, 235); // boca
  fill("#3F51B5");
  triangle(200, 180, 170, 220, 220, 220); // nariz
  line(123, 115, 178, 113); // sobrancelha esquerda
  line(225, 116, 279, 106); // sobrancelha direita
  // circle(150, 150, 10); // pupila esquerda
  circle(250, 150, 10); // pupila direita

  olhoX = map();

  circle(mouseX, mouseY, 10); // nova pupila esquerda

  if (mouseIsPressed) {
    console.log(mouseX, mouseY);
  }
}

```

Vamos pular algumas linhas aqui para facilitar a leitura e compreensão do código.

> > Linhas vazias não fazem diferença no código. O computador simplesmente ignora esses espaços e segue para o próximo código.

O  `map()`  vai definir nossa variável, lendo a posição do mouse e limitando a posição da pupila. Para isso, vamos definir as coordenadas que queremos como parâmetros.

Primeiramente, a variável  `mouseX`  pode ir de  `0`, que é o canto esquerdo do projeto, até  `400`, que é o canto direito. Sabemos disso porque criamos o canvas com esse tamanho.

Isso foi feito no começo do projeto, na  **linha 2**, com o comando  `createCanvas(400, 400);`

> Se o seu canvas tiver, por exemplo,  **600**  no eixo  `x`, podemos usar o limite de 600.

Passaremos essas informações para o comando  `map()`:

```go
// código omitido

circle(250, 150, 10); // pupila direita

olhoX = map(mouseX, 0, 400);

circle(mouseX, mouseY, 10); // nova pupila esquerda

// código omitido

```

Agora, precisamos mapear a área limite da pupila. Neste caso, precisamos saber os limites da coordenada  `x`  dentro do olho esquerdo.

Podemos obter essa informação usando o  **clique do mouse**  e analisando as informações no  **Terminal**, como feito anteriormente.

Clique no  **canto esquerdo**  de dentro do  **olho esquerdo**. Ems eguida, clique no  **canto direito**  de dentro do mesmo  **olho esquerdo**.

Fazendo isso, recebemos no  **Terminal**  as coordenadas  `132, 150`  e  `166, 150`. Sabemos que cada clique nos dá duas coordenadas:  `x`  e  `y`. Como estamos mapeando o  `olhoX`, usaremos apenas os valores  `132`  e  `166`, por enquanto.

> Lembre-se de fazer seus próprios testes, pois cada projeto pode ter valores diferentes.

Passando esses valores para a função  `map()`, teremos:

```go
// código omitido

olhoX = map(mouseX, 0, 400, 132, 166);

// código omitido

```

Podemos fazer o mesmo com o valor do  `mouseY`. Logo abaixo de  `olhoX`, vamos declarar  `olhoY = map();`. Desta vez, vamos mapear os valores da coordenada  `y`, ou seja, a altura.

O valor máximo e mínimo já sabemos. São as mesmas proporções definidas no  `createCanvas`. Neste caso, teremos  `mouseY, 0, 400`.

Para os limites da pupila na altura do olho, vamos clicar no  **canto superior, dentro do olho esquerdo**. Depois, mais um clique no  **canto inferior, dentro do olho esquerdo**.

Recebemos os valores  `148, 133`  e  `151, 169`. Desta vez, precisamos apenas dos valores de  `y`, portanto, usaremos  `133`  e  `169`.

```go
// código omitido

olhoX = map(mouseX, 0, 400, 130, 170);
olhoY = map(mouseY, 0, 400, 133, 169);

// código omitido

```

Perceba que ambos os pares de valores, tanto em  `olhoX`  quanto em  `olhoY`, são muito próximos. Sendo assim, podemos simplificar o código e arredondar os valores. Vamos usar  `130`  para o  `x`  e  `170`  para o  `y`.

```go
// código omitido

olhoX = map(mouseX, 0, 400, 130, 170);
olhoY = map(mouseY, 0, 400, 130, 170);

// código omitido

```

Agora, podemos substituir os parâmetros do último  `circle()`, onde criamos a  **nova pupila esquerda**.

Trocamos o  `mouseX`  e o  `mouseY`  pelas  **variáveis**  com o mapeamento que criamos.

```go
// código omitido

olhoX = map(mouseX, 0, 400, 130, 170);
olhoY = map(mouseY, 0, 400, 130, 170);

circle(olhoX, olhoY, 10); // nova pupila esquerda

// código omitido

```

Ao executar o código, a pupila não sai mais do olho, mas segue o cursor do mouse!

## Criando uma nova pupila direita

Finalizando esse processo, precisamos criar a  **nova pupila**  para o  **olho direito**.

Já podemos comentar a criação da  **pupila direita**, pois substituiremos por uma nova.

```cpp
// circle(150, 150, 10); // pupila esquerda
// circle(250, 150, 10); // pupila direita

```

Para criar a  **nova pupila esquerda**, usaremos o mesmo mapeamento que fizemos.

Perceba que a primeira  **pupila esquerda**  que criamos tinha os valores  `150, 150, 10`  para centralizá-la.

A  **pupila direita**  foi criada com valores muito parecidos:  `250, 150, 10`. Portanto, os parâmetros de  `y`  e do diâmetro são  **os mesmo**.

Sendo assim, sabemos que a diferença está apenas no valor da  **coordenada**  `x`, que tem o valor maior em  `100`.

Podemos criar um novo  `circle`  para a  **nova pupila direita**, logo após a linha da  **nova pupila esquerda**, que receberá  `olhoX + 100, olhoY, 10`.

```go
// código omitido

// circle(150, 150, 10); // pupila esquerda
// circle(250, 150, 10); // pupila direita

olhoX = map(mouseX, 0, 400, 130, 170);
olhoY = map(mouseY, 0, 400, 130, 170);

circle(olhoX, olhoY, 10); // nova pupila esquerda
circle(olhoX + 100, olhoY, 10); //nova pupila direita

// código omitido

```

> Se o seu canvas ou a posição dos olhos no seu projeto forem diferentes, talvez seja necessário ajustar esses valores para o seu código.

# Boas práticas na programação

Para finalizar, vamos reforçar uma prática muito importante no desenvolvimento de códigos. As variáveis que criamos (`olhoX`  e  `olhoY`) aparecem no código e fazem o  **mapeamento da posição**  das novas pupilas direita e esquerda.

Porém, é muito melhor para o computador, que essas variáveis sejam  **declaradas antes**. Na maioria dos casos, fazemos isso fora da função, ou seja, entre o  `setup()`  e o  `draw()`.

Para declarar uma variável no  **JavaScript**, escrevemos  `let`, seguido do nome da variável. Faremos isso para as duas variáveis, portanto:

```csharp
function setup() {
  createCanvas(400, 400);
}
let olhoX;
let olhoY;

// código omitido

```

> O que isso significa? Ao declarar uma variável, estamos reservando um espaço na memória do computador, como se uma “caixinha” fosse criada com esse nome. Nesse espaço, os valores do mapeamento da pupila ficarão guardados, podendo ser alterados e lidos durante a função  `draw()`. Isso torna o código mais leve, otimizado e pode evitar alguns problemas de código.

```javascript
function setup() {
  createCanvas(400, 400);
}
let olhoX;
let olhoY;

function draw() {
  background("#FF5722");
  fill("#03A9F4");
  circle(200, 200, 300); // rosto
  fill("white");
  circle(150, 150, 60); // olho esquerdo
  circle(250, 150, 60); // olho direito
  line(150, 270, 250, 235); // boca
  fill("#3F51B5");
  triangle(200, 180, 170, 220, 220, 220); // nariz
  line(123, 115, 178, 113); // sobrancelha esquerda
  line(225, 116, 279, 106); // sobrancelha direita
  // circle(150,150,10); // pupila esquerda
  //circle(250,150,10); // pupila direita

  olhoX = map(mouseX, 0, 400, 130, 170);
  olhoY = map(mouseY, 0, 400, 130, 170);

  circle(olhoX, olhoY, 10); // nova pupila esquerda
  circle(olhoX + 100, olhoY, 10); //nova pupila direita
  if (mouseIsPressed) {
    console.log(mouseX, mouseY);
  }
}

```

Execute seu projeto e veja que as pupilas dos olhos estarão sempre se movendo na direção do cursor do mouse, dentro da área do desenho.

> Antes de finalizar, lembre-se de  **salvar o projeto**, clicando na opção  **”Arquivo”**, no menu superior e depois em  **”Salvar**”. Ou use o atalho de teclado “**Ctrl + S**”.

![Captura de tela do navegador na página do p5.js mostrando o canto superior esquerdo. O título do editor “p5*” está destacado no canto esquerdo. Ao lado, temos as opções do menu: “Arquivo”, “Editar” e “Esboço”. Uma seta vermelha aponta para a opção “Arquivo”, que está selecionada. Abaixo dela, temos a opção “Novo” e a opção “Salvar”, destacada em vermelho. ](http://cdn3.gnarususercontent.com.br/3962-logica-programacao/imagens-atividades/CriandoArteInterativaComp5js-FCF3.6.png)
