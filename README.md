# Terminal-Linux #
## Caderno de anotação dos comandos no terminal do Linux🐧


## 1- Ls: o Comando apenas e teus atributos
1.1 ls eLista de pastas dentro de um diretorio
1.2 ls -a: Mostra diretorios ocultas <br>
1.3 ls -R: Mostra todos os arquivos e diretorios <br>
1.4 ls -l: Mostra o formato de lista longa <br>
1.5 ls /etc/*.conf: A estrela no diretorio está fazendo uma busca ou referencia a uma  determinada quantidade de caracteres "No caso o .conf, e poderia ser qualquer outro que você deseja buscar" <br >
1.6 ls /etc/?a*: O ponto de interrogação faz uma busca pelo o diretorio "/etc" e busca apenas um caracter "a" e como a estrela esta apos do a pode vim qualquer arquivo ou pasta que contenha a. <br>
1.7 O uso dos COuchetes []
Os couchetes tem função de realiza um intervalo de caracteris por exemplo "ls /etc/p[a-i]"
o comando acima vai buscar algum arquivo ou diretorio que começa com a letra p e tem a variação de a até i.
1.8 couchetes [] com virgula "," 
as vigulas tem a função de delimitar apénas para um carcter apenas com no exemplo a seguir "ls /etc/p[a-i,e]"

1.9 as chaves com os couchetes as chaves apenas buascam um padrão é um ou outro "caso coloque dois, não entre igual o couchetes" como no exemplo a seguir ls /etc/*.{tab,as }

## 2- Criacão de um arquivo de texto  
1- touch: + nome do aquivo + tipo <br> 
Exemplo (touch oi.txt)<br> 
2- Nano: você pode colocar nano + nome do arquivo + tipo;<br> 
Exemplo (nano oi.txt)<br> 

## 3- PWD: mostra o caminho que você está no terminal<br> 

## 4- cat: pega as informaçoes de um determinado arquivos e exibi na tela<br>
exemplo cat etc/services


## 5- rm: é usado para Apagar
1.1 rm -rf: apaga tudo, diretorio e arquivos

## 6- tac: ele é igual a cat mais so que exibe ao contrario de traz para frente

## 7-cp: é para copiar arquivos e mover arquivos
exemplo cp Aulalinux.txt Faculdade
aula linux é o arquivo que eu estou copiando. Faculadade é o diretorio que eu estou movendo a copia.

## 8- mv: Caso precise mover use mv + nome do arquivo + novo diretorio
mv AulaLinux.txt Faculdade 

## 9- Usuarios:
1.1- useradd convidado -m -c "Benedito"
no codigo acima você esta passando o nome de usario, depois, o padrão -m para ser criado as pastas padrões, logo após vem o -c criar uma nova pasta para o novo usuario.

1.2-  userdel -f convidado
O codigo apresentado é usado para apagar o usario.

1.3- useradd convidado -m -c "Benedito" -e 18/08/2022
Temos um novo parametro o -e + data do termino, é usado para dar uma data de uso para o novo usario, ele pode usar até aquela determinada data depois a sua conta é expirada.

1.4- usermod convidado 
Com esse novo comando você pode realizar alterações, apenas passe o paramentro quw você deseja alterar.

1.5- usermod convidado -s /bin/bash
O parametro -s /bin/bash é utilizado para add o shell a pasta, o shell é que faz as configurações finais

1.6- passwd convidado -e 
O comando acima esta requerendo que o novo usario ao entra na conta, crie uma nova senha.
Caso deseje da uma data para a troca de senha, apenas coloque a data limite na frente do paramentro => passwd convidado -e 18/08/2022.

