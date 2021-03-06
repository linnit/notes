# Bash

## Loop through a file line-by-line

```bash
while read line; do
  echo "$p"
done < filename
```


   ## Event Designators
   
       An event designator is a reference to a command line entry in the  his‐
       tory  list.   Unless  the reference is absolute, events are relative to
       the current position in the history list.

       !      Start a history substitution, except when followed by  a  blank,
              newline,  carriage return, = or ( (when the extglob shell option
              is enabled using the shopt builtin).
       !n     Refer to command line n.
       !-n    Refer to the current command minus n.
       !!     Refer to the previous command.  This is a synonym for `!-1'.
       !string
              Refer to the most recent command preceding the current  position
              in the history list starting with string.
       !?string[?]
              Refer  to the most recent command preceding the current position
              in the history list containing string.  The trailing  ?  may  be
              omitted if string is followed immediately by a newline.
       ^string1^string2^
              Quick  substitution.   Repeat  the  previous  command, replacing
              string1 with string2.  Equivalent  to  ``!!:s/string1/string2/''
              (see Modifiers below).
       !#     The entire command line typed so far.

