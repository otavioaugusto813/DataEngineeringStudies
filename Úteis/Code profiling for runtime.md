#python #runTime #performance #computacao
Serve para avaliar o tempo de execução de cada linha do seu código de maneira mais automática (sem usar o módulo %timeit para cada linha, já que ele avalia o tempo total da execução)
## Carregando o módulo

``` 
%load_ext line_profiler
```
## Comando mágico para tempos linha a linha

```
%lprun -f convert_units convert_units(heroes, hts, wts)
```
O comando acima fará uma avaliação linha a linha da função chamada ()

![](../../../Anexos/Pasted%20image%2020220829223114.png)
## Gargalos
When you see certain lines of code taking up the majority of the function's runtime, it is an indication that you may want to deploy a different, more efficient technique.
