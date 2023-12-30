Downloaded v2 only from the site.
        https://www.autohotkey.com/

EXAMPLES:

        ; hotstrings - expand 'btw' to 'By the way' as you type.
::btw::By the way

        ; hotkeys - press winkey-z to go to Google.
#z::Run "http://google.com"

        ; copy text to the clipboard, modify it, paste it back
^+k:: ; ctrl-shift-k
{
    ClipSave := ClipboardAll()                                     ; store current clipboard
    A_Clipboard := ""                                              ; clear the clipboard
    Send "^c"                                                      ; copy selected text
    if ClipWait(1)                                                 ; wait up to a second for content
    {
        ; wrap it in html-tags
        A_Clipboard := "<i>" A_Clipboard "</i>"
        Send "^v"                                                  ; paste
        Sleep 500                                                  ; wait for Windows to complete paste
    }
    A_Clipboard := ClipSave                                        ; restore old clipboard content
    ClipSave := ""                                                 ; clear variable
}



        ; Easy to make GUIs
MyGui := Gui()
MyGui.Add("Text",, "Enter your name")
MyGui.Add("Edit", "w150 vName")
MyGui.Add("Button",, "OK").OnEvent("Click", SayHello)
MyGui.Show()
Return

SayHello(*)
{
    Saved := MyGui.Submit()
    MsgBox "Hello " Saved.Name
    ExitApp
}



     Array Objects
Colors := "Red,Green,Blue"                  ; string
ColorArray := StrSplit(Colors, ",")         ; create array

ColorArray.Push("Purple")                   ; add data

for index, element in ColorArray            ; Read from the array
    MsgBox "Color " index " = " element













Rossetta Code : docs, examples, downloads.
        https://rosettacode.org/wiki/Category:AutoHotkey