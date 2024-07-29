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
![WhatsApp Image 2024-07-29 at 16 10 17](https://github.com/user-attachments/assets/09d94748-ccc4-4173-ac9f-cae6d0f0fc8d)

## Video demonstrando a arquitetura desenvolvida
https://www.youtube.com/watch?v=eDxyCAmyhk8

