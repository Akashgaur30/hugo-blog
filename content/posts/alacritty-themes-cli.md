---
title: "Alacritty Themes Cli"

date: 2022-11-19
url: /alacritty-themes-cli/
categories:
  - Linux
tags:
  - Ubuntu
draft: false
---

![Cover image for alacritty-themes: A CLI tool to set themes for alacritty terminal](https://res.cloudinary.com/practicaldev/image/fetch/s--zYhilofd--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/i/6d2ojdh6y7vbmy3i4pt4.png)

## What is alacritty?

You can config your alacritty terminal by having a config file called `alacritty.yml` in your home folder like `~/.config/alacritty/alacritty.yml`

## alacritty-themes CLI

Configuring your terminal with yml files is definitely fun. But when it comes to customizing colors it definitely needs an intuitive tool for the job. That's why I have created [alacritty-themes](https://github.com/rajasegar/alacritty-themes) for that.

To find the list of themes, you can visit the alacritty [wiki page](https://github.com/alacritty/alacritty/wiki/Color-schemes)

The CLI offers 50+ Themes to choose from, an option to create your `alacritty.yml` config file with a simple, easy and intuitive user experience.

It is using `yaml` and `inquirer` npm packages for parsing the config yml and giving a list of themes to choose from the terminal respectively.

## How do I install it?

Install the `alacritty-themes` package globally with [npm](https://npmjs.com/)

```
npm i -g alacritty-themes
```

If you are using `npx` you don't have to install the package:

## How do I select themes?

[![alacritty-themes demo gif](https://res.cloudinary.com/practicaldev/image/fetch/s--zPC5awo0--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_880/https://github.com/rajasegar/alacritty-themes/raw/master/demo.gif)](https://res.cloudinary.com/practicaldev/image/fetch/s--zPC5awo0--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_880/https://github.com/rajasegar/alacritty-themes/raw/master/demo.gif)

Choose the theme from the list of options and press `Enter` to apply.
You can also navigate with `j` and `k` keys for up/down, courtesy of inquirer. The list of
options are cycled through automatically so you can go to the last theme
by just pressing `up arrow` key.

I am using the `One-Dark` theme, you also have popular themes like Dracula, Monokai, etc.,

If no `alacritty.yml` is found in your `$HOME` path, it will ask you to create one.
You can choose to create one by confirming (`y/n`) and apply the selected theme.

## Bonus Tip: Alias

You can also create an alias for `alacritty-themes` like `at`
Just append this below line to your `~/.bashrc` or `~/.bash_profile`

```
alias at='alacritty-themes'
```

Now you can simply use `at` to choose themes for your alacritty terminal.
