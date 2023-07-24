# challenge-socket

## Comandos

- `npm start`: Levanta el proyecto en el puerto 8080.
- `npm run dev`: Levanta el proyecto y actualiza el servidor con cada cambio guardado.

## Rutas

- [localhost:8080](localhost:8080): Listado de productos
- [localhost:8080/realtimeproducts](localhost:8080/realtimeproducts): Listado de productos con Socket.io integrado
- [localhost:8080/chat](localhost:8080/chat): Sala de chat con Socket.io integrado

## Endpoints

### Products

- `GET /api/products`: Retorna todos los productos.
- `GET /api/products/:id`: Retorna el producto por id.
- `POST /api/products`: Crea un producto nuevo. Se debe enviar con archivo de imagen. Notifica del evento con Socket.io.
- `PUT /api/products/:id`: Edita el producto. Se debe enviar con archivo de imagen. Notifica del evento con Socket.io.
- `DELETE /api/products/:id`: Elimina el producto enviado. Notifica del evento con Socket.io.

### Cart

- `GET /api/carts`: Retorna todos los carts.
- `GET /api/carts/:id`: Retorna el cart por id.
- `POST /api/carts`: Crea un cart nuevo.
- `POST /api/carts/product/:productId`: Agrega un producto al cart. Si ya existe, aumenta su cantidad en uno. Valida que tanto el cart como el product existan.

### Chat

- `GET /api/chat`: Retorna todos los mensajes.
- `POST /api/chat`: Guarda un mensaje nuevo. Notifica el evento con Socket.io.
