# Ideia de jogo: "TeamRaid: Dungeon Guilds"

**Conceito:** Jogo cooperativo em equipe (PvE) onde grupos de amigos formam **guildas** (times de 4-8 jogadores) e invadem **masmorras geradas proceduralmente** juntos. É divertido, social, caótico e perfeito pro Discord (todo mundo no voice chat gritando plano de ataque).

**Mecânicas principais** (fáceis de fazer com lógica funcional):

- Mapa grid/hexagonal gerado proceduralmente (algoritmo de masmorra + Perlin noise simples - tudo em Elixir puro).

- Cada jogador escolhe **classe** (Tank, Healer, DPS, Scout) com habilidades únicas.

- **Tempo real leve** (movimento contínuo + ações com cooldown) ou **turn-based por sala** (mais fácil de começar e 100% determinístico).

- Objetivo por raid: explorar, matar chefes, coletar loot raro, escapar antes do tempo acabar.

- **Modo equipe:** Vocês votam ações em grupo (ex.: "todo mundo ataca o boss agora"), ou cada um age individualmente mas o servidor sincroniza tudo.

- **Escalabilidade:**
    - Salas privadas de 4-8 amigos (ideal pro Discord).
    - Ou um "grande salão" com múltiplas equipes competindo (quem extrai mais loot ganha).
    - Suporta 20-50+ jogadores simultâneos sem problema (Elixir escala horizontalmente com um clique).

### Por que é legal e "maker":

- Procedural = cada raid é diferente (seeds baseados no nome da guilda).
- Lógica em Elixir = regras imutáveis, testes automáticos fáceis, zero bugs de estado compartilhado.
- Social: chat in-game + integração Discord voice + placar de guildas.
- Diferente do habitual: não é mais um Among Us ou Valorant clone - é um roguelike cooperativo com almea de party game.

Se quiser algo mais competitivo: vire PvP (duas guildas invadindo a mesma masmorra e sabotando uma à outra). Mas co-op é mais "divertido de jogar em equipe".

## Arquitetura simples (visual)

