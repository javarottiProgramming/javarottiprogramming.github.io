# Javarotti AD

Página pública (GitHub Pages) dos jogos de Pedro Javarotti. Serve para tudo que uma loja ou rede de anúncio precisa ler numa URL pública:
**políticas de privacidade** e **`app-ads.txt`** (AdMob e outras redes), e o que mais surgir. Um só repositório para todos os jogos.

## Estrutura

```
app-ads.txt                  # UM arquivo na RAIZ, vale para todos os jogos
index.html                   # índice dos jogos
games/<jogo>/privacidade/    # política de privacidade do jogo (index.html)
games/<jogo>/admob/          # IDs e notas do AdMob do jogo (só documentação)
games/<jogo>/<plataforma>/   # outra plataforma/rede que precisar de página pública
_modelo-jogo/                # molde para jogo novo
```

Jogos hoje: `sem-pena`.

## Regra do app-ads.txt (importante)

A AdMob lê **só** `https://<domínio do desenvolvedor>/app-ads.txt`, na raiz. Arquivo dentro de `games/<jogo>/` **não é lido**.
Por isso o arquivo é único e ganha uma linha por rede/conta; não existe um por jogo. O domínio precisa ser o mesmo que está no campo
"site do desenvolvedor" da ficha da Play de cada jogo.

## Publicar jogo novo

1. Copiar `_modelo-jogo/` para `games/<slug-do-jogo>/` e escrever a política em `privacidade/index.html`.
2. Anotar os IDs do AdMob em `admob/README.md`.
3. Linkar o jogo no `index.html` da raiz.
4. Usar `https://<domínio>/games/<slug>/privacidade/` como URL da política na Play Console e no app.
5. Branch de feature + PR; nunca commit direto na `main`.

## Publicação (GitHub Pages)

Pages serve a `main`, pasta raiz. `.nojekyll` evita processamento. Para o `app-ads.txt` funcionar, o endereço da raiz precisa ser o
domínio do desenvolvedor na Play (ver `CLAUDE.md`).
