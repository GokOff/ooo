
```mermaid


flowchart TB
    Admin([Адміністратор])

    subgraph "Digital Menu System"
        UC_Auth(Реєстрація/Вхід)
        UC_Cat(Створення структури меню)
        UC_Dish(Редагування страв)
        UC_Photo(Завантаження медіа)
        UC_QR(Генерація QR-коду)
    end

    Admin --> UC_Auth
    Admin --> UC_Cat
    Admin --> UC_Dish
    Admin --> UC_QR

    UC_Dish -.->|extend| UC_Photo
    UC_Cat -.->|include| UC_Auth
    UC_Dish -.->|include| UC_Auth
    UC_QR -.->|include| UC_Auth


```


