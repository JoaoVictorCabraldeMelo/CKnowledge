
#internet #http

[Referencia](https://cs.fyi/guide/how-does-internet-work)

- Internet Protocol (IP) -> responsavel por rotear pacotes para seu destino correto
- Transmission Control Protocol (TCP) -> garante que os pacatos vao ser transmitidos de forma segura e na ordem correta
- Domain Name System (DNS)
- Hypertext Transfer Protocol (HTTP)
- Secure Sockets Layer/Transport Layer Security (SSL/TLS)

- Pacote: um pequena unidade de dado sendo transmitido pela internet
- Roteador: Um dispositivo que direciona pacotes para diferentes redes de computadores.
- Endereco de IP: Um identificado para cada dispositivo em uma rede.
- Domain Name: Name legivel por humanos usado para identificar websites.
- DNS: Domain Name System eh responsavel por traduzir Domain Names para Endereco de IP
- HTTP: Hypertext Transfer Protocol usado para transferir dados entre clientes como seu navegador web a servidores como um website.
- HTTPS: Uma versao criptografada do HTTP usada para prover comunicacao segura entre cliente e servidor
- SSL/TLS: O Secure Sockets Layer e Transport Layer Security sao protocolos para prover comunicacao segura na internet.

Tem muitos outros protocolos usado na internet para se comunicar como:
- UDP -> User Datagram Protocol faz o mesmo papel do TCP porem nao garente ordem.

O motivo de utilizar protocolos padroes e porque dispositivos e sistemas de diferentes empresas podem se comunicar sem dificuldades.

HTTPS usa SSL/TLS para criptografar suas mensagens

Chaves para entender uma aplicacao TCP/IP (Transmission Control Protocol/Internet Protocol)

- Portas: Portas sao usadas para indentificar aplicacoes ou servisos rodando em um dispositivo. 
- Sockets: E uma combinacao de endereco de ip com um numero de porta, representando um endpoint especifico de comunicacao. 
- Connections: uma conexao e estabelecida com dois sockets quando dois dispositivos querem comunicar com outro. 
- Transferencia de Dados: Quando uma conexao eh estabelecida os dados sao transferidos por segmentos.

### SSL/TLS 
A diferenca na comunicacao quando usamos o SSL/TLS

- Certificates: SSL/TLS certificados sao usados para estabelecer confianca entre cliente e servidor. 
- Handshake: Onde negociam o algoritmo de criptografia e outros parametros
- Criptografia

