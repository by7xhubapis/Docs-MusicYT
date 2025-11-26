<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/0xme/0xme/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/0xme/0xme/output/github-contribution-grid-snake.svg">
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/0xme/0xme/output/github-contribution-grid-snake.svg">
</picture>

## 1) Pesquisar música no **YouTube**

**Exemplo**
```
GET https://7xhub-apis.cloud/api/music/yt-search?q={query}&auth={auth_key}
```

**Resposta (200)**
```json
{
  "developer": "7XHUB APIS",
  "status": "success",
  "result": {
    "id": "rOemX8-L2CI",
    "title": "ANAVITÓRIA - Ai, Amor (Audio)",
    "channel": {
      "id": "UCaRC1kPSc3CcyVT1ddlbVGA",
      "name": "ANAVITÓRIA",
      "url": "https://youtube.com/channel/UChz6hFYw9Qu6iwbEChRfNyA"
    },
    "duration": "3:42",
    "duration_seconds": 222,
    "views": 53423721,
    "published": "7 years ago",
    "published_at": "03/08/2018, 00:00:05",
    "url": "https://youtu.be/rOemX8-L2CI",
    "thumbnails": {
      "default": "https://i.ytimg.com/vi/rOemX8-L2CI/default.jpg",
      "medium": "https://i.ytimg.com/vi/rOemX8-L2CI/mqdefault.jpg",
      "high": "https://i.ytimg.com/vi/rOemX8-L2CI/hqdefault.jpg",
      "standard": "https://i.ytimg.com/vi/rOemX8-L2CI/sddefault.jpg",
      "maxres": "https://i.ytimg.com/vi/rOemX8-L2CI/maxresdefault.jpg"
    },
    "statistics": {
      "views": "53423721",
      "likes": "366158",
      "comments": "5452",
      "definition": "hd"
    }
  }
}
```

**Erros**
- 400 `{ "type": "invalid_request" }`
- 404 `{ "type": "no_results" }`
- 500 `{ "type": "erro_interno" }`
---
## 2) Extrair MP3 do **YouTube**

**Exemplo**
```
GET https://7xhub-apis.cloud/api/music/yt-mp3?q={query}&auth={auth_key}
```

**Resposta (200)**
- **A api sempre retornará "Content-Type: audio/mpeg", exemplo:**
[![Exemplo Resposta (200)](https://files.catbox.moe/l7wa2h.jpg)](https://7xhub-api.squareweb.app)

**Erros**
- 400 `{ "type": "invalid_request" }`
- 404 `{ "type": "mp3_not_found" }`
- 500 `{ "type": "erro_interno" }`
- 504 `{ "type": "timeout" }`
---
## 3) Extrair MP4 do **YouTube**

**Exemplo**
```
GET https://7xhub-apis.cloud/api/music/yt-mp4?q={query}&auth={auth_key}
```

**Resposta (200)**
- **A api sempre retornará "Content-Type: video/mp4" - Ou "Content-Type: video/webm", exemplo:**
[![Exemplo Resposta (200)](https://files.catbox.moe/kqh4t8.jpg)](https://7xhub-api.squareweb.app)

**Erros**
- 400 `{ "type": "invalid_request" }`
- 404 `{ "type": "mp4_not_found" }`
- 500 `{ "type": "erro_interno" }`
- 504 `{ "type": "timeout" }`
---
