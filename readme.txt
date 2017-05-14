A "Forked" and modified version of http://syntax.jedit.org/

Why change anything? The one on their site currently didn't compile when I wanted to
use it in my Java 8 projects. The immediate problem being that 'enum' was used as
a variable name (obvious problems there).

The only added feature currently:
Ability to enable/disable VK_TAB converting into VK_SPACE*4 (like most code editors).

This feature is achieved by use of a static boolean in JEditTextArea.java,
To use this feature: JEditTextArea.setTabConvert(boolean); //Disable by default (like normal)
The InputHandler.insert_tab class (ln 680) is modified to get this static boolean and do the conversion.