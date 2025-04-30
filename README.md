Projeto: Sistema de Ordem de Serviço para Oficina Automotiva

📄 Descrição
Este sistema foi projetado para gerenciar ordens de serviço de veículos que passam por conserto ou revisão em uma oficina automotiva.
O sistema permite o cadastro de clientes, veículos, equipe técnica e serviços realizados, além do controle do valor de mão de obra e peças.

🗂️ Estrutura do Banco de Dados
Principais Entidades:
Cliente: Contém informações do cliente (nome, endereço).

Veículo: Relaciona veículo ao cliente (marca, ano, cor).

Ordem_de_Serviço: Representa a ordem emitida (número, valor, status, datas).

Equipe_Conserto e Equipe_Revisão: Equipes responsáveis por cada tipo de serviço.

Serviços:
Conserto:

Tabelas: Conserto, Conserto_Ordem_de_Serviço, Tabela_de_Serviços_Conserto

Revisão:

Tabelas: Revisão, Revisão_Ordem_de_Serviço, Tabela_de_Serviços_Revisão

Itens Adicionais:
Peças: Controle de peças usadas, associadas a Conserto ou Revisão.

Status da OS: Campo para controlar o andamento da ordem.

🔗 Relacionamentos
Um cliente pode ter vários veículos.

Um veículo pode gerar várias ordens de serviço.

Uma ordem de serviço pode envolver revisão e/ou conserto.

Cada equipe é especializada em revisão ou conserto.

Há muitos-para-muitos entre ordens de serviço e serviços (via tabelas auxiliares).

Peças podem ser utilizadas em mais de um serviço.

📈 Fluxo Operacional
Cadastro de Cliente e Veículo

Entrada do veículo

Análise e decisão do Cliente

Geração da Ordem de Serviço

Execução pela Equipe Técnica

Atualização de valores (mão de obra e peças)

Finalização e conclusão da OS

📋 Observações
O sistema foi pensado para ser escalável: novas marcas de veículos e peças podem ser facilmente adicionadas.

Evita duplicação de informações através da normalização até 3FN.

Facilita futuras integrações com sistemas de estoque, financeiro ou atendimento ao cliente.

📌 Versão Atual
Modelo de Dados: v1.0

Data: Abril/2025

🎯 Créditos
Desenvolvido por: Joelton Feitoza

🚀 Pronto para ser implementado em:
MySQL

PostgreSQL

MariaDB

OracleDB (com pequenos ajustes)
