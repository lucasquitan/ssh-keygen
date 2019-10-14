# Criando chave SSH 

Primeiro, devemos saber se já possuímos alguma chave SSH na máquina em questão. Para isso devemos digitar o comando

``ls ~/.ssh``

Caso apareça dizendo que não há arquivos ou diretórios, então você não tem nenhuma chave e pode prosseguir.

Em seqguida, para criar uma nova chave, digite ***ssh-keygen***

Caso queira adicionar um comentário a chave criada, digite o parâmetro *-C* e em sequencia a mensagem. É recomendado que coloque seu e-mail, por exemplo: 

``ssh-keygen -C "meu-email@mail.com"``

Após isso, é necessário criar uma chave para a sua key.

Depois da chave concluída, e necessário do conteúdo dela para podermos adicionarmos ao Github. Para isso, digite no *Terminal*:

``cat ~/.ssh/id_rsa.pub``

O comando *cat* irá exibir o conteúdo do arquivo *id_rsa.pub* no Terminal. Copie o conteúdo do arquivo.
Em seguida, vá as configurações do Github e acesse ***SSH and GPG key***. Adicione um nome para sua chave, e cole o conteúdo do arquivo abaixo.

Para testar, digite no terminal:

``ssh -T github@github.com``

O comando acima fará com que inicie uma conexão com o Git e irá informar sobre a autentificação do cliente, digite *yes* para continuar.

Após isso, aparecerá um warning dizendo que que o GitHub não fornece acesso pelo bash, porém a chave estará criada com sucesso.