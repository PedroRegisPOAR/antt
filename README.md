

## Para quem usa Docker

Construindo a imagem:

```
docker build -t scrape_antt .
```

Contruída a imagem basta executar:

```
docker run -it --rm -v "$(pwd)":/code -p 8888:8888 scrape_antt bash
```

Note: é necessário expor a porta 8888, que é a porta padrão em que o
jupyter notebook roda.


No terminal interno ao contêiner rodar o seguinte comando:

```
jupyter-notebook --ip="0.0.0.0" --no-browser --allow-root
```

Este produzirá um link semelhante ao abaixo:

http://127.0.0.1:8888/?token=a99bbfc6f95d840a641125d400e2be7bc47df3005fe0a869
