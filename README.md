# ANSI escape codes: A simple Cheat sheet
A little Cheat Sheet to implement ANSI escape codes for customizing the look of your texts in the terminal.

---

![ANSI Cheatsheet by Hugo Montoya](https://github.com/Gugor/ANSI-cheat-sheet/blob/main/ansicheetsheetbyhugomontoya.png)

# Foreword
If you have a memory like mine, this is the same of a colorfish - around 3 secs- you probably need to google every time you want to use an ANSI code for customizing the texts of the programs you create for the terminal. Bored to do so, I just created my own cheat sheet to have in hand every time I'd like to create fancy texts to show in the terminal.

Hope you will find this code usefull!
# Usage

You can add this code to your terminal config file. If you use `zsh` for example you need to go to the `.zshrc` file, and create an alias for caling it.

```Bash
vim ~/.zshrc
```

If you use just plain `bash` go here instead:
```Bash
vim ~/.bashrc
```
Add this code to the file:

```Bash
echo_colors() {
	printf "\n"
	printf "|-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=|\n"
	printf "|            \033[1;37mText Cheat Sheet\033[0m          |\n"
	printf "|         \033[0;92mcreated by\033[0m \033[1;37mHugo Montoya\033[0m      |\n"
	printf "|-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=|\n"
    # Colores en negrita (bold)
	printf "\n"
    printf "\033[1;37m=> Bold text colors\033[1;0m\n"
    printf "\033[1;30m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - Black:" "\033[1;30m"
    printf "\033[1;31m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - Red:" "\033[1;31m"
    printf "\033[1;32m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - Green:" "\033[1;32m"
    printf "\033[1;33m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - Yellow:" "\033[1;33m"
    printf "\033[1;34m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - Blue:" "\033[1;34m"
    printf "\033[1;35m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - Magenta:" "\033[1;35m"
    printf "\033[1;36m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - Cyan:" "\033[1;36m"
    printf "\033[1;37m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - White:" "\033[1;37m"
	printf "|______________________________________|\n"
    
    # Colores en claro (light)
    printf "\n\033[1;37m=> Light text colors\033[1;0m\n"
    printf "\033[0;90m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - Light Black:" "\033[0;90m"
    printf "\033[0;91m%s\033[0m \033[1;37m\t\t\t%s\033[0m\n" " - Light Red:" "\033[0;91m"
    printf "\033[0;92m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - Light Green:" "\033[0;92m"
    printf "\033[0;93m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - Light Yellow:" "\033[0;93m"
    printf "\033[0;94m%s\033[0m \033[1;37m\t\t\t%s\033[0m\n" " - Light Blue:" "\033[0;94m"
    printf "\033[0;95m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - Light Magenta:" "\033[0;95m"
    printf "\033[0;96m%s\033[0m \033[1;37m\t\t\t%s\033[0m\n" " - Light Cyan:" "\033[0;96m"
    printf "\033[0;97m%s\033[0m \033[1;37m\t\t%s\033[0m\n" " - Light White:" "\033[0;97m"
	printf "|______________________________________|\n"

	printf "\n\033[1;37m=> Background Colors:\033[0m\n"
    printf " - \033[1;40m %s \033[0m \033[1;37m\t\t%s\033[0m\n" "Background Black:" "\033[1;40m"
    printf " - \033[1;41m %s \033[0m \033[1;37m\t\t%s\033[0m\n" "Background Red:" "\033[1;41m"
    printf " - \033[1;42m %s \033[0m \033[1;37m\t\t%s\033[0m\n" "Background Green:" "\033[1;42m"
    printf " - \033[1;43m %s \033[0m \033[1;37m\t%s\033[0m\n" "Background Yellow:" "\033[1;43m"
    printf " - \033[1;44m %s \033[0m \033[1;37m\t\t%s\033[0m\n" "Background Blue:" "\033[1;44m"
    printf " - \033[1;45m %s \033[0m \033[1;37m\t%s\033[0m\n" "Background Magenta:" "\033[1;45m"
    printf " - \033[1;46m %s \033[0m \033[1;37m\t\t%s\033[0m\n" "Background Cyan:" "\033[1;46m"
    printf " - \033[1;47m %s \033[0m \033[1;37m\t\t%s\033[0m\n" "Background White:" "\033[1;47m"
	printf "|______________________________________|\n"

	printf "\n\033[1;37m=> Custom Background & Text Colors:\033[0m\n"
    printf " - \033[1;37m %s \033[0m \033[1;37m\t%s\033[0m\n" "Custom Background:" "\033[48;2;R;G;Bm"
    printf " - \033[48;2;255;27;42m %s \033[0m \033[1;37m\t%s\033[0m\n" "Custom Background:" "\033[48;2;255;27;42m"
    printf " - \033[38;2;255;27;42m %s \033[0m \033[1;37m\t%s\033[0m\n" "Custom Background:" "\033[38;2;255;27;42m"
    printf " - \033[38;2;255;27;42;48;2;255;150;190m %s \033[0m \033[1;37m\t%s\033[0m\n" "Custom Bgn & Text:" "\033[38;2;255;27;42m;48;2;255;150;190m"
	printf "|______________________________________|\n"

	printf "\n\033[1;37m=> Other Text codes:\033[0m\n"
	printf " - \033[1m%s\033[0m \033[1;37m\t\t%s\033[0m\n" "Bold:" "\033[1mTexto\033[0m"
	printf " - \033[4m%s\033[0m \033[1;37m\t\t%s\033[0m\n" "Underline:" "\033[4mTexto\033[0m"
	printf "\033[5m - %s\033[0m \033[1;37m\t\t%s\033[0m\n" "*Blink:" "\033[5mTexto\033[0m"
	printf " - \033[7m %s\033[0m \033[1;37m\t\t%s\033[0m\n" "Inverse:" "\033[7mTexto\033[0m"
	printf "|______________________________________|\n"
	printf "\n\n"
	printf "|-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=|\n"
	printf "| * If you don't see the effect of     |\n"
	printf "| of blink in the terminal now         |\n"
	printf "| you need to activate this option     |\n"
	printf "| in the settings of your terminal     |\n"
	printf "|-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=|\n"
}

alias clrs="echo_colors"
```
Now you can use the command `clrs`to show this cheat sheet every time you can't remeber an ANSI code.
```Bash
clrs
```

Feel free to customize it to your needs. 

Enjoy it!
