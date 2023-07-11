# UML-Exercise
To access the UML application navigate to this URL: http://www.plantuml.com/

Then insert the UML diagram code in the text box and press the "Submit" button to see the diagram image
```
@startuml
class Restaurant {
  - name: String
  - address: String
  - tables: List<Table>
  + addTable(table: Table): void
  + removeTable(table: Table): void
}

class Table {
  - tableNumber: int
  - capacity: int
  - isOccupied: boolean
  + occupyTable(): void
  + releaseTable(): void
}

class Menu {
  - items: List<MenuItem>
  + addItem(item: MenuItem): void
  + removeItem(item: MenuItem): void
}

class MenuItem {
  - name: String
  - description: String
  - price: double
}

class Order {
  - table: Table
  - items: List<MenuItem>
  + addItem(item: MenuItem): void
  + removeItem(item: MenuItem): void
  + calculateTotal(): double
}

class Payment {
  - order: Order
  - paymentMethod: String
  - amount: double
  + makePayment(): void
}

class Reservation {
  - table: Table
  - customerName: String
  - reservationTime: DateTime
  + makeReservation(): void
  + cancelReservation(): void
}

Restaurant "1" -- "0..*" Table
Restaurant "1" o-- "1" Menu
Table "1" -- "0..1" Order
Order "1" -- "0..*" MenuItem
Order "1" -- "1" Payment
Table "1" -- "0..1" Reservation
@enduml
```

![UML Exercise image1](https://github.com/luiscoco/UML-Exercise/assets/32194879/7ec6bed9-30e2-4eed-aa8c-916eb3e35068)

This is the complete UML diagram output image:
![UML output image](https://github.com/luiscoco/UML-Exercise/assets/32194879/4558f2ef-f0c9-48e7-929b-9a9f2161dd40)


