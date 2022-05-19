# BackstopJS

O BackstopJS (criado e mantido por [Garris Shipon](https://github.com/garris/BackstopJS#backstopjs)) automatiza os testes de regressão visual de uma interface web responsiva, por meio da comparação das capturas de tela.


Para utilizar o backstopJS basta clonar o repositório ou instalar via npm

`npm install -g backstopjs`

Acessar o arquivo `backstop.json` e realizar as configurações conforme desejado.

> Em _scenarios_ estarão os cenários de testes, sendo propriedades obrigatórias a _label_, que é um nome para a tela, e a _url_ que será o endereço objeto do teste.
> As demais propriedades são opcionais.

```
OBS.: É possível alterar a estrutura para utilizar um arquivo de configuração .js, possibilitando separar em arquivos distintos as viewports e scenarios, por exemplo.
[Example jsBasedConfig](https://github.com/garris/BackstopJS/tree/master/examples/jsBasedConfig) | [Viewports in separate files](https://github.com/garris/BackstopJS/issues/905)
```

### Comandos básicos

> `backstop init` - Inicializará a estrutura, criando os diretórios e arquivos de configuração (Necessário quando instalar via npm)
>
> `backstop test` - Executa os testes
>
> `backstop approve` - Aprova as imagens alteradas para que sejam consiradas como imagens de referência
>
> `backstop reference` - Cria uma nova referência, descartando todas as imagens anteriormente capturadas

### Primeira execução

Todos os testes irão falhar ao utilizar o comando test pela primeira vez. O report será disponibilizado permitindo visualizar as imagens e validar se estão conforme esperado.

Após essa primeira validação e confirmação visual, será possível aprovar as imagens para que sejam consideradas como referência para as próximas execuções. Portanto, é necessário aprovar as imagens utilizando o comando `approve`.


### Docker
Também é possível executar os testes em um container Docker. 

`backstop test --docker`

---
## Mas o que é teste de regressão visual?

Testes de regressão visual (Visual Regression Tests/VRT) são testes de alto nível que conseguem expor qualquer alteração visual de um sistema, seja em uma página específica ou em um determinado fluxo que o usuário irá percorrer. Em vez de apenas assegurar que algum elemento ou valor de texto está presente, o teste realmente abre a página e verifica se esse bloco específico aparece exatamente como é esperado que ele apareça. Para que isso seja feito, esse tipo de teste faz uma captura da página que está sendo testada e compara este screenshot com sua versão estável (baseline).

![](http://shipit.resultadosdigitais.com.br/images/posts/vrt_diagram.jpg)

## Teste de snapshot - Qual é a diferença entre teste de snapshot e teste de regressão visual?
Teste de snapshot e teste de regressão visual são duas maneiras distintas de testar interfaces de usuário, ou UIs, e eles servem para finalidades diferentes. Ferramentas de teste de regressão visual tiram screenshots de páginas web e comparam as imagens resultantes pixel por pixel. Com testes de snapshot os valores são serializados, armazenados dentro de arquivos de texto e comparados usando um algoritmo de comparação.

## Algumas ferramentas
 - **Regressão Visual**
   - [BackstopJS](https://garris.github.io/BackstopJS/) (Gratuito) - Open-source para testes de aplicações web.
   - [Percy](https://percy.io/) (Uso gratuito limitado a 5.000 snapshots por mês)
 
 - **Snapshot**
   - [Jest](https://jestjs.io/pt-BR/docs/snapshot-testing) (Gratuito)
   - [@cypress/snapshot](https://github.com/cypress-io/snapshot)
   

---
 
## Referências
- [Documentação BackstopJS](https://github.com/garris/BackstopJS#readme)
- [Ship it - Testes de regressão visual - Obtendo olhos a prova de erros](http://shipit.resultadosdigitais.com.br/blog/testes-de-regressao-visual-obtendo-olhos-a-prova-de-erros/)
- [Jest - Diferença entre teste de snapshot e teste de regressão visual](https://jestjs.io/pt-BR/docs/snapshot-testing#qual-%C3%A9-a-diferen%C3%A7a-entre-teste-de-snapshot-e-teste-de-regress%C3%A3o-visual)
- [Medium Agnaldo Vilariano - Configurando o BackstopJS](https://medium.com/@vilariano/visual-regression-testing-c84eaf4e5254)
- [Iterasys - Testes de Regressão Visuais com Cypress e Percy](https://www.youtube.com/watch?v=d6-rhhoHhXs&t=5610s)
