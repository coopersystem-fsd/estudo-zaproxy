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

## Quão complexo é o seu uso

## Quais parâmetros são levados em consideração para mensurar a vulnerabilidade do sistema

## Glossário

**Spider:** A Spider ZAP descobre links examinando o HTML nas respostas do aplicativo da web.
