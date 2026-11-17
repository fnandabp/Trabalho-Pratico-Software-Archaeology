# Requisitos Funcionais
## [RF1] Manipular e exportar documentos PDF

**Descrição:** A aplicação deve permitir anotações feitas por cima de arquivos PDF, selecionar, copiar, interagir com links e destacar textos do arquivo, deve também ser possível exportar o documento modificado em PDF.
**Evidência:** A aplicação usa uma biblioteca chamada “Poppler” para renderizar PDFs. Isso está no código em `src/core/pdf/popplerapi/PopplerGlibDocument.cpp`. O carregamento do PDF de fundo de um documento é feito em `src/core/control/xojfile/LoadHandler.cpp`.

## [RF2] : Salvar e carregar documentos

**Descrição:** A aplicação deve permitir que o documento, no estado em que se encontra, com camadas, anotações e demais edições, seja salvo no computador do usuário. Também deve ser possível carregar esses documentos salvos para continuar as edições a partir do ponto em que o arquivo foi salvo.
**Evidência:** O programa usa uma extensão própria de arquivo, o `.xopp`. è possível encontrar os arquivos responsáveis por salvar e carregar, respectivamente, em `src/core/control/xojfile/LoadHandler.cpp` e `src/core/control/xojfile/SaveHandler.cpp`. Testes: `test/unit_tests/control/LoadHandlerTest.cpp` (testPagesZipped, testStrokeWidthRecovery e testRelativePath).

## [RF3] : Fornecer ferramentas de desenho e anotação

**Descrição:** A aplicação deve permitir que sejam usadas diferentes ferramentas de desenho livre, como caneta, marca-texto e borracha. Também deve permitir alterar os estilos de traço, como espessura, cor e se o traço é sólido ou pontilhado.
**Evidência:** As ferramentas são configuradas em `src/core/control/ToolHandler.cpp`. O traço é desenhado em `src/core/control/tools/StrokeHandler.cpp` e o apagamento em `EraseHandler.cpp` (mesma pasta). Testes: `ToolEnumsTest.cpp` e `StrokeStyleTest.cpp`, em `test/unit_tests/`.

## [RF4] : Exportação dos documentos

**Descrição:** A aplicação deve exportar o documento criado para diversos formatos, como SVG, PNG e PDF, tanto pela interface quanto pela linha de comando.
**Evidência:** A exportação em PDF está em `src/core/control/jobs/PdfExportJob.cpp` e a de imagens em `src/core/control/jobs/ImageExport.cpp`. As opções que aparecem na interface ficam em `src/core/gui/dialog/ExportDialog.cpp`. O README também diz que dá para exportar pela linha de comando. 


# Requisitos não-funcionais:
## [RNF1] : Portabilidade

**Descrição:** O sistema deve ser compilado e executado em diferentes sistemas operacionais sem restrições de funcionalidades.
**Evidência:** O repositório tem pastas de instalação separadas para cada sistema: windows-setup/, linux-setup/ e mac-setup/.

## [RNF2] : Confiabilidade e recuperação de falhas

**Descrição:** Por ser uma aplicação voltada a anotações, em caso de queda de energia ou falha do programa, é essencial que o software implemente mecanismos para preservar, salvar automaticamente ou recuperar as informações do documento.
**Evidência:** O autosave está em AutosaveJob `src/core/control/jobs/AutosaveJob.cpp`. Ele salva o documento em um arquivo temporário .autosave.xopp e só troca o arquivo anterior depois de terminar.

## [RNF3] : Traços com baixa latência

**Descrição:** Enquanto o usuário escreve ou desenha no documento, a resposta entre a ação de desenhar e o desenho aparecer na tela tem que ser rápida.
**Evidência:** A entrada do traço é tratada em `src/core/control/tools/StrokeHandler.cpp` e a exibição fica nas classes de `src/core/view/overlays/`. 

## [RNF4] : Compatibilidade com diferentes dispositivos de entrada

**Descrição:** A aplicação deve ser compatível com diferentes dispositivos de entrada, como mesas digitalizadoras, touch-screen e mouse, levando em conta as diferenças de cada um.
**Evidência:** A pasta `src/core/gui/inputdevices/` tem um arquivo para cada tipo de entrada: MouseInputHandler.cpp, TouchDrawingInputHandler.cpp, PenInputHandler.cpp e StylusInputHandler.cpp.
