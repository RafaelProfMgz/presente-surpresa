# 💕 Presente - Carta Interativa para Geise

Uma página web interativa e responsiva criada com amor para o aniversário. Design Hello Kitty, animações personalizadas e sistema de música integrado.

---

## 📋 Funcionalidades

### ✉️ **Envelope Interativo**

- Animação de abertura com efeito hover
- Transição suave para o conteúdo principal
- Pétalas flutuantes decorativas

### 📝 **Seções Temáticas**

1. **Introdução**: Mensagem de boas-vindas com foto (personalizável)
2. **Carta Pessoal**: Texto handwritten style com linhas decorativas alinhadas
3. **Qualidades**: Grid de cards com emojis e características especiais
4. **Estante de Histórias**: Visual de livros coloridos representando momentos juntos
5. **Piquenique dos Sonhos**: Cena visual com xadrez decorativo
6. **Crochê & Arte**: Homenagem às criações manuais
7. **Valinhos de Amor**: Cards com promessas e datas ilimitadas
8. **Mensagem Final**: Grande coração com batida e mensagem de encerramento

### 🎵 **Sistema de Música**

- Botão flutuante com animação (bottom-right)
- Overlay para adicionar URLs de músicas
- Suporta Spotify e YouTube
- Indicador visual de reprodução (pulsação)
- Totalmente responsivo para mobile

### 🎨 **Design**

- Paleta de cores: Rosa, lavanda, amarelo suave, verde menta, bege
- Fontes personalizadas: Caveat (títulos), Patrick Hand (corpo), Quicksand (dados)
- Animações suaves e decorações com fita adesiva (washi tape)
- Totalmente responsivo (mobile-first)

---

## 🛠️ Como Usar

### 1. **Personalização Básica**

#### Adicionar Foto

Procure pela linha do `scrapbook-frame`:

```html
<div class="photo-placeholder">
  💑
  <span>coloque nossa foto aqui ♡</span>
</div>
```

Substitua o emoji `💑` pela sua foto real usando `<img>`:

```html
<img
  src="sua-foto.jpg"
  alt="Nossa foto"
  style="width: 100%; height: 100%; object-fit: cover; border-radius: 2px;"
/>
```

#### Editar Dados da Carta

Localize a seção `.carta-section` e edite o conteúdo:

```html
<p>Seu texto aqui...</p>
```

### 2. **Alterar Cores**

As cores estão definidas no `:root` do CSS:

```css
:root {
  --rosa-claro: #fce4ec;
  --rosa-medio: #f8bbd0;
  --rosa-forte: #f06292;
  --rosa-escuro: #e91e63;
  --creme: #fff8f0;
  --lavanda: #e8d5f5;
  --amarelo-suave: #fff9c4;
  --verde-menta: #e0f2f1;
  --bege: #faf0e6;
}
```

### 3. **Adicionar Música**

1. Clique no botão 🎵 (bottom-right)
2. Cole uma URL do Spotify ou YouTube
3. Clique em "Adicionar 🎶"
4. Clique em "▶️ Tocar" para reproduzir

#### Formatos Aceitos:

- **Spotify**: `https://open.spotify.com/track/[ID]`
- **YouTube**: `https://youtu.be/[ID]` ou `https://www.youtube.com/watch?v=`

---

## 📱 Responsividade

A página é otimizada para:

- **Desktop** (>1024px): Layout completo com todas as animações
- **Tablet** (768px-1024px): Ajustes de espaçamento
- **Mobile** (<768px): Otimizado para toque, player de música no canto superior esquerdo
- **Pequenos** (<600px): Texto reduzido, padding ajustado, elementos stacados

---

## 🎯 Estrutura do Código

### Principais Seções CSS

- `envelope-intro`: Animação inicial da envelope
- `carta`: Texto com linhas decorativas
- `recortes-grid`: Cards das qualidades
- `bookshelf`: Estante de livros
- `music-player`: Sistema de música

### Principais Funções JavaScript

- `openEnvelope()`: Abre a envelope inicial
- `createPetals()`: Cria pétalas flutuantes
- `addMusicFromURL()`: Adiciona música via URL
- `toggleAudio()`: Controla reprodução

---

## 🚀 Melhorias Futuras

- [ ] Integração oficial com Spotify Web API (requer OAuth)
- [ ] Upload de fotos direto na página
- [ ] Exportar como PDF
- [ ] Modo escuro
- [ ] Suporte a múltiplas línguas
- [ ] Animações de confete ao scroll
- [ ] Chat interativo com IA

---

## 💝 Especificações Técnicas

### Arquivos

- `index.html`: Todo o conteúdo (HTML + CSS + JS)

### Dependências

- Google Fonts (Caveat, Patrick Hand, Quicksand)
- Nenhuma biblioteca externa
- Totalmente offline após carregamento

### Compatibilidade

- Chrome/Edge: ✅ Total
- Firefox: ✅ Total
- Safari: ✅ Total
- IE11: ❌ Não suportado

---

## 📞 Suporte

Para questões ou melhorias, consulte:

1. Documentação em `/docs`
2. Comentários no código
3. Skill de customização em `.agent.md`

---

**Feito com ❤️ para tornar esse dia especial!**
