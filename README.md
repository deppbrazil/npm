# npm #
Inspirado no [vídeo](https://www.youtube.com/watch?v=WZoVzdi3N9s) do [Rafael Dias](https://github.com/eudiasrafael)
### [Download Node.js](https://nodejs.org/en/) ###

## Iniciando ##

`npm init`
* name: 
* version:
* description
* entry point: 
* test command:
* git repository:
* keywords:
* author:
* licence:

Isso vai gerar o [package.json](https://github.com/deppbrazil/npm/blob/master/package.json)

## Buscando pacotes/plugin pela linha de comando ##
* `npm search nomeDoPacote` lista todos os pacotes e plugins com base na busca
* [Documentação](https://docs.npmjs.com/cli/search)
* `npm view nomeDoPacote` lista detalhes do pacote
* [Documentação](https://docs.npmjs.com/cli/view)

## Salvar informações em um ## `.json`,`txt`, `etc`
* `--json`
* `npm view --json nomeDoPacote > detalhes.json` coloca os detalhes do pacote em um `.json`
* `npm -g ls --json > ls.json` coloca quais pacotes estão instalados globais em um `.json`
* `npm ls --json > ls-project.json` coloca quais pacotes estão instalados no projeto em um `.json`

* `txt`
* `npm ls > ls.txt` coloca os detalhes do pacote em um `.txt`

## Buscando pacotes/plugin pela Web ##
* [Site oficial do npm](https://www.npmjs.com/)

## Instalação de um pacote ## 
* `npm install nomeDoPacote` instalação simples
* `npm install nomeDoPacote@123` instalação versão 
* `npm install -g nomeDoPacote` instalação global

## [Salvando dependências](https://github.com/deppbrazil/npm/blob/master/package.json) ##
* `npm install --save nomeDoPacote`
## Salvando dependências de desenvolvimento ##
* `npm install --save-dev nomeDoPacote`

## Instalando dependências ## 
* `npm install` instala todas as dependências
## Instalando dependências de produção ## 
* `npm install --production` instala apenas as dependências de produção

## Atualizando pacotes ##
* `npm update nomeDoPacote` local 
* `npm -g update nomeDoPacote` global

* `npm update --save nomeDoPacote` local e salvando no package.json
* `npm -g update --save nomeDoPacote` global e salvando no `package.json`

## Removendo um pacote ## 
* `npm uninstall nomeDoPacote`
* `npm uninstall --save nomeDoPacote` para salvar no `package.json`
* `npm uninstall --save-dev nomeDoPacote` para salvar no `package.json`
>remove os pacotes e suas dependências, exceto se a dependência também é de outro pacote.

## [Ver pacotes instalados no projeto](https://github.com/deppbrazil/npm/blob/master/package-project.json) ##
* `npm ls`

## [Ver pacotes instalados globais](https://github.com/deppbrazil/npm/blob/master/package-macbook.json) ##
* `npm -g ls`

## Cache ##
* `npm cache ls` lista pacotes cacheados 
* `npm cache clear` limpa cache

## Reconstruindo pacotes devido a atualização do npm ##
* `npm rebuild` recupera os pacotes 
* `npm -g rebuild` recupera os pacotes globais 

## Sufixos de versões ## 
* `*` versão mais recebte - mantém a versão mais recente 
* `123` versão exata - mantém exatamente a versão específicada
* `~123` versão aproximada - mantém sempre a versão menor somente permitindo alterações no ultimo parâmetro de versionamento 12`3`(permite bugFixes)
* `^123` compatível com - sempre aceita mudanças de versões menores, mas nunca permite versões novas de sistema 1`23` (permite newFeatures ou bugFixes)
* `>123` maior que - mantém sempre versões maiores que a específicada, é mesma função do `*`
* `>=123` maior igual que - matém sempre versões maiores ou iguais que a específicada, é mesma função do `*`
* `<123` menor que - mantém sempre versões menores que a específicada, ou seja neste caso pegaria a `1.2.2`
* `<=123` menor igual que - matém sempre versões menores ou iguais que a específicada, é mesma função da `versão exata`

* `^123` mais usada =)

[Documentação de Sufixos](https://semver.org/lang/pt-BR)
