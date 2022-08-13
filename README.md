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

## 4- cat: mostra os arquivos que esta dentro do diretorio<br> 

## 5- rm: é usado para Apagar
1.1 rm -rf: apaga tudo, diretorio e arquivos
