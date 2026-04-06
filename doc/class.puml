@startuml
skinparam classAttributeIconSize 0

' --- Иерархия Королей ---
abstract class King {
    + правило()
    + защищатьЗемли()
}

class Mufasa extends King {
    + сила: int = 100
    + мудрость: int = 100
}

class Simba extends King {
    + сила: int = 80
    + возраст: String = "Взрослый"
    + осознатьСебя()
}

' --- Антагонист ---
class Scar {
    + хитрость: int
    + захватитьВласть()
    + изгнать()
}

' --- Ресурс ---
class PrideLands {
    + состояние: String
    + процветание: int
}

' --- Мудрый наставник ---
class Rafiki {
    + показатьИстину(с: Simba)
}

' --- Связи ---
Mufasa <|-- Simba : <<extends>> (наследует титул)
King "1" --> "1" PrideLands : управляет >

Scar --> PrideLands : пытается захватить
Rafiki --> Simba : наставляет >

note bottom of Simba
  **Симба наследует роль Короля**
  Использует полиморфизм:
  правило() работает иначе,
  чем у Муфасы (юность -> мудрость)
end note

note left of Scar
  Не входит в иерархию King,
  но перехватывает доступ
  к ресурсам через захват власти
end note
@enduml
