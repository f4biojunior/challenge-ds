# Apuração · Presidente de Challenge Land

Painel para acompanhar a prova: registre o distrito sorteado e as cartas de cada equipe, e veja quem venceu cada distrito, o andamento das regiões e qual carta usar.

## Como abrir

Abra o link da página no navegador. Antes de tudo, ela pede a senha de acesso. Depois, há dois modos, escolhidos no topo da página:

- **Jogo real**: a partida é compartilhada entre todos com acesso. Só funciona quando a página é aberta pelo Claude, com a conta de quem tem permissão no link. Na primeira vez, quem tem permissão de editor define a senha de administrador.
- **Modo teste**: tudo fica neste aparelho e não mexe no jogo real. Escolha quantas rodadas simular e toque em "Gerar partida simulada" para carregar a partida na tela.

## Regras

Seguem o regulamento da prova: 13 rodadas, 13 distritos em 6 regiões, 27 votos, Coringa com substituta de 5 minutos, desempates por região e no total. A recomendação de carta é uma estimativa por simulação, com o perfil de adversárias escolhido na tela.

## Observações

- As senhas não ficam no código. A página guarda só o hash (PBKDF2-SHA256, 200 mil iterações). Use senhas longas.
- O código é minificado para dificultar a leitura no navegador. Isso não é segurança: quem abre a página consegue ver a lógica.
- Reiniciar a partida ou restaurar uma cópia exige o modo administrador, com a senha de administrador. Quem não tem nível de editor no compartilhamento do link não consegue usar essa senha.
- Não há dependências: é um único arquivo HTML.
