# Apuração · Presidente de Challenge Land

Painel para acompanhar a prova: registre o distrito sorteado e as cartas de cada equipe, e veja quem venceu cada distrito, o andamento das regiões e qual carta usar.

## Como abrir

Abra o arquivo `index.html` no navegador. Há dois modos, escolhidos no topo da página:

- **Jogo real**: a partida é compartilhada entre todos com acesso. Só funciona quando a página é aberta pelo Claude, com a conta de quem tem permissão no link. A primeira abertura pede duas senhas (acesso e administrador).
- **Modo teste**: tudo fica neste aparelho e não mexe no jogo real. Escolha quantas rodadas simular e toque em "Gerar partida simulada" para carregar a partida na tela.

## Regras

Seguem o regulamento da prova: 13 rodadas, 13 distritos em 6 regiões, 27 votos, Coringa com substituta de 5 minutos, desempates por região e no total. A recomendação de carta é uma estimativa por simulação, com o perfil de adversárias escolhido na tela.

## Observações

- As senhas não ficam no código. A checagem acontece no navegador, com hash (PBKDF2-SHA256). Use senhas longas.
- O modo administrador só serve para quem tem nível de editor no compartilhamento do link.
- Não há dependências: é um único arquivo HTML.
