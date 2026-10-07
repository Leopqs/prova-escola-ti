Código, identificadores e documentação em português.
API REST: recursos no plural (/bilhetes), JSON em camelCase.
Framework: Python + FastAPI; persistência em memória (dict/indexed structures) — banco não é exigido.
Testes com pytest; cada regra de negócio deve ter ao menos um teste de borda.
Sem dependências além de fastapi, uvicorn e pytest.
valores monetários sempre em centavos inteiros.

Um sistema de bilhetes de estacionamento possui os seguintes objetos:

Um bilhete possui os campos:
"id": identificador único incremental,
"placa": 7 caracteres alfanuméricos, maiúsculos (ex.: ABC1D23),
"entrada": <ISO-8601 com fuso -03:00>,
"saída": <ISO-8601 com fuso -03:00>,
"minutos": diferença entre horário  saída em minutos
"valorEmCentavos": 450 centavos centavos multiplicado por minutos passados com tolerância de 10 minutos
"status": "aberto"