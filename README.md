# Estudo da Ferramenta OWASP ZAP

Estudo sobre o funcionamento da ferramenta [OWASP ZAP](https://owasp.org/www-project-zap/).

## O que é

O Zed Attack Proxy (ZAP) é uma ferramenta gratuita de teste de penetração de código aberto que é mantida sob a égide do OWASP (Open Web Application Security Project). O ZAP foi projetado especificamente para testar aplicativos da Web e é flexível e extensível.

No fundo, o ZAP é o que é conhecido como um "proxy intermediário". Ele fica entre o navegador do testador e o aplicativo da Web, para que ele possa interceptar e inspecionar as mensagens enviadas entre o navegador e o aplicativo da Web, modificar o conteúdo se necessário e, em seguida, encaminhe esses pacotes para o destino. Ele pode ser usado como um aplicativo independente e como um processo daemon.

## Como instalar / configurar

Fazer o download do instalador [ZAP](https://www.zaproxy.org/download/). O ZAP necessita do Java 8+ para sua execução. O instalador para Mac Os já inclui a versão do Java necessária. Para Linux, Windows e demais plataformas é necessário realizar a instalação separadamente.  

## Como funciona

O ZAP rastreia o aplicativo da Web com seu Spider e passivamente examina cada página que encontrar. Em seguida, o ZAP usa o scanner ativo para atacar todas as páginas, funcionalidades e parâmetros descobertos.

O ZAP varrerá passivamente todas as solicitações e respostas enviadas por proxy. A varredura passiva é boa para encontrar algumas vulnerabilidades e como uma maneira de entender o estado básico de segurança de um aplicativo Web e localizar onde mais investigações podem ser necessárias.

A verificação ativa, no entanto, tenta encontrar outras vulnerabilidades usando ataques conhecidos contra os destinos selecionados.

Alguns ataques utilizados são:

- Path Traversal
- Remote File Inclusion
- URL Redirector Abuse
- Server side include
- Cross Site Scripting
- SQL Injection
- Directory browsing
- Session ID in URL rewrite
- Secure page browser cache
- External redirect
- CRLF injection
- Parameter tampering
- Fuzzer
- Brute force

## Quão complexo é o seu uso

O uso da ferramenta é simples, porém a análise dos resultados encontrados, bem como as atitudes que devem ser tomadas para corrigir possíveis problemas, requerem um conhecimento avançado sobre segurança da informação e programação defensiva.

## Quais parâmetros são levados em consideração para mensurar a vulnerabilidade do sistema

Os testes de segurança geralmente são divididos de maneira arbitrária, de acordo com o tipo de vulnerabilidade sendo testada ou o tipo de teste sendo realizado. Os tipos de testes que podem ser realizados são:

**Avaliação de vulnerabilidade** - O sistema é verificado e analisado quanto a problemas de segurança.

**Teste de penetração** - O sistema passa por análise e ataque de invasores mal-intencionados simulados.

**Teste de tempo de execução** - O sistema passa por análise e teste de segurança de um usuário final.

**Revisão de código** - O código do sistema passa por uma revisão e análise detalhadas procurando especificamente por vulnerabilidades de segurança.

A medida que o ZAP monitora seu aplicativo da Web, ele cria um mapa das páginas dos aplicativos da Web e os recursos usados ​​para renderizar essas páginas. Em seguida, ele registra as solicitações e respostas enviadas a cada página e cria alertas se houver algo potencialmente errado com uma solicitação ou resposta.

O ZAP realiza a contagem dos alertas encontrados durante o teste, divididos em categorias de risco. Essas categorias de risco são:

![Alertas](images/alert-icons.png)

A partir dos alertas gerados é possível mensurar a quantidade de falhas que um sistema possui.


## Glossário

**Spider:** A Spider ZAP descobre links examinando o HTML nas respostas do aplicativo da web. Fonte: Site oficial Zap Proxy
**Programação defensiva:** É um conjunto de técnicas de projeto (do inglês design) e programação objetivando a estabilidade e a segurança de um software independentemente de seu imprevisível. A ideia pode ser vista como forma de reduzir ou eliminar a hipótese de as Leis de Murphy terem efeito. Técnicas de programação defensiva começaram a ser desenvolvidas quando sistemas de software começaram a possibilitar efeitos catastróficos, seja deliberadamente ou inadvertidamente. Fonte: Wikipédia
