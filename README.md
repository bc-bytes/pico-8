# Misc snippets relating to pico-8

## convert_raw.py
This routine will convert raw integer cart data from an embedded pico-8 HTML project into a pico-8 cart. Note that the resulting cart file does not include a cart image, you will need to add that yourself using pico-8 (load into pico-8, run cart, press F7 to add cart image, then save with .png at the end of the file name). Instructions (using Firefox):

1. Load web page with pico-8 game embedded into HTML.
2. Run game.
3. Navigate to about:cache
4. Click "List Cache Entries" under the "disk" section.
5. In the resulting list, look for a recent key entry with a filename like "game_name.js" or "index.js" and click on it.
6. On the "Cache entry information" screen, click on the "key" link a the top of the page.
7. Near the top of the resulting page, look for a variable called "cartdat" and copy the value assigned to the variable. The value of the variable will be a sequence on integers, separated by commas enclosed in square brackets.
8. Save the contents of the clipboard into a file called "source".
9. Run the "convert_raw.py" in the same directory as the "source" file.
10. A new file file will be generated "output.p8". This is the pico-8 cart, and can now be loaded directly into pico-8.
