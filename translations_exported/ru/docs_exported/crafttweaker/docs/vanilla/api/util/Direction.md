# Direction

Represents a cardinal direction (north, south, east, west) and (up and down).

Этот класс был добавлен модом с mod-id `crafttweaker`. Так что если вы хотите использовать эту функцию, вам нужно установить этот мод.

## Импорт класса
Вам может потребоваться импортировать пакет, если вы столкнетесь с какими-либо проблемами (например, с заливкой массива), так что лучше быть в безопасности, чем извиняться и добавлять импорт.
```zenscript
crafttweaker.api.util.Direction
```

## Methods
### rotateY

Rotates this direction on the Y axis

 Returns: `the direction that rotated on the Y axis of this direction`

Тип возврата: [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)

```zenscript
<direction:north>.rotateY();
```

### rotateYCCW

Rotates this direction counter-clock wise on the Y axis

 Returns: `the direction that is counter clockwise on the Y axis`

Тип возврата: [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)

```zenscript
<direction:north>.rotateYCCW();
```


## Свойства

| Название        | Тип                                                                    | Имеет Getter | Имеет Setter |
| --------------- | ---------------------------------------------------------------------- | ------------ | ------------ |
| axis            | [crafttweaker.api.util.DirectionAxis](/vanilla/api/util/DirectionAxis) | true         | false        |
| axisOffset      | int                                                                    | true         | false        |
| down            | [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)         | true         | true         |
| east            | [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)         | true         | true         |
| horizontalAngle | float                                                                  | true         | false        |
| horizontalIndex | int                                                                    | true         | false        |
| index           | int                                                                    | true         | false        |
| name            | String                                                                 | true         | false        |
| north           | [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)         | true         | true         |
| opposite        | [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)         | true         | false        |
| стороны         | [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)[]       | true         | true         |
| south           | [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)         | true         | true         |
| up              | [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)         | true         | true         |
| west            | [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)         | true         | true         |
| xOffset         | int                                                                    | true         | false        |
| yOffset         | int                                                                    | true         | false        |
| zOffset         | int                                                                    | true         | false        |

