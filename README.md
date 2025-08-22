# Z_ATUALIZA_PROGRAMAS_Z

**Autor:** Luiz Guni  
**Data de Criação:** 22/08/2025  
**Descrição:** Atualiza a tabela `Z0FI_PROGRAMAS` com os programas Z originais encontrados na TRDIR (sem includes, function-pools e enhancements).

---

## Objetivo

O report `Z_ATUALIZA_PROGRAMAS_Z` tem como finalidade automatizar a atualização da tabela customizada `Z0FI_PROGRAMAS` com todos os programas Z originais existentes no sistema SAP, garantindo:

- Inclusão apenas de programas Z executáveis (Reports).
- Exclusão de includes, function-pools e enhancements.
- Relatório de status detalhado com total de programas, já existentes e novos inseridos.

---

## Estrutura do Código

O código ABAP segue uma lógica clara e objetiva:

1. **Definição de Tipos e Variáveis**
   - `ty_name`: Estrutura para armazenar o nome do programa.
   - `lt_all`: Lista de todos os programas Z encontrados.
   - `lt_exist`: Lista de programas já existentes na tabela `Z0FI_PROGRAMAS`.
   - Contadores para total, existentes e novos inseridos.

2. **Seleção dos Programas**
   - Consulta a tabela `TRDIR` para buscar programas Z originais.
   - Remove duplicatas e organiza em ordem alfabética.

3. **Verificação e Inserção**
   - Loop em `lt_all` para comparar com `lt_exist`.
   - Inserção de novos programas na tabela `Z0FI_PROGRAMAS`.
   - Saída colorida detalhando inseridos e já existentes.

4. **Resumo Final**
   - Exibe contagem total de programas encontrados, existentes e inseridos.

---

## Requisitos

- SAP ECC ou S/4HANA com acesso à tabela TRDIR.
- Permissão para inserir registros na tabela `Z0FI_PROGRAMAS`.
- Ambiente de desenvolvimento ABAP.

---

## Como Executar

1. Acesse a transação **SE38** ou **SA38**.
2. Informe o nome do report: `Z_ATUALIZA_PROGRAMAS_Z`.
3. Execute o report.
4. Acompanhe a saída detalhada no log do programa.
5. Os novos registros serão inseridos automaticamente na tabela `Z0FI_PROGRAMAS`.

---

## Boas Práticas Implementadas

- Uso de **BINARY SEARCH** para otimização na leitura da tabela existente.
- Saída formatada com cores para melhor visualização de status.
- Commit explícito após inserções.
- Código modular e comentado, fácil de manter e entender.
- Evita inserção de duplicatas.

---

## Exemplo de Saída
Relatório de Atualização - Programas Z Originais (TRDIR)

<img width="3032" height="1526" alt="Captura de tela 2025-08-22 082817" src="https://github.com/user-attachments/assets/96c8c51f-f1e2-4eff-8df7-8e2e250f79f6" />

<img width="3041" height="1512" alt="Captura de tela 2025-08-22 082750" src="https://github.com/user-attachments/assets/bf12d1ca-a46f-41d8-b873-c8204ffb4d23" />

Resumo da execução:

Total de programas Z encontrados na TRDIR: 407

Já existentes na Z0FI_PROGRAMAS : 14.224

Novos inseridos : 0


✨ Autor:
Desenvolvido por Guni
💼 Analista e Desenvolvedor ABAP | Java
📅 Criado em: 22/08/2025
