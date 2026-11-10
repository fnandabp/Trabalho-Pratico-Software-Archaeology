# Requisitos Funcionais
## Manipular e exportar documentos PDF
**Descrição:** A aplicação deve permitir anotações feitas por cima de arquivos PDF, selecionar, copiar, interagir com links e destacar textos do arquivo, deve também ser possível exportar o documento modificado em PDF.
 
**Evidência:** A aplicação faz uso de uma biblioteca chamada “Poppler” para renderização de documentos em PDF, a qual está integrada aos módulos de manipulação e exportação de PDF no código fonte em src/core/pdf/. Nesses módulos se encontram também os códigos responsáveis por conectar as funções da biblioteca às funções de manipulação e exportação dos documentos que são realizados pela aplicação.

## Salvar e Carregar documentos
**Descrição:** A aplicação deve permitir que o documento no estado a qual se encontra, com camadas, anotações e demais edições, possa ser salvo no computador do usuário; Também deve ser possível carregar esses documentos salvos para continuar as edições a partir do ponto em que o arquivo foi salvo.

**Evidência:** O programa utiliza de uma extensão própria de arquivo .xopp, esse formato é um arquivo de texto compactado estruturado em XML(Extensible Markup Language), e guarda as “Informações” do documento como o nome, a posição de cada traço desenhado, as cores que foram usadas nesses traços, quantas camadas e páginas, dentre outros dados que o arquivo possa conter. As funções responsáveis por converter, salvar e carregar esses documentos estão localizadas no código fonte em src/core/model/ e src/core/control/.

## Fornecer ferramentas de desenho e anotação

**Descrição:** A aplicação deve permitir que sejam usadas diferentes ferramentas de desenho livre como pincéis, canetas, marca-texto; Assim como também deve permitir alterar os estilos de traço, sua espessura, transparência, cor, se o traço é pontilhado ou sólido.

**Evidência:** A evidência da implementação e gerenciamento dessas ferramentas está estruturada no código fonte, nos módulos de controle de entrada em src/core/control, e as classes de ferramentas em src/core/tools/. 

## Exportação dos documentos

**Descrição:** a aplicação deve exportar o documento criado para diversos formatos de documento, como SVG, PNG e PDF, tanto pela interface quanto pela linha de comando.

**Evidência:**

# Requisitos Não Funcionais
## Portabilidade - Multiplataforma
**Descrição:** O sistema deve ser compilado e executado em diferentes sistemas sem restrições de funcionalidades.

**Evidência:**

## Confiabilidade - Recuperação de Falhas

**Descrição:** 

**Evidência:**

## Performance - Traços com baixa latência 

**Descrição:**

**Evidência:**

## Compatibilidade com diferentes dispositivos de entrada

**Descrição:** A aplicação deve ser compatível com diferentes dispositivos de entrada como mesas digitalizadoras, touch-screen e mouse. Levando em conta as diferenças d

**Evidência:**
