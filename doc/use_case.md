@startuml
left to right direction

actor "Муфаса" as Mufasa
actor "Симба" as Simba
actor "Шрам" as Scar
actor "Рафики" as Rafiki

package "Земли Прайда (PrideLands)" {
  usecase "Охотиться" as Hunt
  usecase "Вернуть трон" as Restore
  usecase "Изгнать Шрама" as Exile
  usecase "Показать истину" as ShowTruth
  usecase "Узурпировать власть" as Usurp
}

' Наследники Короля
Mufasa --> Hunt
Simba --> Hunt

' Основной сценарий Симбы
Simba --> Restore
Simba --> Exile

' Антагонист
Scar --> Usurp

' Наставник
Rafiki --> ShowTruth

' Расширения и зависимости
Restore ..> Exile : <<include>> \n(чтобы вернуть трон, \nнужно изгнать Шрама)
ShowTruth ..> Restore : <<extend>> \n(если Симба забыл кто он)
@enduml
