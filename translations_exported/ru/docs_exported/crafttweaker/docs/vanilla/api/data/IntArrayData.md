# IntArrayData



Этот класс был добавлен модом с mod-id `crafttweaker`. Так что если вы хотите использовать эту функцию, вам нужно установить этот мод.

## Импорт класса
Вам может потребоваться импортировать пакет, если вы столкнетесь с какими-либо проблемами (например, с заливкой массива), так что лучше быть в безопасности, чем извиняться и добавлять импорт.
```zenscript
crafttweaker.api.data.IntArrayData
```

## Implemented Interfaces
IntArrayData реализует интерфейсы ниже. That means any method available to them can also be used on this class.
- [crafttweaker.api.data.ICollectionData](/vanilla/api/data/ICollectionData)
- [crafttweaker.api.data.IData](/vanilla/api/data/IData)

## Constructors
```zenscript
new crafttweaker.api.data.IntArrayData(internal as int[]);
```
| Параметр | Тип   | Description          |
| -------- | ----- | -------------------- |
| internal | int[] | Описание отсутствует |



## Methods
### add

```zenscript
[4, 128, 256, 1024].add(value as crafttweaker.api.data.IData);
[4, 128, 256, 1024].add("сегодня");
```

| Параметр | Тип                                                    | Description                  |
| -------- | ------------------------------------------------------ | ---------------------------- |
| value    | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | The value to add to the list |



```zenscript
[4, 128, 256, 1024].add(index as int, value as crafttweaker.api.data.IData);
[4, 128, 256, 1024].add(1, "красиво");
```

| Параметр | Тип                                                    | Description                                                          |
| -------- | ------------------------------------------------------ | -------------------------------------------------------------------- |
| index    | int                                                    | The index to add to. Subsequent items will be moved one index higher |
| value    | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | The value to add to the list                                         |


### asList

Gets a List<IData> representation of this IData, returns null on anything but [crafttweaker.api.data.ListData](/vanilla/api/data/ListData).

 Returns: `null if this IData is not a list.`

Тип возврата: Список&lt;[crafttweaker.api.data.IData](/vanilla/api/data/IData)&gt;

```zenscript
[4, 128, 256, 1024].asList();
```

### asMap

Gets a Map<String, IData> representation of this IData, returns null on anything but [crafttweaker.api.data.MapData](/vanilla/api/data/MapData).

 Returns: `null if this IData is not a map.`

Возврат типа: [crafttweaker.api.data.IData](/vanilla/api/data/IData)[String]

```zenscript
[4, 128, 256, 1024].asMap();
```

### asString

Gets the String representation of this IData

 Returns: `String that represents this IData (value and type).`

Return type: String

```zenscript
[4, 128, 256, 1024].asString();
```

### clear

Removes every element in the list

```zenscript
[4, 128, 256, 1024].clear();
```

### contains

Checks if this IData contains another IData, mainly used in subclasses of [crafttweaker.api.data.ICollectionData](/vanilla/api/data/ICollectionData), is the same as an equals check on other IData types

 Возвращается: `истина, если указанная IData содержится в этой IData`

Return type: boolean

```zenscript
[4, 128, 256, 1024].contains(data as crafttweaker.api.data.IData);
[4, 128, 256, 1024].contains("Display");
```

| Параметр | Тип                                                    | Description                      |
| -------- | ------------------------------------------------------ | -------------------------------- |
| data     | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | data to check if it is contained |


### copy

Makes a copy of this IData.

 IData is immutable by default, use this to create a proper copy of the object.

 Returns: `a copy of this IData.`

Тип возврата: [crafttweaker.api.data.IData](/vanilla/api/data/IData)

```zenscript
[4, 128, 256, 1024].copy();
```

### get

Retrieves the [crafttweaker.api.data.IData](/vanilla/api/data/IData) stored at the given index. Возвраты: `The [crafttweaker.api.data.IData](/vanilla/api/data/IData)`

Тип возврата: [crafttweaker.api.data.IData](/vanilla/api/data/IData)

```zenscript
[4, 128, 256, 1024].get(index as int);
[4, 128, 256, 1024].get(0);
```

| Параметр | Тип | Description         |
| -------- | --- | ------------------- |
| index    | int | The index (0-based) |


### getId

Gets the ID of the internal NBT tag.

 Used to determine what NBT type is stored (in a list for example)

 Returns: `ID of the NBT tag that this data represents.`

Тип возврата: байт

```zenscript
[4, 128, 256, 1024].getId();
```

### getString

Gets the String representation of the internal INBT tag

 Returns: `String that represents the internal INBT of this IData.`

Return type: String

```zenscript
[4, 128, 256, 1024].getString();
```

### remove

Removes the [crafttweaker.api.data.IData](/vanilla/api/data/IData) stored at the given index. Возвращается: `The [crafttweaker.api.data.IData](/vanilla/api/data/IData), который был удален`

Тип возврата: [crafttweaker.api.data.IData](/vanilla/api/data/IData)

```zenscript
[4, 128, 256, 1024].remove(index as int);
[4, 128, 256, 1024].remove(0);
```

| Параметр | Тип | Description         |
| -------- | --- | ------------------- |
| index    | int | The index (0-based) |


### set

Устанавливает элемент по указанному индексу для заданного значения Возвращается: `Значение замены`

Тип возврата: [crafttweaker.api.data.IData](/vanilla/api/data/IData)

```zenscript
[4, 128, 256, 1024].set(index as int, value as crafttweaker.api.data.IData);
[4, 128, 256, 1024].set(0, "Bye");
```

| Параметр | Тип                                                    | Description                |
| -------- | ------------------------------------------------------ | -------------------------- |
| index    | int                                                    | The index to set (0-based) |
| value    | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | The new Value              |



## Свойства

| Название | Тип | Имеет Getter | Имеет Setter |
| -------- | --- | ------------ | ------------ |
| size     | int | true         | false        |

