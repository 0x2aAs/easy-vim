# Vim navigation
## within a document
You edit a document and press ``gg`` to get to the top and then you want to go back where you were editing. I used undo/redo quite a while I think, until I got annoyed so much. Fortunately there are much better ways to deal with this.<br />

Go back to...
```
``  position before jump
`.  last edit
```
<br />

In another situation you were editing line xx, then you did some changes in line yy and finally something in zz. To go back and forth in the history of your edits (no matter if you were in normal or insert mode):
```
g;  go edits backwards
g,  go edits forwards
```
<br />

If you were explicitly editing in insert mode and want to continue there, use:
```       
`^  position where INSERT mode was left
gi  same, but also start insert mode
```
<br />
When you jumped/moved across a document, no matter if you were editing anything, Vim also has a history for this:
```
<C-o> go to previous cursor positions (means press 'Ctrl' and 'o' together)
<C-i> opposite direction
```
<br />

And for faster navigation between different parts of a document you can always set marks:
```
mx   this sets a mark called x
`x   go to mark x
```
<br />

Instead of the letter x you can of course use any other one, including numbers. If you want to replace a mark, just set it at another position. 
<br />

To jump between code blocks/paragraphs:
```
{  jump up
}  jump down
```
<br/>

Fast search:
```
*   does a / search for the word under the cursor
#   other direction
```
<br />

## within a line:
```
%   jump between equal brackets  
0   BOL blank                 $   EOL blank
^   BOL non-blank             g_  EOL non-blank
fx  go to next x              tx  put cursor before next x       use , and ; to move to next/previous occurence of x
Fx  same other direction      Tx  same other direction           use , and ; to move to next/previous occurence of x
```



