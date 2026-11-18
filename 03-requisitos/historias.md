# Histórias de Usuário
 
**[H1] Como estudante, quero fazer anotações por cima de um arquivo PDF para facilitar o processo de aprendizado.**
 
*Cenário 1:* Dado que o usuário seleciona alguma ferramenta de escrita, quando o mesmo fizer uma anotação ou desenho, então o programa deve mostrar na tela o desenho de acordo com o que foi tracejado.
 
*Cenário 2:* Dado que o usuário seleciona a ferramenta de borracha, quando o mesmo usá-la para remover alguma anotação, então o programa deve remover do arquivo a parte apagada.
 
**[H2] Como professor, quero exportar o PDF anotado sem perder os links do documento original para enviar aos alunos um material de fácil navegação.**
 
*Cenário 1:* Dado que o usuário abre um PDF com links e faz anotações sobre ele, quando o mesmo exportar o documento como PDF pela interface, então o programa deve gerar um novo arquivo com as anotações e com os links do original funcionando.
 
*Cenário 2:* Dado que o usuário possui um arquivo .xopp, quando o mesmo utilizar a exportação pela linha de comando, então o programa deve gerar o PDF sem precisar abrir a interface.
 
**[H3] Como usuário, quero que o programa salve o documento automaticamente para não perder minhas anotações caso o computador desligue.**
 
*Cenário 1:* Dado que o salvamento automático está ativado, quando passar o tempo configurado pelo usuário, então o programa deve criar um arquivo de autosave com o estado atual do documento.
 
*Cenário 2:* Dado que o programa foi fechado antes de o usuário salvar, quando o mesmo abrir o programa novamente, então o programa deve permitir recuperar o último estado salvo automaticamente.
 
**[H4] Como estudante, quero salvar minhas anotações e abrir o arquivo depois para continuar estudando de onde parei.**
 
*Cenário 1:* Dado que o usuário fez anotações em um PDF com várias páginas e camadas, quando o mesmo salvar o documento no formato .xopp e fechar o programa, então o arquivo deve ser criado no computador do usuário.
 
*Cenário 2:* Dado que existe um arquivo .xopp salvo anteriormente, quando o usuário abrir esse arquivo, então o programa deve mostrar as páginas, as camadas e as anotações do jeito que foram deixadas.
