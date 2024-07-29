# Tech Challenge

## Fluxo de produto
- Ao iniciar a aplicação produtos são cadastrados no banco através de uma função com listener

## Fluxo de fake checkout

- A cada 2 minutos uma função schedulada é trigada para mover os status do pedido:
  Recebido -> Em preparação -> Pronto -> Finalizado


- A cada 2 minutos pedidos com status Finalizado são removidos do banco.

## Categorias de compra
- Lanche
- Sobremesa
- Acompanhamento
- Bebida

## Pagamentos
Ao receber um pedido é gerado um evento de pagamento CREATED na api de Pagamentos.
Uma vez que o pagamento é realizado é feito uma requisição à loja com o evento APPROVED devolvendo o id do pagamento. 
Esse processo promove o pedido para o status "Em preparação".

## Swagger
- http://localhost:31300/swagger-ui/index.html (Loja)
- http://localhost:31301/swagger-ui/index.html (Pagamentos)

## Arquitetura do sistema
<img width="729" alt="image" src="https://github.com/user-attachments/assets/9e9c3b7d-978c-49dc-862a-9015fb6e9e0f">
