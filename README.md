<div align="center">

## A small bit of code to make your form stay on top\!


</div>

### Description

This code will make your form stay on top of any other windows running, just like winamp stays on top.
 
### More Info
 
just make a new form and make a module and follow instructions below.. if you already have a form and or a module just add the code below to them

do not make a large form stay on top or you will not be able to see the other apps that are open


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Kevin Nading](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/kevin-nading.md)
**Level**          |Unknown
**User Rating**    |3.9 (31 globes from 8 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Custom Controls/ Forms/  Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/custom-controls-forms-menus__1-4.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/kevin-nading-a-small-bit-of-code-to-make-your-form-stay-on-top__1-2875/archive/master.zip)

### API Declarations

```
'put this stuff in your new module
Declare Function SetWindowPos Lib "user32" (ByVal hwnd As Long, ByVal hWndInsertAfter As Long, ByVal x As Long, ByVal y As Long, ByVal cx As Long, ByVal cy As Long, ByVal wFlags As Long) As Long
Global Const conHwndTopmost = -1
Global Const conSwpNoActivate = &H10
Global Const conSwpShowWindow = &H40
```


### Source Code

```
'just put this line in your form_load event
SetWindowPos hwnd, conHwndTopmost, 100, 100, 400, 141, conSwpNoActivate Or conSwpShowWindow
```

