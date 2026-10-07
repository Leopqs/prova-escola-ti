Os testes devem seguir os seguintes critérios:
| Número do teste | Cenário | Tipo |
| Tt1 | sucesso ao abrir bilhete retorna 201 + informações do bilhete | feliz |
| Tt2 | erro 422 ao tentar abrir um bilhete que não existe ou fora do horário | borda |
|Tt1	sucesso ao encerrar bilhete retorna 200 + informações do bilhete, incluindo saída, minutos e valor em centavos	| feliz
| Tt2 |	sucesso ao listar bilhetes ativos retorna 200 + array dos bilhetes abertos, mais recentes primeiro	| feliz
| Tt3 |	sucesso ao consultar relatório diário com data válida retorna 200 + total de bilhetes, faturamento e tempo médio	| feliz
| Tt4 |	erro 422 ao consultar relatório diário com data fora do formato AAAA-MM-DD	| borda
| Tt5 |	sucesso ao cancelar bilhete aberto retorna 200 + status cancelado, sem saída e sem valor_centavos	| feliz
| Tt6 |	sucesso ao consultar histórico por placa válida retorna 200 + bilhetes da placa, mais recentes primeiro	| feliz
| Tt7 |	erro 422 ao consultar histórico sem placa ou com placa em formato inválido	| borda
| Tt8 |	erro 404 ao tentar encerrar bilhete inexistente	| borda
| Tt9 |	erro 409 ao tentar encerrar bilhete que já foi encerrado |	borda
| Tt10 |	erro 404 ao tentar cancelar bilhete inexistente	| borda
| Tt11	| erro 409 ao tentar cancelar bilhete já encerrado ou cancelado	| borda
| Tt12 |	valor do bilhete é 0 centavos quando a duração é menor ou igual à tolerância configurada	| feliz
| Tt13 |	valor do bilhete é cobrado integralmente desde o primeiro minuto quando a duração ultrapassa a tolerância	| borda
| Tt14 |	erro 409 ao tentar abrir novo bilhete para uma placa que já possui bilhete aberto | borda