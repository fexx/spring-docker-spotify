# spring-docker-spotify

Projeto para demonstrar como gerar e enviar uma imagem docker usando o plugin Dockerfile-maven do spotify
Para mais detalhes acesse o [artigo no medium][artigomedium]
[artigomedium]: https://medium.com/@fernandoevangelista_28291/criando-e-enviando-imagem-docker-com-java-e-maven-4fa3c70dba0f

## Criar imagem docker

Para criar uma imagem com o plugin do maven execute: `mvn package`.

## Visualizando imagem
Para visualizar a imagem criada execute: `docker images`

A imagem será exibida
```
REPOSITORY                                                        TAG                 IMAGE ID            CREATED             SIZE
fexx182/spring-docker-spotify                                      0.0.1-SNAPSHOT      4ee224b605bb        12 seconds ago      140MB
```

## Executando container
Vamos executar o  container executando o comando:
`docker run -p 8080:8080 fexx182/spring-docker-spotify:0.0.1-SNAPSHOT`

## Enviando para o docker hub
Execute o seguinte comando:
`mvn dockerfile:push`

# Dockerfile Maven do spotify

Mais detalhes em [dockerfile-maven][dockerfilemaven]

[dockerfilemaven]: https://github.com/spotify/dockerfile-maven
