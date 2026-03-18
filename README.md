# 🎬 Movie Reviews Dashboard (Now Playing)

Projeto de coleta, processamento e visualização de reviews de filmes em cartaz, utilizando dados da API do TMDb e web scraping de múltiplas fontes. Este Projeto foi desenvolvido para fins educacionais.

---

## 🚀 Visão Geral

Este projeto implementa um pipeline completo de dados que:

- Coleta filmes em cartaz via API 
- Seleciona os mais populares
- Extrai reviews e notas de diferentes plataformas 
- Traduz automaticamente os textos
- Gera visualizações com WordCloud
- Cria um dashboard HTML interativo

---

## 📊 Funcionalidades

### 🎥 1. Coleta de Filmes (TMDb API)

Consumo da API:
```
https://api.themoviedb.org/3/movie/now_playing
```

Dados coletados:
- Título (Português, Inglês e Original)
- Popularidade
- Data de lançamento
- Posters (PT e EN)

---

### 🔝 2. Seleção dos Top 10

- Critério: **Popularidade**
- Seleção automática dos 10 filmes mais populares em cartaz

---

### 🌐 3. Web Scraping de Reviews

Para cada um dos filmes selecionados:

Coleta de:
- Nota geral
- Reviews com notas dos usuários

Fontes:
- IMDb  
- Rotten Tomatoes  
- Metacritic  
- Letterboxd  

---

### 🌍 4. Tradução Automática

Utilizando:

```python
from deep_translator import GoogleTranslator
```

- Tradução de todas as reviews para:
  - Português 🇧🇷
  - Inglês 🇺🇸
- Identificação da língua original

---

### ☁️ 5. Geração de WordCloud

- Criação de nuvens de palavras com:
  - Reviews em português
  - Reviews em inglês
- WordClouds são geradas **sobre os posters dos filmes**

---

### 🖥️ 6. Dashboard HTML Interativo

Interface final contendo:

- 🎬 Poster do filme
- ⭐ Nota geral por fonte
- ☁️ Poster com WordCloud
- 💬 Reviews dos usuários

#### Funcionalidades interativas:

- 🔍 Filtro por fonte:
  - Todas
  - IMDb
  - Rotten Tomatoes
  - Metacritic
  - Letterboxd

- 🌍 Alternância de idioma:
  - Português
  - Inglês

---

## ⚠️ Observações

- Para acessar a API do TMDb, precisa criar uma conta e gerar a api_key
- O scraping pode quebrar caso os sites mudem a estrutura
