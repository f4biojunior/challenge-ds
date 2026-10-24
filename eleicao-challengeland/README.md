# Apuração · Presidente de Challenge Land

Painel para acompanhar a prova: registre o distrito sorteado e as cartas de cada equipe, e veja quem venceu cada distrito, o andamento das regiões e qual carta usar.

## Como abrir

Abra o link da página no navegador. Antes de tudo, ela pede a senha de acesso, que vale para os dois modos. Depois, escolha o modo no topo da página:

- **Jogo real**: a partida fica salva no navegador de quem está jogando. Para levar a partida para outro aparelho, use "Gerar cópia" e depois "Restaurar cópia" (esta última exige o modo administrador).
- **Modo teste**: tudo fica neste aparelho e não mexe no jogo real. Escolha quantas rodadas simular e toque em "Gerar partida simulada" para carregar a partida na tela.

## Senhas

- **Senha de acesso**: abre a página nos dois modos.
- **Senha de administrador**: liga o modo administrador, que permite reiniciar a partida real, desfazer a última rodada e restaurar cópias. Ela some quando a página é recarregada.

## Regras

Seguem o regulamento da prova: 13 rodadas, 13 distritos em 6 regiões, 27 votos, Coringa com substituta de 5 minutos, desempates por região e no total. A recomendação de carta é uma estimativa por simulação, com o perfil de adversárias escolhido na tela.

## Observações

- As senhas não ficam no código: a página guarda só o hash (PBKDF2-SHA256, 200 mil iterações). Use senhas longas.
- O código é minificado para dificultar a leitura no navegador. Isso não é segurança: quem abre a página consegue ver a lógica.
- Cada navegador tem a sua partida real. Duas pessoas em aparelhos diferentes não veem a mesma partida sem uma cópia.
- Não há dependências: é um único arquivo HTML.
