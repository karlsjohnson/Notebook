# Scripting

Recording a macroEdit
Each register is identified by a letter a to z.
To enter a macro, type: `q<letter><commands>q`
To execute the macro `<number>` times (once by default), type:`<number>@<letter>`

So, the complete process looks like:
qd start recording to register d
... your complex series of commands
q stop recording
@d execute your macro
@@ execute your macro again
