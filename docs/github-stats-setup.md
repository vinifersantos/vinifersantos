# 🛰️ Deploy próprio do GitHub Stats (cards à prova de rate-limit)

Os cards de estatísticas do README usam o projeto [github-readme-stats](https://github.com/anuraghazra/github-readme-stats).
A instância pública (`github-readme-stats.vercel.app`) é gratuita e **muito** requisitada, então
às vezes quebra por _rate-limit_. Subindo a sua própria instância no Vercel, os cards
nunca mais falham.

> Tempo estimado: ~5 minutos. Custo: zero (plano gratuito do Vercel).

---

## 1. Faça um fork do projeto

Acesse e clique em **Fork**:
👉 https://github.com/anuraghazra/github-readme-stats

---

## 2. Crie um token do GitHub (Personal Access Token)

1. Vá em **Settings → Developer settings → Personal access tokens → Tokens (classic)**
   👉 https://github.com/settings/tokens
2. Clique em **Generate new token (classic)**.
3. Dê um nome (ex.: `github-readme-stats`).
4. Marque **apenas** o escopo `repo` (ou nenhum, se só quiser stats públicas).
5. Gere e **copie o token** (você só vê ele uma vez).

---

## 3. Faça o deploy no Vercel

1. Entre em https://vercel.com com sua conta do GitHub.
2. **Add New → Project** e importe o **seu fork** do `github-readme-stats`.
3. Em **Environment Variables**, adicione:

   | Name  | Value                |
   | :---- | :------------------- |
   | `PAT_1` | _cole seu token aqui_ |

4. Clique em **Deploy**.
5. Ao terminar, copie a URL gerada, algo como:
   `https://SEU-PROJETO.vercel.app`

---

## 4. Troque as URLs no README

No `README.md`, na seção **📊 Indicadores de bordo**, troque o domínio
`github-readme-stats.vercel.app` pelo seu domínio do Vercel.

Antes:

```
https://github-readme-stats.vercel.app/api?username=vinifersantos&...
```

Depois:

```
https://SEU-PROJETO.vercel.app/api?username=vinifersantos&...
```

> 💡 Me mande sua URL do Vercel que eu faço essa troca pra você automaticamente.

---

## Pronto 🖖

Seus cards agora rodam na sua própria nave — sem depender da instância pública lotada.

```txt
"Make it so."
```
