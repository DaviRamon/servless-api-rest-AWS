# function-lambda-AWS

instalar o AWS cli. conforme seu sistema operacional
https://docs.aws.amazon.com/pt_br/cli/latest/userguide/install-cliv2.html


após isso, deve-se criar uma conta free na AWS, para ter acesso ao Amazon Consoles.
Configurar um novo usuário com acesso de administrador e obter Access key ID e Secret Access key e Access
configurar no terminal  as chaves com aws configure e colar as chaves. 



após isso instalar o serverless  
LINUX X84 -->  curl -o- -L https://slss.io/install | bash


as taxas da AWS são cobradas por tempo de execução e memória consumida. As lambdas traz escalabilidade.
tempo máximo de execução 15 min. 

para incluir algum código mais dinâmico que necessite de dependencias, se faz necessário o upload da pasta node_modules no diretorio do lambda. 
Pode ser upado via s3 ou por um arquivo ZIP. 

incluir no zip o index.js com o codigo e o node_modules com as dependencias instaladas via npm.


também pode ser feito pelo AWS CLI por meio do comando.

## NO TERMINAL 
criar um .zip com os arquivos desejados e utilizar o método abaixo

aws lambda update-function-code --function-name nome-da-funcao --zip-file fileb://arquivo-desejado.zip
                      
