# Osvaldo Motors

Sistema de software para organizar os clientes, veículos e serviços da oficina Osvaldo Motors,
evitando erros, perda de informações e problemas na cobrança.



#MER (Modelo Entidade-Relacionamento)
1. Cliente
id_cliente — SERIAL PRIMARY KEY
nome — VARCHAR(100)
telefone — VARCHAR(11)
2. Veículo
id_veiculo — SERIAL PRIMARY KEY
placa — VARCHAR(10)
modelo — VARCHAR(100)
tipo — ENUM(tipo_carro)
id_cliente — INTEGER FOREIGN KEY
3. Serviço
id_servico — SERIAL PRIMARY KEY
descricao — TEXT
valor_mao_obra — NUMERIC(10,2)
valor_pecas — NUMERIC(10,2)
valor_materiais — NUMERIC(10,2)
outros_custos — NUMERIC(10,2)
data_servico — DATE
id_cliente — INTEGER FOREIGN KEY
id_veiculo — INTEGER FOREIGN KEY
Relacionamentos
Cliente — Veículo (1:N): um cliente pode possuir vários veículos, mas cada veículo pertence a um cliente.
Veículo — Serviço (1:N): um veículo pode ter vários serviços registrados ao longo do tempo, mas cada serviço está associado a um veículo.
Cliente — Serviço (1:N): um cliente pode ter vários serviços registrados, e cada serviço está associado a um cliente.


<img width="1272" height="492" alt="image" src="https://github.com/user-attachments/assets/ae865b24-6f62-4e81-8f26-c4e7a778d6d8" />

