useCaseDiagram
    actor "Адміністратор (Власник)" as Admin
    
    package "Digital Menu System" {
        usecase "Реєстрація/Вхід" as UC_Auth
        usecase "Створення структури меню" as UC_Cat
        usecase "Редагування страв" as UC_Dish
        usecase "Завантаження медіа" as UC_Photo
        usecase "Генерація QR-коду" as UC_QR
    }

    Admin --> UC_Auth
    Admin --> UC_Cat
    Admin --> UC_Dish
    Admin --> UC_QR
    
    UC_Dish ..> UC_Photo : <<extend>>
    UC_Cat ..> UC_Auth : <<include>>
    UC_Dish ..> UC_Auth : <<include>>
    UC_QR ..> UC_Auth : <<include>>
