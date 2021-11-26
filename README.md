# Voice-do-macaco
Feature: HU01 - Como especialista quiero que la app me deje ver cuanto tiempo usa mi paciente la app para asegurarme que esta siguiendo mis consejos

Scenario: E01: Ver el tiempo que le dedica al app
TA01:
    Given que me encuentro en el home de la app
    When entre en ajustes y seleccione ActiveTime
    Then podre ver cuanto tiempo estuvo activo

    Examples:   
        |  Home  | Ajustes |           ActiveTime          |
        |  xi31  |   x31   | "Home - Ajustes - ActiveTime" |

Scenario: E02: No ver el tiempo que le dedica a la app
TA02:
    Given que me encuentro en el home de la app
    When entre en ajustes y seleccione ActiveTime, si el usuario no estuvo activo más de 30 minutos,
    Then no podre ver el tiempo activo y me llegara un mensaje diciendo de no estuvo activo.

    Examples:
        | Home | Ajustes |     ActiveTime      |
        | xi32 |   x32   | "No estuvo activo"  |