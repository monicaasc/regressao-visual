# BackstopJS

Abrir o arquivo `backstop.json` e realizar configuração conforme desejado.

> Em _scenarios_ estarão os cenários de testes, sendo propriedades obrigatórias a _label_, que é um nome para a tela, e a _url_ que será o endereço objeto do teste.
> As demais propriedades são opcionais.

Utilizar o comando test para executar. Na primeira execução todos os testes irão falhar. O report será aberto, permitindo visualizar as imagens e validar se estão conforme esperado.

`backstop test` 

Após confirmar, é necessário aprovar as imagens que servirão de baseline para a execução dos testes. 

`backstop approve`

## Docker
É possível utilizar o Docker para rodar os testes do BackstopJS.

`backstop test --docker`

### Documentação
- [BackstopJS](https://www.npmjs.com/package/backstopjs)

---

## O que é teste de regressão visual?

Testes de regressão visual (Visual Regression Tests/VRT) são testes de alto nível que conseguem expor qualquer alteração visual de um sistema, seja em uma página específica ou em um determinado fluxo que o usuário irá percorrer. Em vez de apenas assegurar que algum elemento ou valor de texto está presente, o teste realmente abre a página e verifica se esse bloco específico aparece exatamente como você quer que ele apareça. Para que isso seja feito, esse tipo de teste faz uma captura da página que está sendo testada e compara este screenshot com sua versão estável (baseline).

![](http://shipit.resultadosdigitais.com.br/images/posts/vrt_diagram.jpg)

## Teste de snapshot - Qual é a diferença entre teste de snapshot e teste de regressão visual?
Teste de snapshot e teste de regressão visual são duas maneiras distintas de testar interfaces de usuário, ou UIs, e eles servem para finalidades diferentes. Ferramentas de teste de regressão visual tiram screenshots de páginas da web e comparam as imagens resultantes pixel por pixel. Com testes de snapshot os valores são serializados, armazenados dentro de arquivos de texto e comparados usando um algoritmo de comparação.

## Ferramentas
 - **Regressão Visual**
   - [BackstopJS](https://garris.github.io/BackstopJS/) (Gratuito) - Open-source para testes de aplicações web.
   - [Percy](https://percy.io/) (Uso gratuito limitado a 5.000 snapshots por mês)
   - Continua
 
 - **Snapshot**
   - [Jest](https://jestjs.io/pt-BR/docs/snapshot-testing) (Gratuito)
 
## Referências
- [Ship it - Testes de regressão visual - Obtendo olhos a prova de erros](http://shipit.resultadosdigitais.com.br/blog/testes-de-regressao-visual-obtendo-olhos-a-prova-de-erros/)
- [Jest - Diferença entre teste de snapshot e teste de regressão visual](https://jestjs.io/pt-BR/docs/snapshot-testing#qual-%C3%A9-a-diferen%C3%A7a-entre-teste-de-snapshot-e-teste-de-regress%C3%A3o-visual)
- [Medium Agnaldo Vilariano - Configurando o BackstopJS](https://medium.com/@vilariano/visual-regression-testing-c84eaf4e5254)
- [Iterasys - Testes de Regressão Visuais com Cypress e Percy](https://www.youtube.com/watch?v=d6-rhhoHhXs&t=5610s)
