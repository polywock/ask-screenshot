
# Ask Screenshot: Advanced template options 

### Ask command 

Let's create a template in screenshot mode to translate a screenshot's text into Portuguese. 

```
Translate into Portuguese.
```

That's nice, but if I don't always want to translate into Portuguese. Instead of defining a fixed language, we can use the `{{ask}}` command.

```
Translate into {{ask}}.
```

That's better, now it opens a dialogue box so we can input any language. 

To make it even better, we change the default prompt from `Provide context...` to something more relevant. 

```
Translate into {{ ask = Which language? }}.
```

Great, but what if you often translate into Portuguese and don't want to always retype it? You can define a default value. 

```
Translate into {{ ask = Which language? :: default = Portuguese }}.
```

#### `default`

Default remembers your previous value. In this example, the first time it will show Portuguese, but if you type in Spanish, next time it will show Spanish. 
```
Translate into {{ ask = Which language? :: default = Portuguese }}.
```

#### `default2`

`default2` will always show Portuguese.
```
Translate into {{ ask = Which language? :: default2 = Portuguese }}.
```

#### `default3`

`default3` will show an empty dialogue box, but if you enter nothing, it will use Portuguese. This is helpful if you like less clutter. 
```
Translate into {{ ask = Which language? :: default3 = Portuguese }}.
```





### Selection mode 
By default, templates in selection mode automatically include the selection in the end of the text block. However, with the `{{selection}}` placeholder, you can place it wherever you wish. The placeholder will be replaced with the currently selected text. 

```text
Rewrite the following text:

{{selection}}

Make it appropiate for the workplace. 
```