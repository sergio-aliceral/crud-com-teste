# Objetivo
API crud com testes unitários e de integração.

## Iniciando

- `git clone https://github.com/sergio-aliceral/crud-com-teste.git`
- `cd crud-com-teste`

## Pré-requisitos
- `mvn --version`<br>

Você deverá ver a indicação da versão do Maven instalada e a versão do JDK. Observe que o JDK é obrigatório, assim como a definição das variáveis de ambiente **JAVA_HOME** e **M2_HOME**.

## Limpar, compilar e empacotar
- `mvn clean install`<br>

Gera arquivo _crud-com-teste-1.0.0.jar_ no diretório _target_.

## Executando a aplicação
- `java -jar target/crud-com-teste-1.0.0.jar`<br>

Executa o aplicativo por meio do arquivo jar criado pelo comando `mvn clean install`, conforme comentado anteriormente.

### Endpoints

- Lista todos os produtos: `GET` http://localhost:9999/products
- Filtra os produtos: `GET` http://localhost:9999/products/search?q={name_ou_description}&min_price={preco_minimo}&max_price={preco_maximo}
- Lista um produto por id: `GET` http://localhost:9999/products/{id} 
- Cadastra um novo produto: `POST`http://localhost:9999/products

```
  {
    "name": "Lápis",
    "description": "Descrição do Lápis",
    "price": 1.50
  }
```
 
- Atualiza os dados do produto: `PUT` http://localhost:9999/products/{id}

```
{
    "name": "Lápis Alterado",
    "description": "Descrição do Lápis Alterado",
    "price": 1.51
  }
``` 
 - Remove um produto por id: `DELETE` http://localhost:9999/products/{id} 
