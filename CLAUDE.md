# Javarote AD

Repositório **público** e comum a todos os jogos de Pedro Javarotti: políticas de privacidade e `app-ads.txt`. Tudo em português.
Estrutura e regras: `README.md`.

## Para o Claude Code

- **Todo jogo novo** que for publicado na Play (ou outra loja) passa por aqui: antes do envio, propor ao Pedro criar `games/<slug>/` a partir de `_modelo-jogo/`, escrever a política de privacidade e conferir o `app-ads.txt`. Lembrar disso sem esperar ser pedido.
- `app-ads.txt` é **um só, na raiz**. Nunca criar um por jogo. Rede nova de anúncio = linha nova nele.
- Nada secreto aqui (repo público): sem senhas, chaves de assinatura, e-mails pessoais além do contato já usado nas políticas, dados de pagamento. IDs do AdMob são públicos.
- Política publicada é a fonte da URL que vai na Play Console e no app; mudar o texto pede revisar a data "Última atualização".
- Nunca commitar na `main`: branch de feature + PR. Primeiro push: `git push origin <branch>:<branch>`.
