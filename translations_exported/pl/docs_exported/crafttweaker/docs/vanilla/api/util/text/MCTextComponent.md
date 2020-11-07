# Komponent MCText

This class was added by a mod with mod-id `crafttweaker`. So you need to have this mod installed if you want to use this feature.

## Importing the class
It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import.
```zenscript
crafttweaker.api.util.text.MCTextComponent
```

## Methods
### appendSibling

Typ zwrotu: [crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent)

```zenscript
myMCTextComponent.appendSibling(komponent jako crafttweaker.api.util.text.MCTextComponent);
```

| Parameter | Type                                                                                 | Description             |
| --------- | ------------------------------------------------------------------------------------ | ----------------------- |
| komponent | [crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent) | No description provided |


### appendText

Typ zwrotu: [crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent)

```zenscript
myMCTextComponent.appendText(tekst jako ciąg);
```

| Parameter | Type   | Description             |
| --------- | ------ | ----------------------- |
| tekst     | String | No description provided |


### Kopiuj surowy

Typ zwrotu: [crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent)

```zenscript
myMCTextComponent.copyRaw();
```

### createStringTextComponent

Typ zwrotu: [crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent)

```zenscript
crafttweaker.api.util.text.MCTextComponent.createStringTextComponent(text as String);
```

| Parameter | Type   | Description             |
| --------- | ------ | ----------------------- |
| tekst     | String | No description provided |


### createTranslationTextComponent

Typ zwrotu: [crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent)

```zenscript
crafttweaker.api.util.text.MCTextComponent.createTranslationTextComponent(translationKey as String);
```

| Parameter      | Type   | Description             |
| -------------- | ------ | ----------------------- |
| translationKey | String | No description provided |



Typ zwrotu: [crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent)

```zenscript
crafttweaker.api.util.text.MCTextComponent.createTranslationTextComponent(translationKey as String, args as Object[]);
```

| Parameter      | Type     | Description             |
| -------------- | -------- | ----------------------- |
| translationKey | String   | No description provided |
| args           | Object[] | No description provided |


### deepCopy

Typ zwrotu: [crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent)

```zenscript
myMCTextComponent.deepCopy();
```

### getString

Return type: String

```zenscript
myMCTextComponent.getString();
```

### getStringTruncated

Return type: String

```zenscript
myMCTextComponent.getStringTruncated(maxLen as int);
```

| Parameter | Type | Description             |
| --------- | ---- | ----------------------- |
| maxLen    | int  | No description provided |


### getUnformattedComponentText

Return type: String

```zenscript
myMCTextComponent.getUnformattedComponentText();
```

### setStyle

Typ zwrotu: [crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent)

```zenscript
myMCTextComponent.setStyle(style as crafttweaker.api.util.text.MCStyle);
```

| Parameter | Type                                                                 | Description             |
| --------- | -------------------------------------------------------------------- | ----------------------- |
| styl      | [craftaweaker.api.util.text.MCStyle](/vanilla/api/util/text/MCStyle) | No description provided |



## Properties

| Name                     | Type                                                                                                          | Has Getter | Has Setter |
| ------------------------ | ------------------------------------------------------------------------------------------------------------- | ---------- | ---------- |
| formattedText            | String                                                                                                        | true       | false      |
| siblings                 | Lista&lt;[crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent)&gt; | true       | false      |
| unformattedComponentText | String                                                                                                        | true       | false      |

## Operators
### ADD

```zenscript
myMCTextComponent + component as crafttweaker.api.util.text.MCTextComponent
```

| Parameter | Type                                                                                 | Description             |
| --------- | ------------------------------------------------------------------------------------ | ----------------------- |
| komponent | [crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent) | No description provided |
### CAT

```zenscript
myMCTextComponent ~ component as crafttweaker.api.util.text.MCTextComponent
```

| Parameter | Type                                                                                 | Description             |
| --------- | ------------------------------------------------------------------------------------ | ----------------------- |
| komponent | [crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent) | No description provided |
### SHL

```zenscript
myMCTextComponent << component as crafttweaker.api.util.text.MCTextComponent
```

| Parameter | Type                                                                                 | Description             |
| --------- | ------------------------------------------------------------------------------------ | ----------------------- |
| komponent | [crafttweaker.api.util.text.MCTextComponent](/vanilla/api/util/text/MCTextComponent) | No description provided |

## Casters

| Result type | Is Implicit |
| ----------- | ----------- |
| String      | false       |
