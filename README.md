# Author-Only-Interactions
A simple and understanding way to make Author only Buttons with an error message.
This would how a basic command with button would look like:

---

# Main Code

```codeblock
$nomention
$title[Example Code]
$description[Button below, click for more]
$footer[$username]
$addButton[no;AuthorButton-$authorID;Button;success;no]
```
This is how it would look like, with the ID of the button being split by `-`, so we could later split the `-` character and get the first and last split.
Pretty self explanatory, right? Now let's see how $onInteraction would look like.

---
# $onInteraction
This is where our button can be chosen, with only author being able to interact with it.

```codeblock
$nomention
$textSplit[$customID;-] $c[splitting the Button ID by -]

$if[$splitText[1]==AuthorButton] $c[Button ID]
$if[$splitText[2]==$authorID]
$ephemeral
$removeButtons
You're the author!
$else
$ephemeral
$removeButtons
You are **not** the author!
$endif
$endif
```
This is how $onInteraction would button look like, with author being only be able to select it.
Thank you for reading this, you have my respect.

---

If this helped you, star this Git, you'll be blessed with lifetime imaginary BDFD Premium :D.
Guide done by `kitten_tenacious`. Ping me in Support or DM me for further help.
