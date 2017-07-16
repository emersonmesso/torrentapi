# torrentapi
API de gerenciamento de informações de arquivos torrent

API padrão torrente é uma API desenvolvida para facilitar a busca de informações de arquivos torrente.

Dodos os dados de um arquivo .torrent podem ser encontrados utilizando o seguinte site http://padrao-torrent.alphi.media/home e a API que está atrelado a ele.

#Uso
Para utilizar você terá que enviar o arquivo .torrent para o site e posteriormente utilizar o link informado no site, como por exemplo o link abaixo:
http://padrao-torrent.alphi.media/torrent.php?type=json&info_hash=bfc7acfb4e1a347f157592f645fc1a4ad04f5506

Este link fornece a você todos os dados do torrent que você escolher na forma de JSON, onde você pode adicionar ao seu site ou sistema.

Exemplo de uso:

@CODIGO PHP

$json_file = file_get_contents("http://padrao-torrent.alphi.media/torrent.php?type=json&info_hash=c6ef1b82e2715f298803d5be641cb7226916b74b");   
$json_str = json_decode($json_file, true);

@CODIGO PHP
onde será retornada todos os dados da API

#Dados de retorno: 
Nome - ( $json_str[0]['nome'])

