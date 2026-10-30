# Apuração · Presidente de Challenge Land

Painel para acompanhar a prova: registre o distrito sorteado e as cartas de cada equipe, e veja quem venceu cada distrito, o andamento das regiões e qual carta usar.

## Como abrir

Abra o link da página no navegador. Antes de tudo, ela pede a senha de acesso, que vale para os dois modos. Depois, escolha o modo no topo da página:

- **Jogo real**: a partida fica salva no navegador de quem está jogando. Para levar a partida para outro aparelho, use "Gerar cópia" e depois "Restaurar cópia" (esta última exige o modo administrador).
- **Modo teste**: tudo fica neste aparelho e não mexe no jogo real. Escolha quantas rodadas simular e toque em "Gerar partida simulada" para carregar a partida na tela. Na partida simulada, a Dark Side joga pela estratégia selecionada em "Carta sugerida" (Agressivo, Conservador ou Equilibrado), seguindo o mesmo modelo do cálculo, e as adversárias jogam cartas ao acaso. Nenhuma equipe fica ausente.

## Senhas

- **Senha de acesso**: abre a página nos dois modos.
- **Senha de administrador**: liga o modo administrador, que permite reiniciar a partida real, desfazer a última rodada e restaurar cópias. Ela some quando a página é recarregada.

## O que a tela mostra

- **Próxima rodada** e **Como está agora**: horário da rodada e uma explicação simples de quem está na frente, quantos votos cada equipe tem garantidos e quais regiões ainda estão em disputa.
- **Equipes**: votos garantidos e em disputa de cada equipe. A estrela branca marca a líder pelos votos garantidos (sem rodadas, fica na Dark Side). Com as 13 rodadas, a estrela dourada marca a vencedora.
- **Carta sugerida**: a carta da Dark Side com mais chance de vencer a prova, com a lista de todas as cartas. Cartas com "≈" estão em empate técnico com a sugerida.
- **Abertura dos envelopes**: registro da rodada. Nas linhas da Seven e da Rocket aparecem a **tendência** (carta mais provável pelo jeito que a equipe vem jogando) e a **melhor carta para ela** naquela rodada. Se a Dark Side jogar o Coringa, a tela sugere a substituta. Se a substituta não for entregue em 5 minutos, marque "Não entregou".
- **Explicação**: no fim da página, o funcionamento do cálculo, com exemplos. O "?" ao lado de "Carta sugerida" leva até ela.

## Regras

Seguem o regulamento da prova: 13 rodadas, 13 distritos em 6 regiões, 27 votos, Coringa com substituta de 5 minutos (sem substituta, a equipe perde a disputa do distrito), ausência com descarte da menor carta, desempates por região e no total.

## Como a carta é calculada

A recomendação é uma estimativa por simulação:

- Para cada carta da Dark Side, o cálculo simula 3.000 partidas do resto da prova e conta em quantas a Dark Side vence. Todas as cartas são testadas nas mesmas partidas sorteadas.
- As adversárias seguem perfis (Equilibrado, Agressivo ou Conservador) estimados pelas jogadas já registradas. As jogadas consideram o valor de cada distrito: cartas altas aparecem mais em regiões valiosas, e numa região já decidida a equipe joga a menor carta.
- Nas rodadas 1 e 2, o cálculo não usa o Coringa: ele não entra nas cartas testadas para a Dark Side nem na previsão das adversárias, e nenhuma equipe o usa nas simulações dessas rodadas.
- A estratégia da Dark Side (Equilibrado, Agressivo ou Conservador) é escolhida na tela. O resultado de cada estratégia fica guardado enquanto a situação não muda.
- A melhor carta de cada adversária é calculada do mesmo jeito, do ponto de vista dela, com 1.000 partidas por carta, depois da sugestão da Dark Side.
- No celular, o cálculo completo no início da partida, no Equilibrado, pode passar de 20 segundos.

## Observações

- As senhas não ficam no código: a página guarda só o hash (PBKDF2-SHA256, 200 mil iterações). Use senhas longas.
- O código é minificado para dificultar a leitura no navegador. Isso não é segurança: quem abre a página consegue ver a lógica.
- Cada navegador tem a sua partida real. Duas pessoas em aparelhos diferentes não veem a mesma partida sem uma cópia.
- Não há dependências: é um único arquivo HTML.
