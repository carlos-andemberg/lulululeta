# Moldura da câmera da lulululeta 🎀💗

Moldura animada de Madoka pra câmera da [lulululeta](https://www.twitch.tv/lulululeta), feita pra fonte **Navegador** do OBS. O fundo é transparente, e é HTML/CSS/JS puro: sem build e sem dependências.

**No ar:** [lulululeta.carlosandemberg.com.br](https://lulululeta.carlosandemberg.com.br). Lá você escolhe a tela e as opções e copia o link pro OBS. A moldura em si fica em `https://lulululeta.carlosandemberg.com.br/moldura-camera.html`.

| Arquivo | O que é | Tamanho no OBS |
|---|---|---|
| `moldura-camera.html` | Borda rosa com renda, a Soul Gem da Madoka num círculo mágico, o laço vermelho, a fita com o nome descendo pela borda, o Kyubey, rosinhas, penas caindo e a flecha da Madoka | **1920 × 1080** (tela do LoL) ou **545 × 590** (`?solta`, só a câmera) |
| `index.html` | Gerador de link: modelo, nome, posição e tamanho da câmera, quais enfeites entram, quantas penas e o intervalo da flecha. Também mostra a live com a moldura por cima | — |

## A moldura

A borda é rosa, com um filete dourado, o miolo clarinho de coraçõezinhos e uma rendinha branca pra dentro. Um brilho corre por ela de vez em quando.

No canto de cima-esquerdo fica a Soul Gem da Madoka: a gema rosa no engaste dourado, respirando luz, em cima de um círculo mágico que gira devagar. O laço vermelho do cabelo dela fica amarrado atrás da gema, com a ponta deitada na borda de cima. Da gema desce a fita com o nome, **uma letra embaixo da outra**, em [Cherry Bomb One](https://fonts.google.com/specimen/Cherry+Bomb+One), com o corte em V na ponta. Se o nome for comprido demais pra caber assim, ele fica deitado na fita, lendo de baixo pra cima.

Lá embaixo, do lado de fora, o Kyubey fica sentado perto das rosinhas. Ele pisca, balança os fios das orelhas (com os anéis dourados), abana o rabão e inclina a cabeça. De vez em quando solta um **balãozinho**: ／人◕ ‿‿ ◕人＼, Faça um contrato comigo!, Vire uma garota mágica!, Qual é o seu desejo?, Qualquer desejo mesmo!, Só um contratinho..., É só assinar aqui, Não entendo os humanos. Penas cor-de-rosa aparecem com um brilhinho e caem devagar, balançando feito folha, sempre do lado de fora da câmera e longe do painel de itens do LoL.

A cada 30 segundos tem **flecha**. A Madoka aparece no ar, de roupa de garota mágica, em cima de um circulinho mágico do lado do canto: marias-chiquinhas no alto com os laços vermelhos, vestido rosa e branco de babado, sapato vermelho e o arco de galho de roseira com a rosa na ponta. Ela puxa o arco, a ponta da flecha junta luz, e ela solta. A flecha sobe pra esquerda e estoura num coração de luz, como na arte dela, as penas voam pra todo lado e cai uma chuva de flechinhas cor-de-rosa. A Soul Gem acende, o círculo mágico dá uma volta, a fita pula, os enfeites pulam em onda e o Kyubey fala "Contrato fechado!". Depois ela some num brilho.

### A tela do LoL

As medidas saíram da própria live, numa tela 1920 × 1080: câmera em **x 1599, y 781, 321 × 299**, no canto de baixo-direito, encostada nas duas beiradas. Ela fica no mesmo lugar no lobby e na partida.

- A beirada da direita e a de baixo ficam sem borda (a moldura continua pra fora da tela). A borda fica em cima e na esquerda, por dentro da câmera.
- **Em cima da câmera** ficam os retratos dos aliados (de y 690 a 776, de x 1650 pra direita). Nada sobe ali: a borda de cima é fininha e todos os enfeites ficam do lado esquerdo.
- A Madoka, a flecha, as penas e os balões ficam na parte do jogo à esquerda da câmera e nunca entram na frente dela.

### Colocar no OBS (tela do LoL)

1. Na cena do jogo: **Fontes → + → Navegador**
2. **URL**: `https://lulululeta.carlosandemberg.com.br/moldura-camera.html?tela=lol`
3. **Largura 1920, Altura 1080** (o tamanho da tela do OBS). A fonte cobre a tela toda e a moldura cai sozinha em volta da câmera.
4. Na lista de fontes, deixe a moldura **acima** da câmera. Se o lobby e a partida forem cenas diferentes, coloque a mesma fonte nas duas (**Fontes → + → Navegador → Adicionar existente**).

### Só a câmera: pra arrastar junto com a webcam

Com `?solta`, a moldura tem borda **em volta toda**: a Soul Gem no canto de cima-esquerdo, a fita com o nome descendo pela borda da esquerda, o Kyubey sentado em cima da borda de cima, rosinhas nos cantos, a estrelinha na direita e o coração embaixo. Na flecha, a Madoka aparece em cima da borda.

1. **Fontes → + → Navegador**, URL `https://lulululeta.carlosandemberg.com.br/moldura-camera.html?solta`
2. **Largura 545, Altura 590**, pra uma câmera de 321 × 299. Com outro tamanho (`largura=`/`altura=`), o gerador de link mostra o tamanho da fonte.
3. A câmera fica 112 px da esquerda e 220 px do topo da fonte.
4. Selecione a moldura e a câmera → botão direito → **Agrupar itens selecionados**. Daí é só arrastar e redimensionar o grupo.

### Prévia

Abrindo o link num navegador normal aparece um fundo de exemplo, com os retratos dos aliados, a barra de habilidades, os itens e a meta dela de mentirinha, no lugar em que ficam na live. Clique em qualquer lugar pra soltar a flecha. Dentro do OBS o fundo fica transparente.

### Opções no link

Junte com `&`, ex.: `moldura-camera.html?tela=lol&penas=12&flecha=45`.

| Opção | O que faz |
|---|---|
| `tela=lol` | A tela do LoL (o padrão) |
| `solta` | Modelo só da câmera, com borda em volta toda. Usa só `largura`/`altura` |
| `x=1599&y=781` | Canto de cima-esquerdo da câmera, em pixels da tela |
| `largura=321&altura=299` | Tamanho da câmera. Os enfeites crescem ou encolhem junto |
| `resolucao=1280x720` | Tamanho da tela do OBS, se não for 1920 × 1080. Sem `x`/`y`, a posição encolhe junto |
| `nome=Lulu` | Texto da fita (`nome=` sem nada esconde a fita) |
| `penas=12` | Quantas penas caindo (0 a 300; `penas=0` tira as penas) |
| `velocidade=0.6` | Velocidade das penas: `1` é o padrão, `2` é rápido, `0.5` é bem devagar |
| `flecha=45` | Segundos entre uma flecha e outra (`flecha=0` desliga) |
| `madoka=0` | Flecha sem a Madoka: ela sai da Soul Gem |
| `gema=0` | Sem a Soul Gem (e o círculo mágico) |
| `laco=0` | Sem o laço vermelho |
| `kyubey=0` | Sem o Kyubey (os balões saem da fita) |
| `rosas=0` | Sem as rosinhas (e sem a estrelinha e o coração do modelo solto) |
| `falas=0` | Sem os balõezinhos do Kyubey |
| `falas=Oi,Tudo bem?` | Troca as falas (separe com vírgula) |
| `zoom` | Só na prévia: mostra a moldura de pertinho |

**Mudou a câmera de lugar?** No OBS, botão direito na câmera → **Transformar → Editar transformação**. Copie a posição e o tamanho pro gerador de link. O tamanho da tela fica em **Configurações → Vídeo → Resolução base**.

### Personalizar

O resto fica no bloco `CONFIG`, no começo de `moldura-camera.html`: cores, fonte, lugar da câmera, lista de falas, a fala da flecha, grossura da borda e cantos. Edite, salve e faça o deploy de novo. No OBS, botão direito na fonte → **Atualizar**.

## Publicar

São arquivos estáticos, então qualquer hospedagem estática serve.

**Coolify**

1. **Projects → New Resource → Public Repository** (ou **GitHub App**, pra fazer deploy a cada push) e cole a URL deste repositório.
2. **Build Pack**: `Dockerfile` (serve na porta **80**). Em **Health Checks**, ligue o healthcheck no caminho `/`.
3. Defina o domínio e clique em **Deploy**. A moldura fica em `https://SEU-DOMINIO/moldura-camera.html`.

A seção "Em cima da live" do gerador usa o player da Twitch, que só funciona em HTTPS (ou em `localhost`).
