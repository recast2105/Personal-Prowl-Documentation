# AnimationComponent (obsoleto)

[Read in English](README.en.md)

> **Aviso:** este componente está obsoleto. As notas abaixo documentam a implementação existente.

## Selecionar uma animação

Para executar uma animação específica, é necessário um `AssetRef` convertido para o tipo esperado. Também é possível obter uma animação da lista armazenada no `AnimationComponent` usando `GetInstance`; como esse método retorna um objeto, é necessário convertê-lo.

![Obtenção de uma referência de animação](images/get-animation-reference.png)

É possível selecionar um clip específico pelo índice.

![Seleção de clip pelo índice](images/select-clip-by-index.png)

![Exemplo adicional de seleção de animação](images/select-clip-example.png)

Outra opção é usar `RES` no `AssetRef`.

![Uso de RES no AssetRef](images/assetref-res.png)

Essas implementações dependem da lista de animações pertencente ao componente.

## State Machine com animações

Ao usar uma State Machine, compare a ação anterior (`previous`) com a atual (`current`) e atualize o valor anterior depois da comparação. Como isso acontece a cada frame, não atualizar o estado pode fazer com que a animação continue sendo repetida.

![Comparação das ações anterior e atual](images/compare-previous-current.png)

![Exemplo de atualização do estado](images/update-state.png)

![Exemplo adicional de State Machine](images/state-machine-example.png)
