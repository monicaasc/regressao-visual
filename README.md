## O que é testes de regressão visual?

Testes de regressão visual (Visual Regression Tests/VRT) são testes de alto nível que conseguem expor qualquer alteração visual de um sistema, seja em uma página específica ou em um determinado fluxo que o usuário irá percorrer. Para que isso seja feito, esse tipo de teste faz uma captura da página que está sendo testada e compara este screenshot com sua versão estável (baseline).
![](http://shipit.resultadosdigitais.com.br/images/posts/vrt_diagram.jpg)

## Teste de snapshot?

### Qual é a diferença entre teste de snapshot e teste de regressão visual?
Teste de snapshot e teste de regressão visual são duas maneiras distintas de testar interfaces de usuário, ou UIs, e eles servem para finalidades diferentes. Ferramentas de teste de regressão visual tiram screenshots de páginas da web e comparam as imagens resultantes pixel por pixel. Com testes de snapshot os valores são serializados, armazenados dentro de arquivos de texto e comparados usando um algoritmo de comparação.

## Ferramentas
### Regressão Visual
- [BackstopJS](https://garris.github.io/BackstopJS/) (Gratuito) - Open-source para testes de aplicações web.
- [Percy](https://percy.io/) (Uso gratuito limitado a 5.000 snapshots por mês)
- Continua

### Snapshot
- [Jest](https://jestjs.io/pt-BR/docs/snapshot-testing) (Gratuito)

## Referências
> [Testes de regressão visual - Obtendo olhos a prova de erros](http://shipit.resultadosdigitais.com.br/blog/testes-de-regressao-visual-obtendo-olhos-a-prova-de-erros/)
> 
> [Jest - Diferença entre teste de snapshot e teste de regressão visual](https://jestjs.io/pt-BR/docs/snapshot-testing#qual-%C3%A9-a-diferen%C3%A7a-entre-teste-de-snapshot-e-teste-de-regress%C3%A3o-visual)
