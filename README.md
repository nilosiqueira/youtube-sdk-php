# SDK em PHP para o Youtube
SDK em php para download de vídeos do Youtube.



## Observação

Essa SDK foi construída devido a necessidade de integração de um projeto de terceiro com o Youtube. Foi publicada com a ideia de que possa ser útil para outras pessoas. Este repositório (e, consequentemente, seu dono) não possuem qualquer vínculo com o Youtube.


## Como instalar
```
composer require bruceskills/youtube-sdk-php
# Logo após rode o comando abaixo
composer update
```
#
## Como usar
Abra o arquivo index.php que se encontra em vendor/bruceskills/youtube-sdk-php/ e na variável $url coloque a url do vídeo.
```php

<?php
require __DIR__.'/vendor/autoload.php';

use Youtube\Service;

$url = "https://www.youtube.com/watch?v=bo_efYhYU2A";

$youtube = new Service();

$download = $youtube->download($url);

```
#
### Como testar caso tenha clonado o projeto

Dentro do diretório do projeto clonado, digite o comando abaixo em seguida abra seu navegador e cole o endereço: http://localhost:8181/public, você vai perceber que tem uma interface para colar o link do vídeo e em seguida realizar o download. Ou http://localhost:8181, você vai perceber que o download de um vídeo teste do youtube já vai começar à ser feito o download.
```
php -S localhost:8181
```
#
### Como testar caso tenha feito composer require bruceskills/youtube-sdk-php

Dentro do diretório do projeto, digite o comando abaixo em seguida abra seu navegador e cole o endereço: http://localhost:8181/public, você vai perceber que tem uma interface para colar o link do vídeo e em seguida realizar o download. Ou http://localhost:8181, você vai perceber que o download de um vídeo teste do youtube já vai começar à ser feito o download.
```
php -S localhost:8181 -t vendor/bruceskills/youtube-sdk-php/
```
