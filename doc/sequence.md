@startuml
title Пошаговое взаимодействие: "Круг жизни" и возвращение Короля

actor "Муфаса" as M
participant "Земли Прайда" as PL
actor "Шрам" as S
actor "Симба (Львенок)" as SimbaC
actor "Рафики" as R
actor "Симба (Король)" as SimbaK

' 1. Трагедия
M -> PL : правит()
S -> M : предательство (бросок в пропасть)
destroy M
note over S #FFAAAA: Муфаса погибает. \nШрам захватывает власть.

' 2. Изгнание
S -> SimbaC : изгнать()
SimbaC -> SimbaC : уйти в изгнание
note over SimbaC: Статус: Exile (Изгнанник)

' ... время проходит ...
SimbaC -> SimbaC : взрослеть

' 3. Возвращение и осознание (ключевое сообщение)
R -> SimbaC : показатьИстину() \n(rememberWhoYouAre)
activate R
R --> SimbaC : отражение в воде
deactivate R
note right of SimbaC: Осознание: \n"Я — король"

' 4. Смена статуса
SimbaC -> SimbaK : превращение (взрослый Король)

' 5. Финал
SimbaK -> S : битва()
SimbaK -> PL : вернутьТрон()
note over PL #AAFFAA: Земли Прайда \nвосстановлены
@enduml
