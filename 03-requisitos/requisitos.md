# Requisitos Funcionais
## Manipular e exportar documentos PDF
**Descrição:** A aplicação deve permitir anotações feitas por cima de arquivos PDF, selecionar, copiar, interagir com links e destacar textos do arquivo, deve também ser possível exportar o documento modificado em PDF.
 
**Evidência:** A aplicação faz uso de uma biblioteca chamada “Poppler” para renderização de documentos em PDF, a qual está integrada aos módulos de manipulação e exportação de PDF no código fonte em src/core/pdf/. Nesses módulos se encontram também os códigos responsáveis por conectar as funções da biblioteca às funções de manipulação e exportação dos documentos que são realizados pela aplicação.

## Salvar e Carregar documentos
**Descrição:** A aplicação deve permitir que o documento no estado a qual se encontra, com camadas, anotações e demais edições, possa ser salvo no computador do usuário; Também deve ser possível carregar esses documentos salvos para continuar as edições a partir do ponto em que o arquivo foi salvo.

**Evidência:**

# Requisitos Não Funcionais
