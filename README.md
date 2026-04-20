useCaseDiagram
    accTitle: Digital Menu System
    accDescr: Use case diagram for Administrator

    subgraph "Digital Menu System"
        UC_Auth(Реєстрація/Вхід)
        UC_Cat(Створення структури меню)
        UC_Dish(Редагування страв)
        UC_Photo(Завантаження медіа)
        UC_QR(Генерація QR-коду)
    end

    Admin((Адміністратор))

    Admin --> UC_Auth
    Admin --> UC_Cat
    Admin --> UC_Dish
    Admin --> UC_QR

    UC_Dish -.-> UC_Photo : <<extend>>
    UC_Cat -.-> UC_Auth : <<include>>
    UC_Dish -.-> UC_Auth : <<include>>
    UC_QR -.-> UC_Auth : <<include>>
