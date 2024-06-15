# Ruby (for Jekyll)

[CONTENT NEEDED]





## Installing for MacOS

My primary development machine is running MacOS. I've heard that things aren't as easy on Windows. I'll add the Windows instructions shortly after the work to launch JekyllFaces is done. I want to verify all the steps myself and kick the tires a bit before suggesting that you go down that road.

### Install Homebrew

Homebrew makes installing development-ish software on the Mac easier.

```Text
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Install a Version Manager

The Jekyll site recommends `chruby` for Ruby version management. I prefer `rvm`. But we'll go with the suggested tool here. To install `chruby`, run the following command.

```Text
brew install chruby ruby-install xz
```

### Install Ruby

Install the latest stable version of Ruby that's supported by Jekyll. This step may take some time.

```Text
ruby-install ruby 3.1.3
```

### Configure Your Shell

Run the commands for your shell to automatically use `chruby`.

<tabs>
<tab title="zsh">

```Text
echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
echo "chruby ruby-3.2.2" >> ~/.zshrc # run 'chruby' to see actual version
```
</tab>
<tab title="bash">

```Text
echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.bash_profile
echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.bash_profile
echo "chruby ruby-3.2.2" >> ~/.bash_profile # run 'chruby' to see actual version
```
</tab>
</tabs>

> **NOTE:** If you're not sure what shell your're using, see [this article for help](https://www.moncefbelyamani.com/which-shell-am-i-using-how-can-i-switch/).


### Verify Your Work

Let's make sure that everything is configured as needed for using Jekyll.

```Text
$ ruby --version
ruby 3.2.2 (2023-03-30 revision e51014f9c0) [x86_64-darwin22]
```

> **NOTE:** The output for my Ruby version may be different than yours. Just make sure it's version 3.1.3 or later. Also note that my processor is Intel. The Apple Silicon chips will display a different descriptor at the end of the version message.


### Troubleshooting

The steps listed above are best performed on a machine that hasn't used Ruby in the past. MacOS comes with an older version of Ruby, so you're encouraged to install the latest Ruby if possible.

> **NOTE:** If you run into issues with your MacOS installation or update, see [Install Ruby on Mac](https://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/) for detailed troubleshooting instructions.