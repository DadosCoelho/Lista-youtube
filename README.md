# 📺 Lista YouTube

Gerenciador de listas de estudo no YouTube. Organize seus vídeos em listas, acompanhe o progresso e use IA para montar playlists automaticamente.

## Funcionalidades

- **Listas de estudo** — crie e organize vídeos por tema
- **Acompanhamento de progresso** — marque vídeos como assistidos e veja o percentual por lista
- **Gerador de prompt IA** — questionário guiado que gera um prompt pronto para pedir vídeos ao ChatGPT/Gemini/etc.
- **Importar resposta da IA** — cole o JSON retornado pela IA e os vídeos são adicionados automaticamente
- **Salvar na pasta** — persiste `yt_lista.json` localmente via File System Access API
- **Exportar/Importar backup** — backup manual em JSON
- **Tema claro/escuro**
- **Layout responsivo** — mobile, tablet e desktop (sidebar)

## Como usar

Abra o arquivo `app.html` diretamente no navegador (Chrome/Edge recomendado para suporte à File System Access API).

Nenhum servidor ou instalação necessária.

## Fluxo com IA

1. Crie uma lista → clique em **Usar IA**
2. Preencha o questionário (nível, idioma, formato, quantidade…)
3. Copie o prompt gerado
4. Cole no ChatGPT, Gemini ou outro LLM e peça a resposta em JSON
5. Cole o JSON retornado no campo **Importar resposta** → os vídeos são adicionados à lista

## Estrutura

```
app.html          # Aplicação completa (HTML + CSS + JS em arquivo único)
index.html        # Tela de entrada
.gitignore
README.md
```

> Os dados ficam em `dados_lista_youtube/yt_lista.json` (ignorado pelo git — não é versionado).

## Tecnologias

- HTML/CSS/JS puro — sem frameworks, sem build
- File System Access API
- IndexedDB (persistência do handle de pasta)
- localStorage (dados da sessão)
- Google Fonts — Nunito
