# 🧙‍♂️ Codex Of — Um Roguelike Terminal em C

> Um jogo de exploração e sobrevivência baseado em fases com ambientes distintos, monstros e artefatos ocultos. Viva a jornada de um herói que atravessa terras arruinadas em busca da última esperança da humanidade.

---

## 📜 História

No crepúsculo da era dos homens, criaturas das trevas romperam as barreiras do mundo mortal. A luz das civilizações desapareceu. Contudo, uma esperança ainda pulsa: o **Artefato da Aurora**, selado por antigos guardiões.

Você é o último herói. Um viajante que acorda na Vila Miralume com a missão de atravessar vales, picos e infernos. Seu objetivo: recuperar o artefato e selar novamente as forças que consomem o mundo.

---

## 🎮 Regras do Jogo

- 👣 **Movimentação**:
  - `W`, `A`, `S`, `D` ou setas: mover o personagem.
- 🗝️ **Interação**:
  - `I`: interagir com objetos como chaves, portas e NPCs.
- 💀 **Vidas**:
  - Você começa com 3 vidas. Morrer em espinhos, fogo ou para monstros reduz 1 vida.
- 🚪 **Progresso**:
  - Algumas fases exigem chaves para abrir portas ou botões para acessar áreas ocultas.
- ⚠️ **Colisão**:
  - Você não pode atravessar paredes, água (sem nadar) ou obstáculos.

---

## 🧩 Bibliotecas Utilizadas

| Biblioteca        | Função Principal                                                                 |
|-------------------|-----------------------------------------------------------------------------------|
| `stdio.h`         | Entrada/saída padrão (`printf`, `scanf`, etc.)                                   |
| `stdlib.h`        | Utilitários gerais (memória, números aleatórios com `rand`, etc.)                 |
| `time.h`          | Permite `srand(time(NULL))` para aleatoriedade dinâmica                          |
| `conio.h`         | Captura de teclas com `getch()` sem esperar `Enter`                              |
| `windows.h`       | Funções do console: `SetConsoleOutputCP()` e `SetConsoleCursorPosition()`        |

### Principais comandos:

- `gotoxy(x, y)`: move o cursor para uma coordenada X/Y no console.
- `SetConsoleOutputCP(65001)`: define saída como UTF-8 para suportar acentuação e símbolos.
- `getch()`: detecta pressionamento de tecla sem precisar de Enter.
- `rand() % N`: gera um número aleatório entre 0 e N-1.

---

## 🗺️ Legenda de Caracteres

Esses são os ícones que você verá no terminal. Cores e símbolos foram escolhidos para dar identidade visual ao jogo:

| Caractere | Símbolo | Significado                       |
|-----------|---------|-----------------------------------|
| `H`       | 🧍       | **Herói**                         |
| `M`       | 🧟       | **Monstro comum**                 |
| `C`       | 💀       | **Chefe final**                   |
| `#`       | 🧱       | **Parede**                        |
| `=`       | 🚪       | **Porta aberta**                  |
| `D`       | 🔒       | **Porta fechada**                 |
| `-`/`─`   | 🔲       | **Telhado horizontal**            |
| `│`       | 🔳       | **Telhado vertical**              |
| `┌┐└┘`    | 🏠       | **Cantos do telhado (casa)**       |
| `p`       | 🗝️       | **Chave**                         |
| `O`       | 🔘       | **Botão**                         |
| `<`, `>`  | 🌀       | **Teletransportadores**           |
| `*`       | ⚠️       | **Espinho (dano)**                |
| `.` `,` `;` | 🪨     | **Pedra ou solo rochoso**         |
| `^`, `v`  | ❄️       | **Gelo**                          |
| `~`, `=`  | 🌊       | **Água**                          |
| `"` `;` `'` | 🌿     | **Grama**                         |
| `#` (laranja) | 🔥  | **Chão flamejante**               |
| `N`       | 👴       | **NPC da casa do guardião**       |
| `#` (laranja/laranja-claro) | 🪟 | **Tapete**            |

---

## ⚙️ Como Compilar

Você precisa de um compilador C (recomenda-se `gcc`) no Windows com suporte a Windows.h (MSVC ou MinGW):

### 💻 Windows (MinGW)

```bash
git clone https://github.com/seuusuario/CodexOf.git
cd CodexOf
gcc src/main.c -o codexof -luser32 -lkernel32
./codexof
```

---

## 🎨 Créditos

Este jogo foi desenvolvido como parte de um projeto avaliativo.

- 👨‍💻 **Nícola C. Gonçalves** – Programador Principal, Menus
- 🎮 **Luca R. Bacelar** – Pensamento Lógico, Narrativa
---
