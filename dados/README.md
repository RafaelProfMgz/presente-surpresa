# 🎵 Gerenciador de Músicas e Playlists

## Como Funciona

O arquivo `dados/musicas.json` armazena todas as suas músicas e playlists favoritas. Quando você adiciona uma música ou playlist pela interface do site, ela é salva automaticamente no **localStorage** (memória do navegador).

## 📁 Arquivo de Dados

**Localização**: `dados/musicas.json`

### Estrutura

```json
{
  "musicas": [ ... ],    // Suas músicas individuais
  "playlists": [ ... ],  // Suas playlists/álbuns
  "favoritas": [ ... ]   // IDs das suas favoritas
}
```

---

## 🎶 Como Adicionar Músicas Manualmente

### 1. Abra `dados/musicas.json`

### 2. Adicione na seção "musicas":

```json
{
  "id": "3",
  "titulo": "Nome da Música",
  "artista": "Nome do Artista",
  "url": "https://open.spotify.com/track/SEU_ID_AQUI",
  "tipo": "spotify"
}
```

### 3. Onde pegar o ID?

**No Spotify:**

1. Abra Spotify
2. Procure a música
3. Copie o link: `https://open.spotify.com/track/`**`6rqhFgbbKwnb9MLmUQDvDm`**
4. O ID é a parte final: `6rqhFgbbKwnb9MLmUQDvDm`

**Exemplo completo:**

```json
{
  "id": "3",
  "titulo": "Just the Two of Us",
  "artista": "Grover Washington Jr.",
  "url": "https://open.spotify.com/track/4fzsfWzEQVpIyT76F8h9gP",
  "tipo": "spotify"
}
```

---

## 📋 Como Adicionar Playlists/Álbuns

### Seção "playlists":

```json
{
  "id": "playlist_2",
  "nome": "Nossos Momentos",
  "url": "https://open.spotify.com/playlist/SEU_ID_AQUI",
  "tipo": "playlist",
  "descricao": "Uma descrição linda pra sua playlist"
}
```

### Tipos suportados:

- `"playlist"` - Playlist do Spotify
- `"album"` - Álbum (como o que você passou)
- `"youtube"` - Vídeo do YouTube

**Exemplo:**

```json
{
  "id": "playlist_2",
  "nome": "Músicas Românticas",
  "url": "https://open.spotify.com/playlist/37i9dQZF1DXcBWIGoVmsDQ",
  "tipo": "playlist",
  "descricao": "Nossas músicas favoritas"
}
```

---

## 💾 LocalStorage - Salvamento Automático

Quando você usa a interface do site:

1. **Adiciona uma música** → Salva no localStorage automaticamente
2. **Adiciona uma playlist** → Salva no localStorage automaticamente
3. **Marca como favorita** → Salva no localStorage

### Como ver o que foi salvo?

**No navegador (F12):**

1. Abra DevTools (F12)
2. Vá para "Application" ou "Aplikácia"
3. Clique em "LocalStorage"
4. Procure pela URL do site
5. Verá uma chave: `apresento_musicas`

---

## 🔄 Sincronização

```
Arquivo musicas.json (você edita)
            ↓
   index.html carrega
            ↓
   LocalStorage (navegador salva)
            ↓
  Interface atualiza
```

**Processo:**

1. Você edita `musicas.json` → Reinicie o navegador
2. Usuario adiciona via interface → Salva no localStorage
3. Próxima vez que abrir → Carrega do localStorage

---

## 📝 Objeto de Música - Campos Completos

```json
{
  "id": "identificador_único",
  "titulo": "Nome da música",
  "artista": "Nome do artista",
  "url": "link_completo",
  "tipo": "spotify|youtube|youtube-music",
  "data_adicionada": "2026-04-01" // OPCIONAL
}
```

### Campo "tipo":

- `"spotify"` - Link do Spotify (música/track)
- `"youtube"` - Link do YouTube
- `"youtube-music"` - YouTube Music

---

## 📝 Objeto de Playlist - Campos Completos

```json
{
  "id": "identificador_único",
  "nome": "Nome da playlist",
  "url": "link_completo",
  "tipo": "playlist|album|youtube",
  "descricao": "Uma descrição bonita",
  "genero": "romântico|pop|indie", // OPCIONAL
  "data_adicionada": "2026-04-01" // OPCIONAL
}
```

---

## 🎯 Exemplo Completo Editado

```json
{
  "musicas": [
    {
      "id": "1",
      "titulo": "Lover",
      "artista": "Taylor Swift",
      "url": "https://open.spotify.com/track/1BxfuPKGuaTgP7aM0frO2M",
      "tipo": "spotify"
    },
    {
      "id": "2",
      "titulo": "Perfect",
      "artista": "Ed Sheeran",
      "url": "https://open.spotify.com/track/0VjIjW4GlUZAMYd2vXMwbk",
      "tipo": "spotify"
    },
    {
      "id": "3",
      "titulo": "At Last",
      "artista": "Etta James",
      "url": "https://open.spotify.com/track/3qm84nBvXcWhTuq4dues5M",
      "tipo": "spotify"
    }
  ],
  "playlists": [
    {
      "id": "playlist_1",
      "nome": "Álbum Especial",
      "url": "https://open.spotify.com/intl-pt/album/5CUFurrJe05hnz189d5mDK",
      "tipo": "album",
      "descricao": "A playlist que você adicionou para nosso presente especial"
    },
    {
      "id": "playlist_2",
      "nome": "Músicas Românticas",
      "url": "https://open.spotify.com/playlist/37i9dQZF1DXcBWIGoVmsDQ",
      "tipo": "playlist",
      "descricao": "Nossas favoritas para momentos especiais"
    }
  ],
  "favoritas": [
    {
      "id": "1",
      "tipo": "musica",
      "data_adicionada": "2026-04-01"
    },
    {
      "id": "playlist_1",
      "tipo": "playlist",
      "data_adicionada": "2026-04-01"
    }
  ]
}
```

---

## ⚠️ Importante

- Mantenha a sintaxe JSON válida (vírgulas, aspas, etc.)
- Use caminhos COMPLETOS para URLs
- IDs devem ser únicos dentro da categoria
- Se editar, **reinicie o navegador** para carregar as mudanças

---

## 🔗 Referência Rápida de Links

### Spotify Música

```
https://open.spotify.com/track/ID
```

### Spotify Playlist

```
https://open.spotify.com/playlist/ID
```

### Spotify Álbum

```
https://open.spotify.com/album/ID
ou
https://open.spotify.com/intl-pt/album/ID
```

### YouTube

```
https://youtu.be/ID
ou
https://www.youtube.com/watch?v=ID
```

---

**Dúvida? Veja [MUSICA.md](../docs/MUSICA.md) na documentação!**
