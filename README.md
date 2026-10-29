# FNaF 1 3D — movimento livre

Jogo de terror em 3D que roda direto no navegador, em **um único arquivo** (`fnaf1v36.html`). Você é o vigia noturno de uma pizzaria com animatrônicos que se mexem quando ninguém está olhando. Sobreviva até as 6 da manhã.

Funciona no **celular (toque)** e no **PC (teclado e mouse)**, e tem **multiplayer cooperativo de até 5 jogadores**.

> Projeto de fã, sem fins lucrativos e sem ligação com os criadores de nenhuma franquia. Todos os personagens, nomes e gráficos são originais.

## Como jogar

Abra o `fnaf1v36.html` no navegador (ou publique no GitHub Pages) e toque/clique em **COMEÇAR**.

1. Entre na pizzaria pelas portas de vidro.
2. Vá até o **gerador** e segure **E** para ligar a energia.
3. Chegue ao escritório, vigie as câmeras e controle as portas e as luzes.
4. Aguente até as **6 AM** e saia pela porta do saguão.

### Controles

| Ação | PC | Celular |
|---|---|---|
| Andar | WASD | Joystick |
| Olhar | Mouse | Arrastar a tela |
| Correr (gasta fôlego) | Shift | Botão RUN |
| Interagir | E ou clique (segurar: luz e gerador) | Botão E |
| Lanterna | F | Botão F |
| Câmeras | Espaço | Botão CAM |
| Configurações | Esc | Botão ⚙ |

O jogo **detecta sozinho** se você está usando toque ou teclado e mouse, inclusive celular com teclado/mouse. Para forçar um modo, use `?touch=1` ou `?touch=0` na URL.

## Os animatrônicos

- **Barão**: só anda quando você não olha para ele (e sempre, se a energia acabar).
- **Zig**: é atraído pela luz; com a lanterna ligada ele fica mais rápido.
- **Pipoca**: fica mais rápida com barulho (correr, ligar o gerador).
- **Rex**: fica furioso no Pirate Cove. Vigie a câmera 1C e, quando ele correr, feche a porta. Apontar a lanterna para ele o deixa mais lento.

Porta fechada faz Barão, Zig e Pipoca desistirem e se afastarem por um tempo.

## Lanterna e pilhas

A lanterna gasta bateria. Há poucas pilhas espalhadas pelo mapa (cada uma recarrega 45%), então escolha bem quando usá-la.

## Perfil

Em **👤 PERFIL**, no menu, você escolhe o seu **nome** e uma **imagem**: um dos animatrônicos (Barão, Zig, Pipoca ou Rex) ou uma foto do seu celular/PC. O perfil fica salvo no seu aparelho e aparece para os outros jogadores da sala.

## Multiplayer (até 5 jogadores)

1. No menu, abra **👥 MULTIPLAYER**.
2. Uma pessoa **cria a sala** e define o máximo de jogadores (2 a 5). O host pode mudar esse máximo depois, com a sala aberta.
3. Ela passa o **código** (4 letras) ou o **link** (`?sala=CODIGO`) para os outros.
4. Quando todos entrarem, o host fecha a janela e toca em **▶ COMEÇAR** no menu. A noite começa para todo mundo.

A sala continua aberta entre as noites: quem estava dentro segue junto na próxima noite, e novos jogadores podem entrar entre uma noite e outra. Se dois jogadores escolherem o mesmo nome, o jogo acrescenta um número (por exemplo, "Ana 2").

Todos jogam a mesma noite no mesmo mapa. O host controla relógio, energia, portas e robôs; os robôs perseguem quem estiver mais perto. Quem é pego vira espectador, e a noite termina quando todos forem pegos ou chegar 6 AM.

**Observações**
- A conexão é direta entre os aparelhos (WebRTC via [PeerJS](https://peerjs.com/)), sem servidor próprio. A biblioteca é carregada de um CDN, então é preciso internet.
- Em algumas redes (dados móveis, Wi-Fi corporativo) a conexão pode falhar. O jogo usa servidores de relay públicos como reserva, mas sem garantia.
- O multiplayer ainda é novo: relate qualquer problema nas issues.

## Publicar no GitHub Pages

1. Envie o `fnaf1v36.html` para o repositório (se quiser abrir direto pelo endereço do site, mantenha também uma cópia chamada `index.html`).
2. Em **Settings → Pages**, escolha a branch principal e a pasta raiz.
3. Compartilhe o link gerado; o link de sala fica `https://miguelbelardt.github.io/Fnaf-1-3D-movimento-livre/fnaf1v36.html?sala=CODIGO`.

## Tecnologia

- [three.js](https://threejs.org/) r128 (via CDN), iluminação por vértice e lanterna por shader.
- JavaScript puro, sem build e sem dependências locais.
- PeerJS 1.5.4 (via CDN) para o multiplayer.

## Contribuindo

Sugestões e correções são bem-vindas: abra uma issue ou um pull request. Mantenha o projeto em um único arquivo e use apenas personagens e recursos originais.

## Licença

Defina aqui a licença do projeto (por exemplo, MIT).
