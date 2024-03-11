# desafioEntregable

README: Explicación del Código
Este README proporciona una explicación detallada del código proporcionado, que se centra en una clase llamada ProductManager y su uso para gestionar productos.

Clase ProductManager
La clase ProductManager se encarga de administrar los productos. Tiene dos métodos principales: create() y read().

Método create(data)
Este método se utiliza para crear un nuevo producto y agregarlo a la lista de productos gestionados por ProductManager.

create(data) {
const product = {
id:
ProductManager.#products.length === 0
? 1
: ProductManager.#products[ProductManager.#products.length - 1].id + 1,
title: data.title,
photo: data.photo,
category: data.category,
price: data.price,
stock: data.stock,
};
ProductManager.#products.push(product);
console.log("Producto creado");
}

El método create() toma un objeto data como argumento, que contiene la información del producto a crear, como el título, la foto, la categoría, el precio y el stock.
Se genera un nuevo objeto product con los datos proporcionados y se le asigna un id. Si no hay productos en la lista, el id se establece en 1; de lo contrario, se asigna un id que es uno más que el id del último producto en la lista.
El nuevo producto se agrega a la lista de productos ProductManager.#products.
Se imprime un mensaje indicando que el producto ha sido creado.
Método read()
Este método devuelve la lista de productos gestionados por ProductManager.

read() {
return ProductManager.#products;
}

El método read() simplemente devuelve la lista de productos ProductManager.#products.

const gestorDeProductos = new ProductManager();

Se crea una nueva instancia de ProductManager llamada gestorDeProductos.

gestorDeProductos.create({
title: "remera",
photo: "remera.png",
category: "ropa",
price: 80,
stock: 1000,
});

// Crear más productos aquí...

Se utilizan llamadas al método create() de gestorDeProductos para agregar nuevos productos. Cada llamada proporciona los datos del producto a crear.

console.log(gestorDeProductos.read());

Finalmente, se imprime en la consola la lista de productos gestionados por gestorDeProductos utilizando el método read().
Este README proporciona una visión general del código y explica cómo se utiliza la clase ProductManager para gestionar productos.



Gestor de Usuarios
Este repositorio presenta un gestor de usuarios desarrollado en JavaScript, proporcionando funcionalidades para la creación y lectura de usuarios mediante la clase UserManager.

Funcionalidades
Crear Usuario: El método create permite la creación de usuarios con datos como foto, correo electrónico y contraseña, asignándoles un ID único automáticamente.

Leer Usuarios: El método read devuelve una lista de todos los usuarios existentes.

Implementación
Clase UserManager: Encargada de gestionar la creación y lectura de usuarios.

Atributo Privado #users: Utiliza un atributo estático privado #users para almacenar todos los usuarios creados, asegurando su encapsulamiento dentro de la clase.

Método create: Crea un nuevo usuario con un ID único basado en el último ID existente o 1 si es el primer usuario, y lo agrega a la lista de usuarios.

Método read: Devuelve la lista de todos los usuarios almacenados en el gestor.

Uso
Para emplear el gestor de usuarios, simplemente se instancia un objeto de la clase UserManager. Luego, se pueden crear usuarios utilizando el método create, proporcionando los datos necesarios. Para visualizar todos los usuarios almacenados, se utiliza el método read.
