# Desarrollo-de-aplicaciones-IV
ACTIVIDAD 1 -  CODIGO SWITFT DE IENDA ONLINE

struct Articulo {
  let nombre: String
  let precio: Int
  var stock: Int
}

var articulos = [
  Articulo(nombre: "Zapatos", precio: 500, stock: 10),
  Articulo(nombre: "Playeras", precio: 400, stock: 40),
  Articulo(nombre: "Pantalones", precio: 300, stock: 50),
  Articulo(nombre: "Sombreros", precio: 200, stock: 100)
]

//variables para pedir datos con el teclado
var aux: String = ""
var opcionIngresada: String = aux
var cuenta: Int = 0 //aqui se almacenara la cantidad de articulos vendidos

while opcionIngresada != "2"{
  print("*****Bienvenido a la Tienda Online*****")
  print("\n")
  print("Articulos disppnibles: ")
  print("1: \(articulos[0].nombre)")
  print("Precio: $\(articulos[0].precio) pesos")
  print("Stock: \(articulos[0].stock)")
  print("\n")

  print("2: \(articulos[1].nombre)")
  print("Precio: $\(articulos[1].precio) pesos")
  print("Stock: \(articulos[1].stock)")
  print("\n")

  print("3: \(articulos[2].nombre)")
  print("Precio: $\(articulos[2].precio) pesos")
  print("Stock: \(articulos[2].stock)")
  print("\n")

  print("4: \(articulos[3].nombre)")
  print("Precio: $\(articulos[3].precio) pesos")
  print("Stock: \(articulos[3].stock)")
  print("\n")

  print("Selecciona un número de acuerdo a la acción que deseas realizar: ")
  print("\n")

  print("1.- Comprar articulos")
  print("2.- Salir")
  print("\n")

  aux = readLine()!
  opcionIngresada = aux

  switch opcionIngresada {
    case "1":  //Que articulo desea comprar
      print("Ingresa el número de articulo que deseas comprar: ")

     aux = readLine()!
     opcionIngresada = aux

    switch opcionIngresada {
      case "1":
        print("Ingresa la cantidad de \(articulos[0].nombre) que deseas comprar: ")

       aux = readLine()!
       opcionIngresada = aux

      let cantidadIngresada = Int(opcionIngresada)!
      if cantidadIngresada <= articulos[0].stock {
        articulos[0].stock = articulos[0].stock - cantidadIngresada
        cuenta = cantidadIngresada * articulos[0].precio
        print("Usted ha comprado \(cantidadIngresada) \(articulos[0].nombre)")
        print("El total a pagar es: $ \(cuenta)")
        print("Gracias por tu compra")
      } else {
          print("No hay suficiente stock, lo sentimos")
      }

      case "2":
        print("Ingresa la cantidad de \(articulos[1].nombre) que deseas comprar: ")

       aux = readLine()!
       opcionIngresada = aux

      let cantidadIngresada = Int(opcionIngresada)!
      if cantidadIngresada <= articulos[1].stock {
        articulos[1].stock = articulos[1].stock - cantidadIngresada
        cuenta = cantidadIngresada * articulos[1].precio
        print("Usted ha comprado \(cantidadIngresada) \(articulos[1].nombre)")
        print("El total a pagar es: $ \(cuenta)")
        print("Gracias por tu compra")
      } else {
          print("No hay suficiente stock, lo sentimos")
      }

      case "3":
        print("Ingresa la cantidad de \(articulos[2].nombre) que deseas comprar: ")

       aux = readLine()!
       opcionIngresada = aux

      let cantidadIngresada = Int(opcionIngresada)!
      if cantidadIngresada <= articulos[2].stock {
        articulos[2].stock = articulos[2].stock - cantidadIngresada
        cuenta = cantidadIngresada * articulos[2].precio
        print("Usted ha comprado \(cantidadIngresada) \(articulos[2].nombre)")
        print("El total a pagar es: $ \(cuenta)")
        print("Gracias por tu compra")
      } else {
          print("No hay suficiente stock, lo sentimos")
      }

      case "4":
        print("Ingresa la cantidad de \(articulos[3].nombre) que deseas comprar: ")

       aux = readLine()!
       opcionIngresada = aux

      let cantidadIngresada = Int(opcionIngresada)!
      if cantidadIngresada <= articulos[3].stock {
        articulos[3].stock = articulos[3].stock - cantidadIngresada
        cuenta = cantidadIngresada * articulos[3].precio
        print("Usted ha comprado \(cantidadIngresada) \(articulos[3].nombre)")
        print("El total a pagar es: $ \(cuenta)")
        print("Gracias por tu compra")
      } else {
          print("No hay suficiente stock, lo sentimos")
      }

    default:
    print("Opción no válida")
      
  }//fin del swich de la opcion de comprar
  case "2":
  print("Gracias por su visita, vuelva pronto!!")
    
  default:
  print("Opción no válida")
  } //fin del switch de la opcion de salir
    
}
