# 🎨 Guia de Customização

## Personalizações Comuns

### 1️⃣ Mudar a Foto do Casal

**Localização**: Linha ~1160 no `index.html`

**Antes:**

```html
<div class="photo-placeholder">
  💑
  <span>coloque nossa foto aqui ♡</span>
</div>
```

**Depois (com imagem):**

```html
<div class="photo-placeholder">
  <img
    src="path/to/sua-foto.jpg"
    alt="Nossa foto"
    style="width: 100%; height: 100%; object-fit: cover; border-radius: 2px;"
  />
</div>
```

---

### 2️⃣ Personalizar a Carta

**Localização**: Seção `.carta-section` (~linha 1194)

Edite o conteúdo dos parágrafos mantendo a estrutura:

```html
<p>Meu amor,</p>
<p>Seu novo texto aqui...</p>
<p class="assinatura">
  Com todo meu amor,<br />
  seu namorado 💌
</p>
```

---

### 3️⃣ Alterar as Qualidades

**Localização**: Seção `.qualidades-section` (~linha 1216)

Cada card tem a estrutura:

```html
<div class="recorte fade-in" style="--rotation: -2deg">
  <span class="emoji">🌸</span>
  <h3>Sua gentileza</h3>
  <p>Você trata o mundo com uma delicadeza que me encanta</p>
</div>
```

- **emoji**: Mude para qualquer emoji
- **h3**: Título da qualidade
- **p**: Descrição
- **--rotation**: Ângulo de rotação (-3deg a 3deg)

---

### 4️⃣ Editar a Estante de Livros

**Localização**: Seção `.livros-section` (~linha 1250)

Cada livro:

```html
<div
  class="book"
  style="height: 140px; background: linear-gradient(180deg, #f48fb1, #e91e63);"
>
  Nosso 1° encontro
</div>
```

- **height**: Altura do livro (120-170px recomendado)
- **background**: Gradiente de cores
- **Texto**: Título do "livro"

---

### 5️⃣ Mudar Cores Globais

**Localização**: CSS `:root` (~linha 15)

```css
:root {
  --rosa-claro: #fce4ec; /* Cor de fundo principal */
  --rosa-medio: #f8bbd0; /* Cor secundária */
  --rosa-forte: #f06292; /* Cor dos textos principais */
  --rosa-escuro: #e91e63; /* Cor de destaque */
  --creme: #fff8f0; /* Cor de fundo neutral */
  --lavanda: #e8d5f5; /* Cor pastel */
  --amarelo-suave: #fff9c4; /* Cor pastel clara */
  --verde-menta: #e0f2f1; /* Cor pastel fria */
  --bege: #faf0e6; /* Cor quente */
}
```

Mude os valores HEX para suas cores preferidas.

---

### 6️⃣ Customizar os Valinhos

**Localização**: Seção `.promessas-section` (~linha 1320)

Cada vale:

```html
<div class="vale fade-in">
  <div class="vale-emoji">🎬</div>
  <h3>Vale 1 Noite de Filme</h3>
  <p>Com cobertor, pipoca e nenhuma interrupção</p>
  <p class="validade">Validade: para sempre ♡</p>
</div>
```

- **vale-emoji**: Mude o emoji
- **h3**: Nome do vale
- **p**: Descrição
- **validade**: Texto de validade

---

### 7️⃣ Mudar Fontes

**Localização**: Tag `<link>` no `<head>` (~linha 4)

```html
<link
  href="https://fonts.googleapis.com/css2?family=Caveat:wght@400;600;700&family=Patrick+Hand&family=Quicksand:wght@300;400;500;600&display=swap"
  rel="stylesheet"
/>
```

Adicione novas fontes e atualize no CSS.

---

### 8️⃣ Desabilitar Animações

Para melhor performance em móvel, você pode desabilitar algumas animações:

**Remova ou comente:**

```css
@keyframes fall { ... }      /* Pétalas caindo */
@keyframes heartbeat { ... }  /* Coração pulsando */
@keyframes bounce { ... }     /* Bounce do rosto */
```

---

## 🎵 Sistema de Música - Guia Avançado

### Adicionar Pré-carregada (Offline)

Se você tiver um arquivo MP3, substitua:

```html
<audio id="audioPlayer" style="display: none;"></audio>
```

Por:

```html
<audio id="audioPlayer" style="display: none;controls">
  <source src="sua-musica.mp3" type="audio/mpeg" />
  Seu navegador não suporta audio.
</audio>
```

### Integração com Spotify (Avançado)

Para embed interativo do Spotify, você precisa:

1. Registrar um app em https://developer.spotify.com
2. Obter Client ID
3. Usar Spotify Web API

---

## 🐛 Troubleshooting

### A carta está desalinhada

- Ajuste `line-height` em `.carta` (recomendado: 2em)
- Ajuste `background-size` para corresponder

### Mobile vê elementos sobrepostos

- Redimensione em `@media (max-width: 600px)`
- Reduza padding/margin

### Música não toca

- Verifique se a URL é válida
- Spotify Web embed requer permissões
- YouTube pode ter bloqueio de CORS

### Fontes não carregam

- Verifique conexão de internet
- Tente incluir fontes localmente

---

## 📚 Referências Rápidas

| Elemento        | Localização CSS  | Cores Padrão             |
| --------------- | ---------------- | ------------------------ |
| Títulos         | `.section-title` | `--rosa-forte`           |
| Fundo           | `body`           | `--creme`                |
| Cards           | `.recorte`       | `white` + gradiente      |
| Linhas da Carta | `.carta`         | `#f8bbd0`                |
| Botão Música    | `.music-toggle`  | `white` / `--rosa-claro` |

---

**Dúvidas? Veja o arquivo principal para referências!**
