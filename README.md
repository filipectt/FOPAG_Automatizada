**FOPAG AUTOMATIZADA - CONFERÊNCIA E VALIDAÇÃO DE PAGAMENTOS**

A conferência manual de folha de pagamento (FOPAG) é complexa e exige a validação cruzada entre planilhas da Empresa e do Banco para garantir que todos os beneficiários estejam ativos e cadastrados. 
Este processo manual é propenso a erros e muito demorado, podendo custar quase o dia inteiro a depender do número de colaboradores a conferir.

**O que ele faz:**
- Leitura e Validação: O script automatiza o upload de duas planilhas Excel (Ativos Banco e Ativos Empresa).
- Conferência Cruzada: Compara a lista de beneficiários da Empresa com a lista de ativos do Banco (utilizando o CPF como chave de busca, após padronização).
- Sinalização: Para cada registro da folha, o script adiciona a Matrícula do Banco se o beneficiário for encontrado, ou marca o registro com o status **"Não Cadastrado no Banco"** se a validação falhar.
- Exportação Final: Gera uma nova planilha Excel (Planilha_Pagamento_Final.xlsx) com a lista consolidada e as validações, pronta para ser usada no processo de pagamento.
- Ponto chave: esta planilha final foi pensada pra ser gerada exatamente igual ao do modelo do banco pra fins de importação, sendo necessário somente o CTRL C e CTRL V após o processo do script.

**Bibliotecas:**
- pandas e openpyxl: Essenciais para a leitura, manipulação e escrita de arquivos Excel (XLSX).
- google.colab: Utilizada para o upload e download dos arquivos dentro do ambiente de execução do Google Colab.

**Observações finais:**
- Este código reduziu em aproximadamente 30 minutos o que custava o dia todo e dois funcionários. Meu contexto: aproximadamente 1000 colaboradores pra processar.
- Este código foi pensado pra resolver um problema da minha rotina e de um contexto de conferência de folha de pagamento específico, talvez não funcione pra você.

**Acesso:**
