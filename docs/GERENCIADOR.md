# 🎵 Gerenciador de Músicas - Guia Completo

## Visão Geral

O gerenciador de músicas permite controlar todas as suas músicas e playlists salvas de forma completa e intuitiva.

---

## 🎵 Como Acessar

### Desktop

1. Clique no botão **⚙️** (canto inferior direito)
2. O painel desliza da direita

### Mobile

1. Clique no botão **⚙️** (canto inferior esquerdo)
2. O painel sobe da base da tela

---

## 📑 Abas Disponíveis

### 🎶 Músicas

Gerencia suas músicas individuais do Spotify ou YouTube.

**Ações:**

- 🔍 **Buscar** - Digite para filtrar por título ou artista
- ♡ **Favoritar** - Clique para marcar como favorita
- ✏️ **Editar** - Mude o nome ou artista
- 🗑️ **Deletar** - Remova a música

### 📋 Playlists

Gerencia suas playlists e álbuns do Spotify.

**Ações:**

- 🔍 **Buscar** - Filter por nome
- ♡ **Favoritar** - Marque como favorita
- ✏️ **Editar** - Renomeie a playlist
- 🗑️ **Deletar** - Remova a playlist

### ⚙️ Configurações

Ferramentas para backup e restauração de dados.

---

## 🔧 Guia de Ações

### Buscar Música/Playlist

```
1. Abra qualquer aba (🎶 ou 📋)
2. Digite no campo "🔍 Buscar..."
3. A lista filtra em tempo real
4. Limpe o campo para ver tudo novamente
```

### Favoritar Item

```
1. Abra a aba desejada
2. Clique no botão ♡ do item
3. Button fica destacado = favoritado
4. Clique novamente para desmarcar
```

### Editar Música

```
1. Na aba 🎶 Músicas
2. Clique em ✏️ na música
3. Atualize o título
4. Atualize o artista
5. Salva automaticamente
```

### Editar Playlist

```
1. Na aba 📋 Playlists
2. Clique em ✏️ na playlist
3. Digite o novo nome
4. Salva automaticamente
```

### Deletar Item

```
1. Abra a aba (🎶 ou 📋)
2. Clique em 🗑️ do item
3. Item desaparece imediatamente
4. Impossível desfazer (tá deletado!)
```

---

## 📥 Exportar Dados (Backup)

### Por quê?

Fazer backup de todas suas músicas e playlists para não perder dados.

### Como?

```
1. Clique no botão ⚙️
2. Vá para aba "⚙️ Configurações"
3. Clique em "📤 Baixar JSON"
4. Arquivo baixa: "musicas-DD-MM-AAAA.json"
5. Guarde em local seguro!
```

### Arquivo gerado

```json
{
  "musicas": [
    {
      "id": 1234,
      "titulo": "Song Name",
      "artista": "Artist Name",
      "url": "https://...",
      "tipo": "spotify",
      "data_adicionada": "01/04/2026"
    }
  ],
  "playlists": [ ... ],
  "favoritas": [ ... ]
}
```

---

## 📥 Importar Dados (Restaurar)

### Quando usar?

- Restaurar backup de outro dispositivo
- Mesclar dados de outro arquivo
- Recuperar após limpar dados

### Como?

#### Opção 1: Mesclar com existentes

```
1. Clique em ⚙️ → Configurações
2. Clique em "📥 Carregar JSON"
3. Selecione seu arquivo JSON
4. Escolha "SIM" para mesclar
5. Novos itens adicionados aos existentes
```

#### Opção 2: Substituir tudo

```
1. Clique em ⚙️ → Configurações
2. Clique em "📥 Carregar JSON"
3. Selecione seu arquivo JSON
4. Escolha "NÃO" para substituir
5. Todos os dados são sobrescritos
⚠️ Cuidado: dados atuais são perdidos!
```

---

## 🗑️ Limpar Todos os Dados

### ⚠️ Aviso: AÇÃO IRREVERSÍVEL!

```
1. Clique em ⚙️ → Configurações
2. Clique no botão vermelho "Limpar Dados"
3. Confirme a primeira mensagem
4. Confirme a segunda mensagem
5. TUDO deletado!
```

**Dica:** Sempre faça export antes de limpar!

---

## 💾 Como Funciona o Armazenamento

### Local

- **Armazena:** localStorage do navegador
- **Persiste:** Enquanto não limpar cache/histórico
- **Limite:** ~5MB por site
- **Segurança:** Dados locais, não enviados a servidor

### Sincronização

- Adicionar música → salva automaticamente em localStorage
- Deletar música → remove de localStorage
- Editar música → atualiza em localStorage
- Tudo acontece instantaneamente!

---

## 🎯 Dicas & Truques

### 💡 Tip 1: Organização

- Use nomes descritivos para playlists
- Adicione artista nas músicas
- Use favoritos para destacar especiais

### 💡 Tip 2: Backup Regular

- Faça export mensalmente
- Guarde em múltiplos locais
- Nomeie com datas: "musicas-01-04-2026.json"

### 💡 Tip 3: Busca Eficiente

- Busca é case-insensitive
- Busca título E artista
- Tipo: primeira letra (s, a) funciona bem

### 💡 Tip 4: Transferência de Dados

```
Device A:
1. ⚙️ → Configurações → Exportar
2. Guarda arquivo

Device B:
1. ⚙️ → Configurações → Importar
2. Seleciona arquivo
3. Mescla dados!
```

---

## 🐛 Troubleshooting

### Problema: Dados desapareceram após recarregar

**Solução:** localStorage pode ser limpo junto com cache

- Tente export em arquivo para backup
- Configure navegador para não limpar localStorage

### Problema: Import não funciona

**Solução:** Verifique o arquivo JSON

- Deve ter estrutura: `{ "musicas": [], "playlists": [], "favoritas": [] }`
- Valide em: https://jsonlint.com

### Problema: Muitos itens, busca lenta

**Solução:** Limite é browser/device

- Limpe itens não usados
- Considere fazer export e criar novo arquivo

### Problema: Mudei a música mas não meteu

**Solução:** Tente novamente

- Às vezes prompt pode falhar
- Certifique-se de clicar OK, não Cancel

---

## 🎁 presente para Geise ❤️

**O gerenciador foi criado para facilitar:**

- ✅ Adicionar suas músicas favoritas
- ✅ Organizar playlists especiais
- ✅ Salvar seus itens preferidos (favoritos)
- ✅ Backup de dados importante
- ✅ Sincronizar entre dispositivos

**Divirta-se! 🎵**
