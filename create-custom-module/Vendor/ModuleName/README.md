Como criar um novo módulo  no Magento 2

Estrutura de pastas para a criação de modulo de

Vendor
 -NomedoModulo
    -etc
        module.xml
    registration.php

Obs: seu novo modulo deve ser carregado na app/code da estrutura de pasta do seu magento instalado. Pode fazer o upload dos arquivos via FTP ou SSH.


-Substitua o nome da pasta "Vendor" e pelo nome a sua escolha
-Substitua o nome da pasta "ModuleName"  pelo nome do seu módulo

1- passo
arquivo módulo.xml

2- passo
registration.php

Esses dois arquivos acima são de uso obrigatório para criar e começar com o desenvolvimento do modulo.

Após a criação de arquivos module.xml e registro.php, o próximo passo é acessar a linha de comandos do magento e executar os seguintes comandos sequencialmente:

php bin/magento setup:upgrade
php bin/magento setup:static-content:deploy -f
php bin/magento cache:flush
