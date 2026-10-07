O sistema deve permitir as seguintes funcionalidades:
| Número da task | Descrição da task |Método API request | Caminho | Body |
| T1 | Abrir bilhete | POST | /bilhetes | placa(obrigatório), entrada(opcional)|
|T2 |	Encerrar bilhete | POST	/bilhetes/{id}/encerramento — sem body|
|T3 |	Listar bilhetes ativos |	GET	/bilhetes/ativos — sem body|
|T4	| Relatório diário	| GET	/relatorios/diario?data=AAAA-MM-DD — data (obrigatório)|
|T5	| Cancelar bilhete	| POST	/bilhetes/{id}/cancelamento — sem body|
|T6	| Histórico por placa	| GET	/bilhetes?placa=... — placa (obrigatório)|
|T7	| Aplicar tolerância	| 10 iniciais grátis; se ultrapassar a tolerância, cobra integralmente desde o primeiro minuto|
|T8	| Impedir placa duplicada|	POST /bilhetes — placa (obrigatório), entrada (opcional); uma placa só pode possuir um bilhete aberto|