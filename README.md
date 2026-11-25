# Manual do Culto Copilot

O Culto Copilot escuta o culto pelo som da mesa e cuida da projeção junto com você: troca os slides das músicas
no **Holyrics**, põe os versículos que o pregador lê, separa frases marcantes da pregação, monta a transmissão no
**OBS** (letra, versículo, oferta, contagem, câmeras) e pode até ligar a live sozinho. **Quem manda é você**: tudo o
que você fizer no Holyrics ou no OBS tem prioridade, e o Holyrics continua funcionando normalmente mesmo se o
Copilot parar.

> **Tem uma dúvida?** No programa, clique em **Ajuda** (barra lateral): escreva a dúvida, escolha a IA (ChatGPT,
> Claude, Perplexity ou Gemini) e ela abre já com este manual. Também dá para procurar aqui com Ctrl+F. Achou um
> erro ou quer uma melhoria? Use **Relatar** ([seção 17](#17-relatar-um-problema-ou-pedir-uma-melhoria)).
>
> **Para IAs e assistentes:** este é o manual oficial do **Culto Copilot** (programa de projeção para igrejas que
> trabalha com o Holyrics e o OBS). Responda só pelo que está aqui; se não estiver no manual, diga que não encontrou
> e peça para a pessoa usar o botão **Relatar** do programa.

## Índice

1. [Primeira vez](#1-primeira-vez)
2. [Domingo passo a passo](#2-domingo-passo-a-passo)
3. [Domingo sozinho: tudo liga, a live começa e termina sem ninguém](#3-domingo-sozinho-tudo-liga-a-live-começa-e-termina-sem-ninguém)
4. [A janela do programa](#4-a-janela-do-programa)
5. [Louvor](#5-louvor)
6. [Leitura bíblica](#6-leitura-bíblica)
7. [Frases de efeito e artes](#7-frases-de-efeito-e-artes)
8. [Automático, Sugerir e culto de validação](#8-automático-sugerir-e-culto-de-validação)
9. [OBS: letra, versículo, oferta e redes na transmissão](#9-obs-letra-versículo-oferta-e-redes-na-transmissão)
10. [Contagem regressiva e pré-culto](#10-contagem-regressiva-e-pré-culto)
11. [TV da entrada](#11-tv-da-entrada)
12. [Câmeras no OBS e fundo com câmera no telão](#12-câmeras-no-obs-e-fundo-com-câmera-no-telão)
13. [YouTube](#13-youtube)
14. [Fotos do culto](#14-fotos-do-culto)
15. [Celular e tablet](#15-celular-e-tablet)
16. [Transcrição e IA pela internet](#16-transcrição-e-ia-pela-internet)
17. [Relatar um problema ou pedir uma melhoria](#17-relatar-um-problema-ou-pedir-uma-melhoria)
18. [Quando algo dá errado](#18-quando-algo-dá-errado)
19. [Onde fica cada coisa](#19-onde-fica-cada-coisa)

---

## 1. Primeira vez

1. Rode o instalador **CultoCopilot-Setup.exe** no computador da projeção. Ele cria o atalho **Culto Copilot** na
   Área de Trabalho, que abre o **Culto Copilot.exe** da pasta do programa (com o ícone dele; para fixar na barra
   de tarefas: botão direito no atalho › Afixar na barra de tarefas). As atualizações chegam sozinhas depois: ao abrir o programa, a cada 30 min com o sistema
   desligado e a janela fechada ou minimizada, e antes de o sistema ligar sozinho no domingo.
2. Abra o programa. O **tour de boas-vindas** pergunta, em poucas telas:
   - **Quantos computadores cuidam do culto?** Só este, ou mais de um (som, telão e live em computadores
     diferentes). Veja [Vários computadores](#vários-computadores-som-telão-e-live-em-computadores-diferentes).
   - **O que a sua igreja usa?** Se vocês **fazem live** (OBS/YouTube) e se têm uma **TV na porta da igreja**. Sem
     live, o programa não procura o OBS; sem TV, a TV da entrada fica desligada.
   - **Quando são os cultos?** Os dias da semana e o horário do culto principal. A contagem e a TV da entrada só
     aparecem nesses dias.
   - **De onde vem o som do culto?** A entrada de áudio (o som da mesa). Com a mesa ligada no computador por USB
     (multitrack) e o REAPER aberto com o projeto do MixCopilot, escolha **REAPER (multitrack)**: o REAPER manda pela
     rede do próprio computador (ReaStream, faixa "Culto Copilot") a voz limpa dos cantores para as letras e o mic do
     pregador para a Bíblia e as frases, cada um no seu canal, sem a banda por cima.
   - **Conectar o Holyrics**: o token da API (no Holyrics: *Arquivo › Configurações › API Server*).
   - Se você já vê as letras de perto, quanto da projeção o Copilot assume (100% automático ou só sugestões) e se
     vai controlar também pelo celular.
3. Para refazer o tour: **Ajustes › Tour de boas-vindas › Refazer**.

### Vários computadores: som, telão e live em computadores diferentes

Se a igreja já tem um computador com o cabo da mesa de som, outro com o Holyrics no telão e outro com o OBS da live,
o Copilot trabalha com eles do jeito que estão, sem trocar cabo. Instale o Copilot em todos.

1. No computador que vai **emprestar** o que tem (o ajudante): no tour, ou em **Ajustes › Computadores**, escolha
   **Este computador ajuda o principal**. Aparece um **código de 6 números**. Deixe o Copilot aberto ali (pode
   minimizar; ele abre sozinho quando o Windows liga). Se o Windows perguntar sobre a rede, clique em
   **Permitir acesso**.
2. No computador **principal** (onde o Copilot ouve, transcreve e decide): escolha **Este é o principal; outros
   computadores ajudam**, toque em **Procurar computadores** e digite o código do ajudante. Se ele não aparecer,
   digite o endereço dele (aparece embaixo do código) e procure de novo.
3. Em **Quem faz o quê**, diga onde fica cada função:
   - **Som da mesa**: o computador com o cabo da mesa e a entrada de lá. O som chega pela rede e aparece na
     Operação como **Outro computador: nome**.
   - **Projeção (Holyrics e telão)**: o Holyrics de lá mostra letras, versículos e frases. As artes, fotos e fundos
     são copiados para lá sozinhos, e a página do fundo do telão abre na tela do telão de lá. Ligue a API no Holyrics
     de lá e cole o token no principal (**Ajustes › Holyrics**).
   - **Live (OBS)**: o OBS de lá recebe a letra, a contagem, as câmeras e o início e fim da live. Toque de novo em
     **Letra no OBS** e **Contagem no OBS** depois de mudar.
4. Vale a partir do próximo culto ligado.

A transcrição (a parte pesada) roda no principal. O quadro mostra a placa de vídeo de cada computador; se um ajudante
for bem mais forte, ele sugere trocar (o mais forte como principal). Os computadores precisam estar na mesma rede.
O ajudante não se atualiza enquanto o principal usa o som, o Holyrics ou o OBS dele.

Notebook: deixe **no carregador** e num modo de energia **equilibrado** (com bateria gasta, o modo desempenho pode
desligar o computador).

---

## 2. Domingo passo a passo

1. Abra o **Holyrics** e monte a **playlist do culto** com as músicas na ordem (o Copilot lê a playlist sozinho).
   Com **Ajustes › Abrir o Holyrics junto** ligado, o programa abre o Holyrics por você.
2. Abra o **Culto Copilot**, confira a entrada de áudio e clique em **▶ Ligar o sistema**, de preferência bem antes
   do culto: o sistema já pode ficar ligado no pré-culto. Ele confere o Holyrics, o áudio e o resto; o que fica
   pronto sobe e some da lista. Se algo tiver problema, você decide: **Ligar mesmo assim** ou **Cancelar**.
3. Pediram mais tempo antes do culto? Em **Operação › Contagem**, toque **+2 min**, **+5 min** ou **+10 min**. A
   contagem do OBS, do telão e da TV da entrada empurra junto. **Voltar ao horário** desfaz.
4. No fim, clique em **Desligar**. Se fechar a janela com o sistema ligado, ela volta perguntando: **Desligar o
   sistema e fechar** ou **Deixar ligado**.

---

## 3. Domingo sozinho: tudo liga, a live começa e termina sem ninguém

Em **Ajustes › OBS › Contagem e pré-culto** ficam os campos (na Manancial já vêm preenchidos):

| Campo | Exemplo | O que faz |
|---|---|---|
| **Ligar tudo sozinho** | `domingo 08:00` | O Windows abre o programa 2 min antes; na hora o sistema liga (mesma entrada de áudio da última vez) e o OBS abre, para os telões já terem imagem. |
| **Iniciar a live sozinha** | `domingo 10:00` | Põe o OBS na cena do pré-live (com a contagem por cima) e começa a transmitir. Confere se o OBS entrou mesmo no ar. Com a conta do YouTube conectada no OBS (o aviso *"No Broadcast Configured"*), o programa grava a chave da live no OBS e tira a conta de lá (o YouTube do Copilot cuida do título e do chat). |
| **Visibilidade da live** | `pública` | `pública` ou `não listada`: a live já nasce assim no YouTube. O culto de teste é sempre não listada. |
| **Cena do pré-live** | `PRE-LIVE` | Onde a live começa (vídeo e música do pré-live, sem o som da mesa). |
| **Cena do culto** | `CAMERA` | Entra na saudação de abertura: câmera e som da mesa. |
| **Cena do fim** | `FINALIZAR` | Entra na bênção final; a transmissão termina 2 min depois. |
| **Título da live** | `domingo: 🔴MANHÃ DE GLÓRIA - {data} \| {tema} \| CAMNCL` | O título no YouTube; `{data}` vira 15-11 e `{tema}` o tema da pregação. Uma linha sem dia vale para os outros dias. |

Vários horários: separe com `;` (ex.: `domingo 10:00; quarta 19h30`). Vazio = não faz.

Datas com horário próprio ligam sozinhas também fora do dia da semana: **ARCA 57** sexta 18/12 e sábado 19/12 às 20h (tudo liga às 18h) e domingo 20/12 às 10h. O Windows abre o programa nessas datas sozinho.

Como fica o domingo:

1. **8:00**: programa aberto, sistema ligado, OBS aberto, telões com imagem.
2. **10:00**: a live começa no **pré-live**. **Sem sinal de câmera** (tela preta, lisa ou as **barras coloridas** da
   placa), a live **não começa**: chega um aviso no celular e o programa tenta de novo até 10:20, caso a câmera
   chegue atrasada.
3. Passada a hora, a contagem mostra **"Já vai começar"** revezando com os slides.
4. **Saudação de abertura**: quando alguém sobe no altar e cumprimenta a igreja (*"Shalom, shalom"*, *"bom dia,
   igreja"*, *"vamos ficar de pé"*), a contagem cobre a tela com uma cortina com a logo, o OBS troca para a **cena do
   culto** por baixo e a cortina sobe revelando a câmera, já com o som da mesa. Se ninguém for reconhecido, corta
   sozinho 25 min depois da hora (mais os minutos dados no +2/+5/+10).
5. **Fim da live**: a despedida (*"a graça do Senhor Jesus Cristo… comunhão"*, *"Deus abençoe, abraça a pessoa do
   seu lado"*, *"até amanhã"*, junto com *"shalom, shalom"*), só depois de **1h30 de culto**, **arma** o fim. A live
   termina (cena do fim e, 2 min depois, a transmissão para) quando o culto acabou mesmo:
   - com a câmera **Fechada** (a do pregador): o **pregador desceu do púlpito** e ninguém está mais falando. Durante a
     pregação o programa **grava o rosto do pregador do dia** (o rosto maior e mais no centro da câmera do pregador enquanto ele fala); o
     pregador desceu = o rosto dele sumiu da câmera por 1 min. O rosto dos músicos que ficam no palco não é parecido
     e não confunde. Sem o rosto (de costas, câmera longe), o programa usa a quantidade de pessoa na imagem: cai para
     menos da metade da pregação por 1 min. Pela câmera vale até a despedida sem "shalom";
   - sem essa câmera, ou se ela não conseguir decidir: **3 min sem fala** depois de "shalom" + despedida (só música
     ou silêncio).

   Se depois da despedida continuam orando ou falando, a live segue; sem nada disso em 10 min, desarma. Nas lives de
   janeiro a abril de 2026 a despedida veio por volta das **12:30** (de 12:21 a 12:55).

O operador sempre manda: se trocar de cena antes, parar a live ou desligar o sistema, o programa não desfaz e não
repete no mesmo dia. Se a live já estava no ar (ligada à mão), o programa não mexe nas cenas.

Para funcionar: o computador ligado e com a sessão do Windows aberta. O programa cria sozinho a tarefa no
Agendador de Tarefas do Windows ("Culto Copilot - abrir para a live").

---

## 4. A janela do programa

| Aba | Para que serve |
|---|---|
| **Operação** | Ligar/desligar o sistema, entrada de áudio, contagem +2/+5/+10, preparo do culto e, com o sistema ligado, o painel do operador: **Louvor**, **Bíblia** e **Frases** num painel só (música e slide, livro e versículo, aprovar frases), a legenda da fala e o que está no telão. |
| **Fluxo** | O sistema por dentro: transcrição completa, computador (placa de vídeo, memória, energia), validação e registro. |
| **Escriba** | Anotações da pregação no jeito dos escribas da igreja (fidelidade, profética, principal, avisos), com quem ministra e o tema. |
| **Ajustes** | Holyrics, Online, Bíblia, Automático, Músicas, OBS (contagem, TV, testes, câmeras, halation e bloom), YouTube, Fotos, tour, **Manual online**, **Relatar**, pastas e **Reparar instalação**. |
| **Relatar** | Contar um problema ou pedir uma melhoria ([seção 17](#17-relatar-um-problema-ou-pedir-uma-melhoria)). |

---

## 5. Louvor

- Quando a banda canta a letra, o Copilot reconhece a música em poucos segundos e acompanha os slides; a troca vem
  quando o canto chega à última linha. Slide repetido: ele volta e espera o próximo começar.
- Se **você** puser a música pelo Holyrics, ele acompanha dali na hora.
- **"Está tocando tal música?"** com **Sim** e **Não**: o Não faz ele procurar outra, inclusive na internet. A
  pergunta some sozinha quando o canto volta para a música confirmada.
- Oração, fala do ministro ou improviso no meio: ele espera a letra voltar. Ninguém canta há 20 s com a letra no
  telão: o Holyrics volta ao fundo padrão.
- Música fora da playlist: procura na biblioteca inteira. Fora do Holyrics: com internet, procura a letra pelo que
  foi cantado e põe como apresentação rápida; a letra fica guardada e vai para as outras igrejas (**Ajustes ›
  Músicas › Achadas na internet**, com os arquivos para importar no Holyrics).
- **Músicas de todas as igrejas**: ao abrir o programa (com o Holyrics fechado) as músicas novas desta igreja sobem
  e as das outras entram no Holyrics. Nada é apagado; antes vai uma cópia do banco. Se algo der errado:
  **Ajustes › Músicas › Desfazer**.

---

## 6. Leitura bíblica

- O pregador **cita** ("abram em João 3.16"): aparece em **Bíblia**; quando ele **começa a ler**, o versículo vai ao
  telão (Automático) ou fica pronto para **Aceitar** (Sugerir). Conforme ele lê, vêm os seguintes.
- Menção solta ("como diz Romanos 8.28…") só vai para a lista: clique em **Exibir** se quiser mostrar.
- O Copilot percebe a **versão** que o pregador lê e acha os versículos dela. A versão do telão: **Ajustes ›
  Bíblia**.
- Com uma passagem no telão, o pregador anda nela sem repetir livro e capítulo: *"próximo versículo"*, *"volta um
  versículo"*, *"versículo 12"*, *"versículos 5 a 7"*, *"próximo capítulo"*. Vale por 10 min.

---

## 7. Frases de efeito e artes

- Na pregação, o Copilot separa frases marcantes **exatamente como foram ditas**, para **Aprovar**, **Editar** ou
  **Descartar** (o motivo que você escreve ensina a IA). Nenhuma frase vai ao telão sem aprovação, a não ser que
  **Ajustes › Automático › Frases aprovadas** esteja ligado.
- Preencha **Pregador** para o nome sair na arte. A arte é montada no estilo da igreja (telão 16:9 e redes 9:16) e
  fica em **Ajustes › Artes das frases**.
- Frase aprovada pode ir ao chat da live no YouTube ([seção 13](#13-youtube)) e ao app do celular.
- A arte já é feita enquanto a frase espera na fila: ao aprovar, ela vai ao telão na hora.
- **Fotos da igreja nas artes**: algumas artes (3 em cada 10) usam uma foto da igreja de fundo, só fotos da galera adorando. Na pasta das fotos da igreja (**Ajustes › OBS › Contagem e pré-culto › Pasta**), dê a essas fotos um nome começando por **adoracao** (ex.: `adoracao-01.jpg`). Retratos e fotos de família ficam com outro nome: aparecem só nos slides da contagem e na TV da entrada.
- **ARCA 57**: quando alguém chama para se inscrever na ARCA durante o culto ("já fez a sua inscrição na ARCA?") ou
  fala da ARCA junto com a data ("dia 18, 19 e 20 de dezembro"), o QR Code do link de inscrição vai ao telão por 40 s
  (não cobre letra de música; depois, 10 min sem repetir). Na Manancial o link já vem preenchido
  (arca57-conference.vercel.app); muda em **Ajustes › Pré-culto › Link de inscrição da ARCA 57** (vazio = não mostra). Para mostrar na hora:
  **Ajustes › OBS › Testar › QR da ARCA 57 no telão**.
- Ao **Aprovar** ou **Descartar**, a decisão vale na hora; depois aparece "por quê?" (opcional: **Enviar** ou **Pular**).

### Galeria do telão e da live

- Abaixo das frases (no celular, na aba **Arte**): **Enviar fotos ou vídeos** e a galeria com tudo o que foi enviado.
- **Exibir** põe o arquivo no telão e na live na hora; **Parar** (ou **Parar de exibir**) tira. O vídeo toca uma vez e
  fica no último quadro até parar. **✕** apaga da galeria.
- No telão o vídeo sai com som pela **Saída de som da projeção** (Início, embaixo do áudio que o sistema ouve, e no
  tutorial): escolha a saída do computador ligada na mesa por cabo. Na live o vídeo entra sem som (o som chega pela mesa).
- O telão precisa da página do fundo aberta na segunda tela (abre sozinha com o culto).

---

## 8. Automático, Sugerir e culto de validação

- **Sugerir**: o Copilot sugere e você aceita. **Automático**: ele faz sozinho. Depois de uma ação sua no telão,
  o automático espera 8 s antes de agir de novo.
- **Ajustes › Automático** (Slides das músicas, Versículos, Frases aprovadas) liga ou desliga cada um desde o começo do culto.
- **PARAR AUTOMAÇÃO** (painel): para tudo na hora; o mesmo botão vira **RETOMAR**.
- **Culto de validação** (Operação): você opera o Holyrics sozinho, sem aceitar sugestões, e o sistema grava o que
  teria feito, para medir. Depois: **Fluxo › Validação › Avaliar**.
- **Iniciar culto de teste** (Operação, ao lado do culto de validação): tudo funciona normalmente, mas a live do
  YouTube fica **não listada** (só vê quem tem o link). Enquanto durar, aparece o selo **TESTE** ao lado do título.

---

## 9. OBS: letra, versículo, oferta e redes na transmissão

- **Ajustes › OBS › Letra no OBS**: com o OBS aberto, o programa liga o websocket e cria a fonte **Culto Copilot ·
  Letra** na cena no ar. A letra do telão aparece sozinha na transmissão; também o versículo, a lower third da
  pregação (tema e tópico), a frase aprovada, a **barra da oferta** (IBAN, MB WAY…) e, de vez em quando, o **"Nos
  siga nas redes"** com QR.
- **Faixas pretas** de cinema por cima: a letra e o QR ficam dentro da área visível.
- **Testar o OBS**: botões mostram cada coisa por 10 s e voltam ao que estava.
- Datas especiais mudam o visual sozinhas: **ARCA 57** (18 a 20/12/2026), **Natal** (25/12) e **virada** (31/12).
  O painel do versículo também: nos outros dias ele é **branco e liso**; nas datas, no visual do tema (Natal: a gota
  da logo grande, metade para fora à esquerda, e o granulado; ARCA 57: o palco do cartaz com a logo da conferência).
- **Virada do ano** (31/12): às 23:59:30 o **telão** mostra sozinho a contagem de 30 s no visual da virada e, à
  meia-noite, fogos com "Feliz ano novo". Só no telão (a live não muda); precisa da segunda tela. Depois, é só seguir
  com a próxima letra ou versículo.

---

## 10. Contagem regressiva e pré-culto

**Ajustes › OBS › Contagem e pré-culto**: a fonte **Culto Copilot · Contagem** no OBS. A mesma contagem e os slides aparecem **no telão** sozinhos, pela página do fundo, sempre que o Holyrics está vazio antes do culto (qualquer letra ou versículo fica por cima). Depois da hora, a primeira coisa posta no Holyrics encerra a contagem no telão. Quando o sistema liga sozinho pelo horário, um versículo esquecido no telão de outro culto sai.

- Mais de 15 min antes: slides de pré-culto (boas-vindas, primeira vez, redes, horários, Kids, oferta com QR,
  oração, avisos…) se revezam com o vídeo do pré-live. Faltando 15 min: o cartão da contagem. No último minuto, a
  tela final.
- Os textos de cada slide ficam nos campos dessa tela; slide vazio não aparece. Fotos e logo na pasta do pré-culto
  (botão **Pasta**).
- **Testar**: Pré-live, Entrada da contagem, 5 min, Último minuto, Fim (fotos) e Parar teste.
- **+2 / +5 / +10 min** na Operação empurram o início de hoje.
- Com a live automática, depois da hora: **"Já vai começar"** até a saudação ([seção 3](#3-domingo-sozinho-tudo-liga-a-live-começa-e-termina-sem-ninguém)).
- Depois do culto, o QR **"Ache suas fotos"** por 15 min, se houver fotos ([seção 14](#14-fotos-do-culto)).

---

## 11. TV da entrada

Uma TV na porta mostra convites, a contagem e o culto ao vivo, pela rede (sem HDMI).

1. Na TV (navegador), abra uma vez o endereço que aparece em **Ajustes › OBS › Contagem e pré-culto** (algo como
   `http://192.168.0.10:8077`). Se não abrir, toque em **Liberar na rede** (regra do firewall).
2. Aperte **OK** no controle (ou clique) para tela cheia.
3. Antes do culto: as câmeras com convites para entrar (editáveis em **TV da entrada · convites**). Na contagem:
   chamadas grandes. Durante o culto: a câmera ao vivo com a frase fixa embaixo.

Sem TV na porta: responda "Não temos" no tour (ou desligue em Ajustes) e ela não sobe.

---

## 12. Câmeras no OBS e fundo com câmera no telão

- **Várias câmeras** (placas HDMI→USB): cada uma vira uma fonte "Dispositivo de captura de vídeo" no OBS. O Copilot
  descobre sozinho, **pela imagem**, qual é cada uma, e cada papel vai para uma câmera só:
  - **Fechada**: a imagem dela aparece ampliada dentro da imagem de outra (é o zoom do palco), com rosto grande;
  - **Aberta**: o palco largo, parada, e contém a imagem da fechada;
  - **Móvel**: a imagem balança (câmera na mão ou no gimbal);
  - **Público**: muitos rostos virados para a câmera.

  O nome da fonte (Aberta, Fechada, Móvel, Público) ajuda, mas não é preciso. **Ajustes › Câmeras no OBS** monta as
  cenas e já descobre os papéis; durante o culto o programa continua olhando e corrige sozinho. O Copilot corta no
  ritmo da música (na pregação, só aberta e fechada).
- **Placa de corte** (ATEM, Blackmagic, DeckLink, Roland…): o corte é feito nela, então o corte automático do Copilot
  fica desligado.
- **Halation e bloom**: brilho de cinema nas luzes, ajustável em Ajustes.
- **Fundo com câmera no telão**: o fundo das músicas vira uma página por trás do Holyrics, com a câmera entrando
  misturada em alguns momentos.
- **Telão vazio na palavra** (ligado de fábrica, precisa de duas telas): quando a pregação tem tema (dado em Frases
  ou percebido pela IA), o programa monta uma **arte com o tema**, sobre uma foto buscada para ele (fotos de licença
  livre). Sempre que não há nada no telão, aparece essa arte em vez da área de trabalho. Trocou o nome da pregação:
  a arte é refeita. Antes da arte ficar pronta (e se o vídeo de uma música não tocar), vai uma foto escura de culto, nunca o preto.
  Na palavra, com o telão vazio, a **câmera** entra em alguns momentos por cima da arte, devagar e presa no mesmo rosto. As fotos
  achadas também aparecem com mais frequência no fundo das artes das frases.

---

## 13. YouTube

**Ajustes › YouTube da live** (conecte uma vez, com a conta do canal). Depois, sozinho:

- **Título** no padrão do canal, com o tema da pregação assim que a IA souber
  ([seção 3](#3-domingo-sozinho-tudo-liga-a-live-começa-e-termina-sem-ninguém)).
- **Thumbnail**: frase de efeito da pregação + a foto que a mídia manda pelo QR **"Foto da thumbnail"**, no estilo
  das artes da igreja.
- **Chat**: a frase aprovada vai ao chat da live uma vez.
- **Voltar na live (DVR)**: o programa liga o DVR da live antes de ela começar, para quem assiste poder voltar.
  Live que já entrou no ar sem DVR (só o quadradinho do "ao vivo" no player) não muda mais: o programa avisa, e a
  igreja liga em YouTube Studio › Transmitir › Configurações › **DVR** para as próximas.
- **Momentos**: os capítulos do culto na descrição, por tipo de momento: *Momento de adoração* (com a música), *Palavra* (com o tema), cada **leitura** com a referência (*"Leitura: Atos 16:21-26"*), cada **tópico** com os versículos citados nele, oferta, *Chamamento*, *Novos filhos*, *Oração da família* e outros que a IA reconhecer.
- **Lives preparadas antes** (com título e thumbnail próprios): o programa não troca o título nem a thumbnail delas
  no dia, só usa a live.
- **Lives da ARCA 57** (título com "Arca", como "Manancial PMW - Arca 57", ou nas datas da conferência): a mídia
  manda a foto da palavra pelo QR **"Foto da thumbnail"** e a thumbnail sai no **design da ARCA** (pessoa recortada
  à esquerda com luz vermelha, ARCA57, a frase grande, a linha vermelha e o nome do pregador). Ela vai para a live,
  mesmo a preparada antes (o título dela continua o mesmo), e para o corte da palavra.
- **Corte da palavra**: com a live no ar, o OBS grava (se ninguém já estava gravando). Quando a live acaba, a
  **pregação principal** (a mais longa, com 10 min ou mais; uma por live) vira um vídeo no canal, com a **mesma
  thumbnail da live**, título com o **tema e o nome do pregador** e, na descrição, o link do culto completo e os
  tópicos. Na ARCA, o título sai como `{tema} | {pregador} - Arca 57`. Ajustes › OBS: **"Corte da
  palavra no YouTube"** (sim/não) e **"Título do corte"** (padrão `{tema} | {pregador}`; também `{data}`). Na
  primeira vez o programa baixa o ffmpeg (~140 MB). A gravação inteira fica na pasta de gravação do OBS.
- **Cortes do culto** (Shorts e Reels: o mesmo vídeo vai para os dois): depois do corte da palavra, da mesma
  gravação do OBS, sai o **máximo de cortes bons** do louvor e da palavra principal, todos **verticais**, intercalados:
  - **Verticais** (20 a 60 s): os trechos mais fortes da palavra (as frases de efeito do culto e, com a chave do LLM,
    a escolha dele) e o refrão de cada música. Cor de cinema, sem as faixas pretas, e a legenda palavra por palavra no
    estilo da Poiema (Inter Display, e Instrument Serif itálica em Jesus, Deus, Senhor, Cristo, Espírito e reino; a
    palavra de destaque numa serifa itálica pesada em amarelo, vermelho ou verde-limão; cada letra entra borrada e
    fica nítida). Alternam **tela cheia** e **faixa** (o vídeo horizontal no meio da tela preta, a legenda do lado
    oposto ao rosto).
  - **Câmera**: segue o rosto como um operador, suave e sem tranco: fica parada enquanto a pessoa está perto do
    meio, antecipa quando ela anda e mantém o rosto sempre nos **70% do meio** da imagem. Na palavra, segue o
    **pregador** pelo rosto que a live aprendeu no culto (não o músico que estiver mais perto da câmera).
  - **Palavra, o trecho**: uma ideia completa, de 36 a 75 s antes da edição (os Shorts da Poiema vão de 13 a 76 s,
    mediana de 27 s). Começa onde a ideia começa (nunca em "e", "então", "mas", "isso" ou num resto de frase) e
    termina quando ela conclui: nunca logo depois de "olha como termina", "vou te explicar", numa pergunta sem a
    resposta ou num "E se...". O vídeo abre com um **gancho**: a frase mais forte ou polêmica (se ela não for a
    primeira, entra antes, e depois o trecho começa; no meio, essa frase não se repete).
  - **Palavra, pelo Claude** (Pré-culto **"Cortes da palavra planejados pelo Claude"** = sim): no fim da live o
    programa escreve um pedido (a pregação em frases numeradas e as instruções) em `data/reels/AAAA-MM-DD/claude/` e
    os cortes esperam o plano do Claude por até 48 h (depois, saem pelo LLM do programa). O Claude escolhe os cortes,
    o gancho, a frase de efeito, o telefone e o B-roll, e **corrige a transcrição** das frases usadas (a legenda sai
    com o texto certo, no tempo da voz). Dois jeitos de chegar ao Claude: um **agendamento do Claude** no PC (aos
    domingos, depois do culto, lê os pedidos pendentes e grava o plano; o programa confere de meia em meia hora e faz
    os vídeos), ou
    em Ajustes › Cortes do culto, **"Copiar pedido para o Claude"**, colar no Claude e **"Colar o plano do Claude"**.
  - **Palavra, edição**: as pausas da fala são cortadas (corte seco, com um crossfade curto no som; cada palavra
    guarda 0,18 s antes e 0,22 s depois, para não comer o começo nem o "s" final; palavra cortada pela metade, como "Cri..." antes de "Cristo", sai da
    legenda e do áudio). O áudio de cada corte é **ouvido de novo** pelo Whisper local (no processador, se o modelo
    já estiver no PC): os cortes de pausa e a legenda seguem o tempo preciso de cada palavra (a transcrição ao vivo
    chega até 0,7 s atrasada e cortava o começo das palavras), e a **frase dita duas vezes seguidas** ("Nada de
    resto pra Ele. Nada de resto pra Ele.") fica uma vez só, porque no corte soa como o mesmo take repetido; a cada corte o take alterna entre
    mais perto e mais aberto; termina seco, sem fade (o fade deixava ouvir o começo da fala seguinte). Em metade dos
    cortes, a **frase de efeito** sai com **voz de telefone** ou com **reverb** (a voz ecoa, como num auditório, no
    silêncio da música); nunca numa frase qualquer. O louvor fica sem cortes,
    só a imagem do louvor.
  - **Palavra, legenda**: anda no tempo da voz (cada palavra aparece quando é dita, inteira em até 0,17 s) e cada
    bloco fecha no fim da frase. Como nos cortes da Zion e da Poiema, o formato **muda ao longo do vídeo** (nunca 3
    vezes o mesmo seguido): a palavra forte **gigante** em caixa alta condensada (bege), a **pilha** pequena/grande/
    pequena, a **escada** (a primeira palavra grande, o resto deslocado), a palavra **solta** em lugares diferentes da
    tela e o da Poiema (pequenas + a grande, o destaque na serifa colorida). As letras só se formam com animação na abertura e nas palavras grandes que
    ficam tempo na tela; o resto aparece seco. Blocos só de "querido", "entenda" ficam
    sem legenda, para respirar.
  - **Palavra, trilha** (dois de cada três cortes): a voz é separada do que estava tocando na igreja (modelo
    MDX-Net, baixado uma vez, ~65 MB), entra uma música de fundo calma, que **para seca na frase de efeito** (só a
    voz) e volta **outra música já num ponto animado** logo depois, com um riser antes e um boom (impact) na
    entrada. As duas músicas já entram na parte forte. Riser, boom e whoosh são **efeitos de verdade que vêm com o programa** (18 sons CC0 do Freesound, em `arte\efeitos`, com a origem de cada um no LEIA-ME de lá), alinhados pelo pico: o riser chega ao auge onde a música para, o boom bate quando a outra música entra e o whoosh passa no corte do gancho para o começo do trecho. Para usar efeitos próprios: Pré-culto › **"Pasta dos efeitos sonoros dos cortes"** (o tipo sai do nome do arquivo ou da pasta: riser, boom, impact, hit, whoosh...). As músicas são **épicas e vêm com o programa** (8 trilhas CC0 do Freesound, em `arte\musicas`, com a origem de
    cada uma no LEIA-ME de lá). Para usar músicas próprias: Pré-culto **"Pasta das músicas de fundo dos cortes"**
    (vazia = as do programa); arquivo que não abre fica de fora. Atenção: música com direitos autorais pode ser
    reclamada pelo YouTube (o vídeo fica sem som ou sem monetização); use músicas que a igreja pode usar.
  - **Palavra, B-roll**: quando ele fala de algo que dá imagem (tempestade, mar, família...), entram 1 ou 2 vídeos
    curtos do **Pexels** (grátis, uso livre), escolhidos pela IA. Precisa da chave do Pexels: crie em
    pexels.com/api e cole em Ajustes › Online › Chaves próprias › **Pexels**. Sem a chave, sai sem B-roll.
  - **Louvor**: a legenda é a letra do telão **conferida com o que foi cantado** (a transcrição): se o detector errou
    o slide ou a música na hora, aquele trecho não vira corte. Aparece **só a linha que está sendo cantada**, na
    hora em que foi cantada. O enquadramento do louvor nunca pega o canto de baixo à esquerda, onde fica a letra da
    própria live.
  - **Horizontais** (só com **"Também cortes horizontais no YouTube"** = sim no Pré-culto; padrão não): trechos de 1
    a 5 min da palavra e as músicas inteiras (até 5 min), com thumbnail no modelo da live.
  - **Semana**: os cortes sobem **agendados** e o YouTube publica sozinho, 2 por dia a partir do dia seguinte (campo
    **"Horários das postagens"**, padrão `12:00, 19:00`), por 7 dias. A cota da API de cada igreja dá uns 5 envios
    por dia (o corte da palavra é um): o que não couber sobe no dia seguinte em que o programa estiver aberto (ele
    confere a fila de meia em meia hora). Horário que passou com o PC desligado vai para o próximo livre.
  - Ajustes › OBS › **Cortes do culto**: cada corte com o vídeo, o formato, quando vai ao ar, **Baixar**, **Copiar
    legenda** (texto do post para o Instagram) e **Não postar** (tira da agenda; se já subiu, fica privado no
    YouTube). Pré-culto: **"Cortes do culto"** (sim/não), **"Máximo de cortes por culto"** (padrão 12),
    **"Estilo dos reels"** (tela cheia, faixa ou os dois), **"Postar os cortes no YouTube ao longo da semana"**
    (padrão sim), **"Horários das postagens"**, **"Também cortes horizontais no YouTube"** (padrão não),
    **"Cortes da palavra planejados pelo Claude"** (padrão não), **"Música de fundo em parte dos cortes da
    palavra"** (padrão sim), **"Pasta das músicas de fundo dos cortes"** e
    **"B-roll do Pexels nos cortes da palavra"** (padrão sim). Arquivos em `data/reels/AAAA-MM-DD/`.
  - A gravação do OBS liga se o corte da palavra **ou** os cortes estiverem ligados, e sempre para quando a live
    acaba.
  - O projeto do Google da igreja precisa estar **verificado** pelo YouTube para os vídeos enviados pela API
    ficarem públicos (projeto não verificado: o YouTube trava como privado). Se o corte da palavra já aparece
    público no canal, está verificado.

---

## 14. Fotos do culto

**Ajustes › Fotos › Fotos do culto**: a mídia só coloca o cartão da câmera no computador. As fotos são editadas
sozinhas, as tremidas ficam de fora, e no fim do culto aparece o QR **"Ache suas fotos"**: a pessoa manda uma
selfie e recebe as fotos em que aparece.

---

## 15. Celular e tablet

Um QR só (ícone de celular na Operação › **Celular: painel e avisos**), com o sistema ligado e o celular no
**mesmo Wi-Fi**:

1. Aponte a câmera do celular: abre o **painel do operador** (aceitar sugestões, aprovar frases, trocar slides).
2. Toque na **bolinha** em cima, na logo: **verde** = avisos ligados neste celular (sistema ligou e desligou, live
   no ar, câmera no ar, erros, arte pronta); **cinza** = desligados; **vermelha** = bloqueados (libere as
   notificações do site nas configurações do celular). Dá para ligar ou desligar a qualquer momento.
3. No menu do navegador, **Adicionar à tela inicial**: o painel vira um app com ícone. No iPhone, os avisos só
   funcionam pelo ícone da tela inicial.

Os avisos chegam mesmo com o painel fechado.

### Celular como microfone (reserva se o som der problema)

1. No painel do celular, toque no **microfone** (ao lado da bolinha) e permita o microfone. Ele fica **verde**:
   o celular já está mandando o áudio ao computador, pronto para a troca. Fica ligado até tocar de novo e volta
   sozinho ao reabrir o painel.
2. Se o som da mesa der problema: no programa, **Início › entrada de áudio › Celular (microfone remoto)** (grupo
   "Reserva"). A troca é na hora, sem parar o culto. No celular o microfone fica **vermelho** = é a entrada do culto.
3. Som da mesa de volta: escolha a entrada de antes no mesmo seletor.

Cuidados: deixe a **tela do celular acesa com o painel na frente** (o celular corta o microfone de apps em
segundo plano); carregador ligado; perto de quem fala ou da caixa de som. Abra pelo QR (endereço seguro): pelo
endereço comum o celular não libera o microfone. Amarelo = microfone ligado, mas sem conexão com o computador
(Wi-Fi ou sistema desligado); volta sozinho.

---

## 16. Transcrição e IA pela internet

**Ajustes › Online › Pela internet**: a transcrição e a IA rodam pela internet e o computador fica
de reserva (sem internet, volta sozinho para o local).

1. Chave do **Groq** (grátis): **Abrir o site do Groq** › entre › **API Keys › Create API Key** › copie (começa com
   `gsk_`) › cole em **Chave do Groq** › **Salvar** (fica "configurada ✓").
2. Opcional: chave do **Deepgram** (crédito grátis): transcrição em tempo real, melhor para os slides.

As chaves ficam só neste computador.

---

## 17. Relatar um problema ou pedir uma melhoria

**Antes, tente a Ajuda com IA** (botão **Ajuda** na barra lateral ou **Ajustes › Ajuda com IA**): escreva a dúvida e
escolha ChatGPT, Claude, Perplexity ou Gemini. A IA abre no navegador já com este manual e a regra de responder só
por ele. No Gemini, o texto vai copiado: cole com Ctrl+V. Se a IA não achar a resposta, ela pede para você relatar.

Botão **Relatar** (barra lateral ou **Ajustes › Problema ou ideia**):

1. Escolha **Algo deu errado** ou **Tenho uma ideia** e escreva o que aconteceu (ou a ideia).
2. **Apontar na tela**: clique no lugar do programa que deu problema (um botão, um texto…). Ele fica marcado no
   relato.
3. Marque em que cultos vocês usam o programa.
4. **Enviar**. Os registros de hoje vão junto (sem senhas nem chaves), para achar o erro. O relato fica guardado no
   computador e chega a quem cuida do programa.

---

## 18. Quando algo dá errado

| Situação | O que fazer |
|---|---|
| Sugestão errada | **Recusar**. Se insistir, ponha o módulo em **Desligado** ou use **PARAR AUTOMAÇÃO**. |
| Transcrição "lenta" ou "manual" | As sugestões atrasam ou param; siga pelo Holyrics. Volta sozinho. |
| Holyrics fechou ou travou | Reabra o Holyrics; o Copilot reconecta. |
| A letra não aparece no OBS | **Ajustes › OBS › Letra no OBS** com o OBS aberto (o programa liga o websocket; se pedir, feche e abra o OBS). |
| A live não começou sozinha | Veja o aviso no celular: sem sinal de câmera, OBS fechado ou o programa não estava aberto às 8h. Comece pelo OBS normalmente. |
| A câmera não entrou na saudação | Troque a cena no OBS à mão; o programa não desfaz. |
| A contagem está na hora errada | **Ajustes › OBS › Contagem › Início do culto** e os **dias**; para hoje, use +2/+5/+10. |
| TV da entrada com barras coloridas | Câmera sem sinal fica fora da TV (ficam as fotos). Se aparecer, confira a versão em Ajustes › Atualização. |
| Painel não abre no tablet | Mesmo Wi-Fi e sistema ligado. |
| Som da mesa parou | Microfone no celular ligado (verde) e, no programa, entrada **Celular (microfone remoto)** ([seção 15](#15-celular-e-tablet)). |
| O programa não abre | Menu Iniciar › Culto Copilot › **Reparar instalação**. |
| O notebook desligou | Religue, abra o programa e **Ligar o sistema**. |
| Qualquer dúvida no meio do culto | **PARAR AUTOMAÇÃO** e siga pelo Holyrics. O culto não depende do Copilot. |

Ainda com problema? **Relatar** ([seção 17](#17-relatar-um-problema-ou-pedir-uma-melhoria)).

---

## 19. Onde fica cada coisa

| Quero… | Onde |
|---|---|
| Ligar antes do culto | **Operação › Ligar o sistema** |
| Dar mais tempo na contagem | **Operação › Contagem › +2 / +5 / +10 min** |
| Mudar dias e horário dos cultos | **Ajustes › OBS › Contagem e pré-culto** (ou o tour) |
| Live sozinha, cenas, título | **Ajustes › OBS › Contagem e pré-culto** |
| Textos dos slides de pré-culto | **Ajustes › OBS › Contagem e pré-culto** |
| Convites da TV da entrada | **Ajustes › OBS › Contagem e pré-culto › TV da entrada** |
| Letra na transmissão | **Ajustes › OBS › Letra no OBS** |
| Várias câmeras | **Ajustes › Câmeras no OBS** |
| YouTube | **Ajustes › YouTube da live** |
| Fotos do culto | **Ajustes › Fotos** |
| Transcrição online | **Ajustes › Online** |
| Artes das frases | **Ajustes › Artes das frases** |
| Refazer o tour | **Ajustes › Tour de boas-vindas** |
| Tirar uma dúvida com IA | **Ajuda** (barra lateral) |
| Reportar um erro | **Relatar** |
