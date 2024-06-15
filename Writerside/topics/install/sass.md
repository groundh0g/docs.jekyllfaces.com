# Sass

There are many ways to install the sass compiler/transpiler to turn your sass files into vanilla css. This section describes a common way of installing the sass tools, but there are [other options](https://sass-lang.com/install/).

> **NOTE:** If you don't plan on using sass in your project, feel free to skip this section. You can create your sites in JekyllFaces using vanilla css just as easily.

## Install Sass

Depending on your machine's configuration, I recommend one of the three following installation methods.

<tabs>
<tab title="Cross-Platform (Node)">

```Text
npm install -g sass
```

This is a great option if you're already using [NodeJS](https://nodejs.org/) for other projects (like Eleventy).

To use the `npm` command, you will need to first install Node on your system.

> **NOTE:** The following instructions involve running scripts from the individual project's host site.
>
> You should verify the security and contents of any script from the internet you are not familiar with.

<br />

```Text
# installs nvm (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

# download and install Node.js (you may need to restart the terminal)
nvm install 20

# verifies the right Node.js version is in the environment
node -v # should print `v20.14.0`

# verifies the right NPM version is in the environment
npm -v # should print `10.7.0`
```

</tab>
<tab title="MacOS and Linux (Homebrew)">

```Text
brew install sass/sass/sass
```

"[Homebrew](https://brew.sh/) installs the stuff you need that Apple (or your Linux system) didn’t."

To use  the `brew` command, you will need to first install Homebrew.

<tabs>
<tab title="Command Line">

> **NOTE:** The following instructions involve running scripts from the individual project's host site.
>
> You should verify the security and contents of any script from the internet you are not familiar with.

<br />

```Text
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

</tab>
<tab title="MacOS Installer">

If you're on macOS, you can try the new .pkg installer. Download it from [Homebrew's latest GitHub release](https://github.com/Homebrew/brew/releases/latest).

> **NOTE:** I personally recommend that you use the command-line installation since this is a new feature of Homebrew.

</tab>
</tabs>

</tab>
<tab title="Windows (Chocolatey)">

```Text
choco install sass
```

[Chocolatey](https://chocolatey.org/) installs the stuff you need that Windows didn’t.

To use the `choco` command, you will need to first install Chocolatey _as an administrator_.

> **NOTE:** The following instructions involve running scripts from the individual project's host site.
>
> You should verify the security and contents of any script from the internet you are not familiar with.

<br />

```Text
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

<br />

> **NOTE:** If you would prefer to install Chocolatey as a non-admin, follow [the instructions in the documentation](https://docs.chocolatey.org/en-us/choco/setup#non-administrative-install).

</tab>
</tabs>



## Why Install Sass Separately?

Jekyll has an interesting way of incorporating Sass content into their build process. 

```Text
---
# This is Jekyll-specific, empty front matter to trigger processing
---

@use "globals/reset";

html, body {
  margin: 0;
  padding: 0;
}
```

The front matter is a marker for the Jekyll build that says, "include me!" Unfortunately, that's not valid sass markup. While it makes Jekyll happy, it really upsets other tools that process sass files, like 3rd-party transpilers and linters.
