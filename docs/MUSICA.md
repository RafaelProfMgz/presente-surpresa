# 🎵 Guia do Sistema de Música

## Como Funciona

O sistema de música permite que você adicione músicas e playlists/álbuns do Spotify diretamente na página!

### 🎯 Passo-a-Passo de Uso

#### **TAB 1: Música Única** 🎶

1. Clique no botão 🎵 (canto inferior direito)
2. Verifique se está na aba **🎶 Música**
3. Cole uma URL do Spotify ou YouTube
4. Clique "Adicionar 🎶"
5. Clique "▶️ Tocar"

#### **TAB 2: Playlist/Álbum** 📋

1. Clique no botão 🎵
2. Clique na aba **📋 Playlist**
3. Cole uma URL de álbum ou playlist do Spotify
4. Clique "Carregar 📀"
5. O player do Spotify aparece automaticamente
6. Clique em qualquer faixa para selecionar

---

## 🎶 Fontes de Música Suportadas

### ✅ Spotify - Música Única

**Onde pegar o link?**

1. Abra Spotify (web ou app)
2. Procure pela música
3. Botão "Compartilhar" → "Copiar link da música"
4. Será algo como: `https://open.spotify.com/track/1234567890`

**Exemplo:**

```
https://open.spotify.com/track/6rqhFgbbKwnb9MLmUQDvDm
```

### ✅ Spotify - Álbum/Playlist

**Onde pegar o link?**

1. Abra Spotify
2. Procure pelo álbum ou playlist
3. Botão "Compartilhar" → "Copiar link"
4. Será algo como:
   - `https://open.spotify.com/album/5CUFurrJe05hnz189d5mDK`
   - `https://open.spotify.com/playlist/37i9dQZF1DX...`

**Exemplos:**

```
# Álbum
https://open.spotify.com/album/5CUFurrJe05hnz189d5mDK

# Playlist
https://open.spotify.com/playlist/37i9dQZF1DXcBWIGoVmsDQ

# Com localização (também funciona)
https://open.spotify.com/intl-pt/album/5CUFurrJe05hnz189d5mDK
```

**Você vai ver:**

- 🎵 Embed interativo do Spotify com reprodutor completo
- 📋 Lista de faixas para clicar
- ✅ Todas as funcionalidades do Spotify funcionam

### ✅ YouTube

**Onde pegar o link?**

1. Encontre o vídeo/música no YouTube
2. Botão "Compartilhar"
3. Copie o link (alguma das formas abaixo)

**Formatos aceitos:**

```
https://youtu.be/E6hCoLXH6qE
https://www.youtube.com/watch?v=E6hCoLXH6qE
```

---

## 🔧 Características da Nova Playlist

✨ **Duas abas separadas**

- Música Única: Para uma música específica
- Playlist: Para álbuns e playlists

🎯 **Player Interativo do Spotify**

- Reprodutor completo integrado
- Botões de play/pause/volume
- Seeker de posição
- Lista de faixas

📋 **Seleção Rápida de Faixas**

- Clique em qualquer faixa
- Visual de seleção (destaque em rosa)
- Feedback visual instantâneo

🎨 **Interface Responsiva**

- Funciona perfeito em mobile
- Overlay se adapta ao tamanho da tela
- Scroll automático para playlists longas

---

## 💾 Para Áudio Local

Se você tiver um arquivo MP3 e quer que toque direto sem pedir:

1. Coloque o arquivo `.mp3` na mesma pasta que `index.html`
2. Encontre esta linha no HTML:

```html
<audio id="audioPlayer" style="display: none;"></audio>
```

3. Substitua por:

```html
<audio id="audioPlayer" style="display: none;" controls>
  <source src="sua-musica.mp3" type="audio/mpeg" />
</audio>
```

4. Atualize a função `toggleAudio()` para ativar automáticamente

---

## 🎵 Playlist Recomendada para Presente

A URL que você passou:

```
https://open.spotify.com/intl-pt/album/5CUFurrJe05hnz189d5mDK
```

Cole no Tab **📋 Playlist** para ver todas as faixas!

---

## ⚠️ Troubleshooting

### "A música não toca"

- ✅ Verifique se a URL é válida
- ✅ Cheque se tem http:// ou https://
- ✅ Spotify pode exigir estar logado para embed
- ✅ YouTube pode bloquear por política CORS em alguns navegadores

### "As faixas não aparecem"

- ✅ Aguarde o Spotify embed carregar (5-10 segundos)
- ✅ Verifique conexão de internet
- ✅ Cole de novo a URL se não funcionou

### "Como faço música tocar automático?"

- ✅ Edite a função `openEnvelope()` para chamar `toggleAudio()`
- ✅ Ou adicione `autoplay` na tag `<audio>`

### "Posso usar outras plataformas?"

- ❌ Formato atual aceita apenas Spotify/YouTube
- ✅ Você pode adicionar SoundCloud com padrão regex similar

---

## 🚀 Melhorias Futuras

- [ ] Conectar com Spotify Web API (requer OAuth)
- [ ] Agregar SoundCloud
- [ ] Apple Music
- [ ] Deezer
- [ ] Upload direto de MP3
- [ ] Playlist completa com reordenação
- [ ] Visualizador de espectro
- [ ] Histórico de músicas

---

**Dúvida? Veja a documentação geral em `/docs/README.md`**
