# Manual do Culto Copilot

O Culto Copilot escuta o culto pelo som da mesa e cuida da projeção junto com você: troca os slides das músicas
no **Holyrics**, põe os versículos que o pregador lê, separa frases marcantes da pregação, monta a transmissão no
**OBS** (letra, versículo, oferta, contagem, câmeras) e pode até ligar a live sozinho. **Quem manda é você**: tudo o
que você fizer no Holyrics ou no OBS tem prioridade, e o Holyrics continua funcionando normalmente mesmo se o
Copilot parar.

> **Tem uma dúvida?** Procure aqui com Ctrl+F, ou pergunte a uma IA (Claude, ChatGPT…) colando o endereço deste
> manual: *"Leia https://github.com/pivotanimato-oss/culto-copilot-manual e me diga como fazer X no Culto
> Copilot"*. Achou um erro ou quer uma melhoria? Use **Relatar** no programa ([seção 17](#17-relatar-um-problema-ou-pedir-uma-melhoria)).

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
   Área de Trabalho. As atualizações chegam sozinhas depois.
2. Abra o programa. O **tour de boas-vindas** pergunta, em poucas telas:
   - **O que a sua igreja usa?** Se vocês **fazem live** (OBS/YouTube) e se têm uma **TV na porta da igreja**. Sem
     live, o programa não procura o OBS; sem TV, a TV da entrada fica desligada.
   - **Quando são os cultos?** Os dias da semana e o horário do culto principal. A contagem e a TV da entrada só
     aparecem nesses dias.
   - **De onde vem o som do culto?** A entrada de áudio (o som da mesa).
   - **Conectar o Holyrics**: o token da API (no Holyrics: *Arquivo › Configurações › API Server*).
   - Se você já vê as letras de perto, quanto da projeção o Copilot assume (100% automático ou só sugestões) e se
     vai controlar também pelo celular.
3. Para refazer o tour: **Ajustes › Tour de boas-vindas › Refazer**.

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
| **Iniciar a live sozinha** | `domingo 10:00` | Põe o OBS na cena do pré-live (com a contagem por cima) e começa a transmitir. |
| **Cena do pré-live** | `PRE-LIVE` | Onde a live começa (vídeo e música do pré-live, sem o som da mesa). |
| **Cena do culto** | `CAMERA` | Entra na saudação de abertura: câmera e som da mesa. |
| **Cena do fim** | `FINALIZAR` | Entra na bênção final; a transmissão termina 2 min depois. |
| **Título da live** | `domingo: 🔴MANHÃ DE GLÓRIA - {data} \| {tema} \| CAMNCL` | O título no YouTube; `{data}` vira 15-11 e `{tema}` o tema da pregação. Uma linha sem dia vale para os outros dias. |

Vários horários: separe com `;` (ex.: `domingo 10:00; quarta 19h30`). Vazio = não faz.

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
5. **Bênção final** (*"a graça do Senhor Jesus Cristo… comunhão do Espírito Santo"*, *"Deus abençoe"*, *"até
   logo"*, junto com *"shalom, shalom"*): vai para a **cena do fim** e a transmissão termina 2 min depois.

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

---

## 8. Automático, Sugerir e culto de validação

- **Sugerir**: o Copilot sugere e você aceita. **Automático**: ele faz sozinho. Depois de uma ação sua no telão,
  o automático espera 8 s antes de agir de novo.
- **Ajustes › Automático** (Slides das músicas, Versículos, Frases aprovadas) liga ou desliga cada um desde o começo do culto.
- **PARAR AUTOMAÇÃO** (painel): para tudo na hora; o mesmo botão vira **RETOMAR**.
- **Culto de validação** (Operação): você opera o Holyrics sozinho, sem aceitar sugestões, e o sistema grava o que
  teria feito, para medir. Depois: **Fluxo › Validação › Avaliar**.

---

## 9. OBS: letra, versículo, oferta e redes na transmissão

- **Ajustes › OBS › Letra no OBS**: com o OBS aberto, o programa liga o websocket e cria a fonte **Culto Copilot ·
  Letra** na cena no ar. A letra do telão aparece sozinha na transmissão; também o versículo, a lower third da
  pregação (tema e tópico), a frase aprovada, a **barra da oferta** (IBAN, MB WAY…) e, de vez em quando, o **"Nos
  siga nas redes"** com QR.
- **Faixas pretas** de cinema por cima: a letra e o QR ficam dentro da área visível.
- **Testar o OBS**: botões mostram cada coisa por 10 s e voltam ao que estava.
- Datas especiais mudam o visual sozinhas: **ARCA 57** (18 a 20/12/2026), **Natal** (25/12) e **virada** (31/12).

---

## 10. Contagem regressiva e pré-culto

**Ajustes › OBS › Contagem e pré-culto**: a fonte **Culto Copilot · Contagem** no OBS (e no telão, se quiser).

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

- **Várias câmeras** (placas HDMI→USB): cada uma vira uma fonte "Dispositivo de captura de vídeo" no OBS, e o nome
  diz o papel: **Aberta**, **Fechada**, **Móvel**, **Público**. **Ajustes › Câmeras no OBS** monta as cenas, e o
  Copilot corta sozinho no ritmo da música (na pregação, só aberta e fechada).
- **Placa de corte** (ATEM, Blackmagic, DeckLink, Roland…): o corte é feito nela, então o corte automático do Copilot
  fica desligado.
- **Halation e bloom**: brilho de cinema nas luzes, ajustável em Ajustes.
- **Fundo com câmera no telão**: o fundo das músicas vira uma página por trás do Holyrics, com a câmera entrando
  misturada em alguns momentos.

---

## 13. YouTube

**Ajustes › YouTube da live** (conecte uma vez, com a conta do canal). Depois, sozinho:

- **Título** no padrão do canal, com o tema da pregação assim que a IA souber
  ([seção 3](#3-domingo-sozinho-tudo-liga-a-live-começa-e-termina-sem-ninguém)).
- **Thumbnail**: frase de efeito da pregação + a foto que a mídia manda pelo QR **"Foto da thumbnail"**, no estilo
  das artes da igreja.
- **Chat**: a frase aprovada vai ao chat da live uma vez.
- **Momentos**: os capítulos do culto (louvor, músicas, palavra, oferta, tópicos) na descrição.

---

## 14. Fotos do culto

**Ajustes › Fotos › Fotos do culto**: a mídia só coloca o cartão da câmera no computador. As fotos são editadas
sozinhas, as tremidas ficam de fora, e no fim do culto aparece o QR **"Ache suas fotos"**: a pessoa manda uma
selfie e recebe as fotos em que aparece.

---

## 15. Celular e tablet

- **App no celular** (ícone de celular na Operação): aponte a câmera, abra e ative os avisos (sistema ligou e
  desligou, erros, live no ar, câmera no ar, arte pronta).
- **Painel no tablet**: pelo celular ou tablet dá para aceitar sugestões, aprovar frases e trocar slides. Precisa
  estar no **mesmo Wi-Fi** e com o sistema ligado.

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
| Painel não abre no tablet | Mesmo Wi-Fi e sistema ligado. |
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
| Reportar um erro | **Relatar** |
