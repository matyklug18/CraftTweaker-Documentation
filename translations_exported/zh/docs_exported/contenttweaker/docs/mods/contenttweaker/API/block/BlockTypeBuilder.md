# BlockTypeBuilder

Denotes a special builder that is used for building special block types. 用于 [mods.contenttweeper.block.BlockTypeBuilder#withType](/mods/contenttweaker/API/block/BlockTypeBuilder/#withtype)

This class was added by a mod with mod-id `contenttweaker`. 因此，如果要使用此功能，则需要安装此mod。

## 导入相关包
如果遇到任何问题（例如强制转换数组），则可能需要导入软件包，因此，最好的方式就是导入包支持。
```zenscript
mods.contenttweeper.block.BlockTypeBuilder
```

## 已实现的接口
BlockTypeBuilder implements the following interfaces. 这意味着对这个接口可用的任何方法也可以在此类上使用。
- [mods.contenttweaker.api.IIsBuilder](/mods/contenttweaker/API/api/IIsBuilder)

## 方法
### build

Instructs CoT to actually build whatever this builder is supposed to be building.

```zenscript
new BlockBuilder().withType<BlockBuilderBasic>().build(resourceLocation as String);
new BlockBuilder().withType<BlockBuilderBasic>().build("my_awesome_block");
```

| 参数               | 类型     | 描述                                   |
| ---------------- | ------ | ------------------------------------ |
| resourceLocation | String | The resource path to give this block |



