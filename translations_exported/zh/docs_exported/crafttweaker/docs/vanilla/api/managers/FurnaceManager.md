# FurnaceManager



这个类由mod-id为`crafttweaker`的模组添加. 因此，如果要使用此功能，则需要安装此mod。

## 导入相关包
如果遇到任何问题（例如强制转换数组），则可能需要导入软件包，因此，最好的方式就是导入包支持。
```zenscript
crafttweaker.api.FurnaceManager
```

## 已实现的接口
FurnaceManager implements the following interfaces. 这意味着对这个接口可用的任何方法也可以在此类上使用。
- [crafttweaker.api.brackets.CommandStringDisplayable](/vanilla/api/brackets/CommandStringDisplayable)
- [crafttweaker.api.registries.ICookingRecipeManager](/vanilla/api/managers/ICookingRecipeManager)
- [crafttweaker.api.registries.IRecipeManager](/vanilla/api/managers/IRecipeManager)

## 方法
### addJSONRecipe #添加JSON配方

基于提供的IData添加配方 提供的 IData 应该代表一个JSON数据包 ,这有效地允许您注册任何支持 IRecipeType 系统的 DataPack配方。

```zenscript
furnace.addJSONRecipe(name as String, data as crafttweaker.api.data.IData);
furnace.addJSONRecipe("recipe_name", {ingredient:{item:<item:minecraft:gold_ore>.registryName},result:<item:minecraft:cooked_porkchop>.registryName,experience:0.35 as float, cookingtime:100});
```

| 参数   | 类型                                                     | 描述                              |
| ---- | ------------------------------------------------------ | ------------------------------- |
| name | String                                                 | name of the recipe              |
| data | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | data representing the json file |


### addRecipe

添加基于给定参数的合成表

```zenscript
furnace.addRecipe(name as String, output as crafttweaker.api.item.IItemStack, input as crafttweaker.api.item.IIngredient, xp as float, cookTime as int);
furnace.addRecipe("wool2diamond", <item:diamond>, <tag:minecraft:wool>, 1.0, 0);
```

| 参数             | 类型                                                                  | 描述         |
| -------------- | ------------------------------------------------------------------- | ---------- |
| name           | String                                                              | 新的合成表名称    |
| output（输出）     | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)   | 合成表的输出物品id |
| input（输入）      | [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) | 合成表的输入成分   |
| xp             | float                                                               | 玩家获得多少经验   |
| cookTime #烧制时间 | int                                                                 | 烧制需要多长时间   |


### getAllRecipes

Return type: List&lt;[crafttweaker.api.recipes.WrapperRecipe](/vanilla/api/recipe/WrapperRecipe)&gt;

```zenscript
furnace.getAllRecipes();
```

### getRecipeByName

Return type: [crafttweaker.api.recipes.WrapperRecipe](/vanilla/api/recipe/WrapperRecipe)

```zenscript
furace.getRecipeByname(名称为字符串)；
```

| 参数   | 类型     | 描述                      |
| ---- | ------ | ----------------------- |
| name | String | No description provided |


### getRecipesBy输出

Return type: List&lt;[crafttweaker.api.recipes.WrapperRecipe](/vanilla/api/recipe/WrapperRecipe)&gt;

```zenscript
furnace.getRecipesByOutput(输出为 craftbiner.api.item.IIngredient);
```

| 参数         | 类型                                                                  | 描述                      |
| ---------- | ------------------------------------------------------------------- | ----------------------- |
| output（输出） | [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) | No description provided |


### removeAll

Remove all recipes in this registry

```zenscript
furnace.removeAll();
```

### removeByModid

Remove recipe based on Registry name modid

```zenscript
furnace.removeByModid(modid as String);
furnace.removeByModid("minecraft");
```

| 参数    | 类型     | 描述                             |
| ----- | ------ | ------------------------------ |
| modid | String | modid of the recipes to remove |



通过添加排除检查，删除基于注册表名称的配方，这样除了指定的几个选项之外，您可以删除整个模组。

```zenscript
furnace.removeByModed(mody as String, exclusion as craftweeker.api.recipe.RecipeFilter);
furace.removeByModed("minecraft", (name as string) => {return name == "orange_wool";});
```

| 参数    | 类型                                                              | 描述                             |
| ----- | --------------------------------------------------------------- | ------------------------------ |
| modid | String                                                          | modid of the recipes to remove |
| 不包含   | [制作器.api.recipe.RecipeFilter](/vanilla/api/recipe/RecipeFilter) | 要避免被移除的配方。                     |


### removeByName

Remove recipe based on Registry name

```zenscript
furnace.removeByName(name as String);
furnace.removeByName("minecraft:furnace");
```

| 参数   | 类型     | 描述                                |
| ---- | ------ | --------------------------------- |
| name | String | registry name of recipe to remove |


### removeByRegex

Remove recipe based on regex

```zenscript
furnace.removeByRegex(regex as String);
furnace.removeByRegex("\\d_\\d");
```

| 参数    | 类型     | 描述                     |
| ----- | ------ | ---------------------- |
| regex | String | regex to match against |


### 删除合成表

Remove a recipe based on it's output.

```zenscript
furnace.removeRecipe(output as crafttweaker.api.item.IItemStack);
furnace.removeRecipe(<item:minecraft:glass>);
```

| 参数         | 类型                                                                | 描述                   |
| ---------- | ----------------------------------------------------------------- | -------------------- |
| output（输出） | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack) | output of the recipe |



移除基于输出和输入的合成表

```zenscript
furnace.removeRecipe(output as crafttweaker.api.item.IItemStack, input as crafttweaker.api.item.IIngredient);
furnace.removeRecipe(<item:minecraft:diamond>, <tag:minecraft:wool>);
```

| 参数         | 类型                                                                  | 描述          |
| ---------- | ------------------------------------------------------------------- | ----------- |
| output（输出） | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)   | 合成表的输出物品id. |
| input（输入）  | [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) | 要移除的配方的成分。  |



## 参数

| 名称            | 类型     | 可获得  | 可设置   |
| ------------- | ------ | ---- | ----- |
| commandString | String | true | false |

