# Votação de ideias · JUNITEC

Mini app para equipas da JUNITEC escolherem as melhores ideias depois de um brainstorm. Cada pessoa vota no seu telemóvel e tudo actualiza em tempo real.

**Abrir a app:** https://miguel-galrito.github.io/o-nosso-repo/

## Como se usa

1. Uma pessoa abre a app, carrega em **Criar sala** e depois em **Copiar link da sala**, e envia o link ao grupo.
2. Toda a gente escreve as ideias do brainstorm em **1. Ideias**.
3. Cada pessoa escreve o seu nome em **3. O teu voto**, distribui os votos (3 por omissão, e pode pôr vários na mesma ideia) e carrega em **Entregar voto**.
4. Quando a última pessoa entrega o voto, o ranking aparece em todos os ecrãs.
5. **Copiar resultado** ou **Exportar CSV** para levar o ranking para o relatório.

## Voto secreto

- Até ser entregue, o voto só existe no teu browser.
- Depois de entregue, os outros só vêem que já votaste, não em que ideias.
- O ranking fica escondido até toda a gente votar, para ninguém ser influenciado. **Revelar já** serve para quando alguém sai a meio.
- **Nova votação** começa outra ronda com as mesmas ideias e pessoas.

## Como funciona por dentro

- Um só ficheiro, `index.html`, com HTML, CSS e JavaScript, sem frameworks e sem chaves de API.
- Cada sala é um tópico do serviço público [ntfy.sh](https://ntfy.sh). Cada acção (ideia, pessoa, voto) é uma mensagem nesse tópico. Cada browser lê as mensagens por ordem e reconstrói o mesmo estado.
- O código da sala vai no link (`#sala=...`) e é aleatório.

## Limites

- As mensagens ficam no ntfy.sh cerca de 12 horas. Depois a sala fica vazia.
- Quem tiver o link da sala consegue ver as mensagens. **Não ponham dados confidenciais nem dados de clientes.**

## Como contribuir

O `main` está protegido. Cada mudança entra por pull request, com a aprovação de um colega:

```
git switch main
git pull
git switch -c nome-da-melhoria
# editar o index.html
git add index.html
git commit -m "Descreve a melhoria"
git push -u origin nome-da-melhoria
```

---

Feito pela JUNITEC na formação de GitHub, com a skill `junitec-mini-app`.
