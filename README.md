Custom Italian keyboard layout for Ubuntu, based on the US International layout.

This is a keyboard layout based on the US International layout, but with some changes to make it more suitable for Italian users.
Acute accents are available on vowels, as well as the grave accent on the letter A.

To type grave accents, just type \` followed by the letter you want to accentuate.
For acute accents, type altGr + \` followed by the letter you want to accentuate.

Example:

-   to type è, type \` followed by e.
-   to type é, type altGr + \` followed by e.

[img1]: ./images/keyboard-layout.png "Keyboard layout"

## Installation on Ubuntu

Open a terminal and type the following commands:

```bash
cd /usr/share/X11/xkb/symbols
sudo touch us_it
sudo nano us_it
```

Copy the contents of the file `us_it` from this repository and paste them into the file you just created.

Then, open the file `/usr/share/X11/xkb/rules/evdev.xml` with your favorite text editor, find `</layoutList>` and add the following lines right before it:

```xml
<layout>
	<configItem>
		<name>us_it</name>
		<shortDescription>us_it</shortDescription>
		<description>Italian (US, intl., with AltGr dead keys)</description>
		<languageList>
			<iso639Id>eng</iso639Id>
		</languageList>
	</configItem>
	<variantList/>
</layout>
```

Finally, reboot your computer or log out/login and you should be able to select the new layout from the keyboard settings.

You'll find the new layout under the name "Italian (US, intl., with AltGr dead keys)" the with English (United States) language.
