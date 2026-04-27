# UI/UX Fighters — Hackathon

Página de divulgação do hackathon da equipe de UI/UX Design, construída como uma tela de seleção de personagem estilo arcade dos anos 90 (Street Fighter / Mortal Kombat).

![Estilo arcade retro · CRT scanlines · pixel art](https://img.shields.io/badge/style-arcade--retro-yellow) ![Sem dependências](https://img.shields.io/badge/dependencies-none-brightgreen)

## ✨ Recursos

- **Tela de seleção 2v2** — duas duplas se enfrentam (formato do hackathon)
- **Estética arcade completa** — fontes Press Start 2P + VT323, scanlines CRT, vinheta, glitch RGB no logo
- **Trilha sonora** — Techno Syndrome 16-bit Style Remix em loop com botão MUSIC ON/OFF
- **Efeitos sonoros 8-bit** sintetizados em tempo real (Web Audio API) em todas as interações
- **Placeholder automático de imagem** — se a foto de qualquer fighter falhar ao carregar, vira automaticamente um avatar com as iniciais do nome em pixel art
- **Easter egg do Konami Code** (↑↑↓↓←→←→BA) — ativa o "BOSS MODE" com paleta vermelha
- **Animação FIGHT!** ao confirmar as duplas
- **Totalmente responsivo** (desktop, tablet, mobile)
- **Zero dependências** — apenas HTML/CSS/JS puro, fontes do Google Fonts via CDN

## 🚀 Como hospedar no GitHub Pages

1. Crie um repositório novo no GitHub
2. Faça upload de todos os arquivos desta pasta (mantendo a estrutura)
3. Vá em **Settings → Pages**
4. Em "Source", selecione `Deploy from a branch` → `main` → `/ (root)`
5. Salve. Em ~1 minuto a página estará no ar em `https://seu-usuario.github.io/nome-do-repo/`

## 📁 Estrutura

```
.
├── index.html          # toda a aplicação (HTML + CSS + JS num arquivo só)
├── README.md
├── .gitignore
└── assets/
    ├── bgm.mp3         # trilha sonora (Techno Syndrome 16-bit remix)
    ├── fighter1.png    # Leonardo
    ├── fighter2.png    # Eduarda
    ├── fighter3.png    # Samantha
    ├── fighter4.png    # Stefane
    ├── fighter5.png    # Lucas
    ├── fighter6.png    # Danilo
    └── fighter8.png    # Renam
    # fighter-edmundo.png ← coloque aqui quando tiver a foto do Edmundo
```

## 🛠️ Como customizar

### Trocar nomes dos fighters
No `index.html`, procure pelos botões `<button class="fighter">` (linha ~640) e edite o `data-name` e o conteúdo do `<span class="name-tag">`.

### Adicionar a foto do Edmundo
Salve a foto dele como `assets/fighter-edmundo.png` (mesmo estilo das outras: fundo magenta/púrpura com splash). O placeholder some automaticamente.

### Trocar a música
Substitua o arquivo `assets/bgm.mp3`. Se preferir desativar a música externa e usar o chiptune sintetizado embutido, basta deletar o arquivo `bgm.mp3` — o sistema cai automaticamente no fallback.

### Mudar a paleta de cores
No `<style>` do `index.html`, edite as variáveis CSS `:root` (linhas ~10–22):
- `--primary` — amarelo arcade
- `--hot` — magenta
- `--cyan` — ciano
- `--team1` / `--team2` — cores das duplas

## ⚠️ Aviso de copyright

A trilha sonora `bgm.mp3` é um remix 16-bit do **Techno Syndrome** (The Immortals, 1993, Capcom — Mortal Kombat). Para uso interno em apresentação fechada de equipe geralmente é tolerado, mas para **publicação pública** (site online, redes sociais), considere:

- Substituir por música própria/licenciada, ou
- Deletar o `bgm.mp3` e usar o chiptune original sintetizado que já está embutido no código

## 🎮 Controles

| Ação | Como |
|------|------|
| Selecionar fighter | Clicar em qualquer card do grid |
| Remover de um slot | Clicar no slot já preenchido |
| Resetar tudo | Botão `RESET` |
| Iniciar duelo | Botão `FIGHT!` (ativa quando 4 selecionados) |
| Ligar/desligar música | Botão `♪ MUSIC` no canto superior direito |
| Easter egg | Konami Code: ↑ ↑ ↓ ↓ ← → ← → B A |

---

Built with ☕ and pixels.
