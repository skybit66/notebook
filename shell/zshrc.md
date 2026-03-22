# If you come from bash you might have to change your $PATH.
# export PATH=$HOME/bin:/usr/local/bin:$PATH

# Path to your oh-my-zsh installation.
export ZSH="$HOME/.oh-my-zsh"

# Set name of the theme to load --- if set to "random", it will
# load a random theme each time oh-my-zsh is loaded, in which case,
# to know which specific one was loaded, run: echo $RANDOM_THEME
# See https://github.com/ohmyzsh/ohmyzsh/wiki/Themes
# ZSH_THEME="robbyrussell"
ZSH_THEME="agnoster"

# Set list of themes to pick from when loading at random
# Setting this variable when ZSH_THEME=random will cause zsh to load
# a theme from this variable instead of looking in $ZSH/themes/
# If set to an empty array, this variable will have no effect.
# ZSH_THEME_RANDOM_CANDIDATES=( "robbyrussell" "agnoster" )

# Uncomment the following line to use case-sensitive completion.
# CASE_SENSITIVE="true"

# Uncomment the following line to use hyphen-insensitive completion.
# Case-sensitive completion must be off. _ and - will be interchangeable.
# HYPHEN_INSENSITIVE="true"

# Uncomment one of the following lines to change the auto-update behavior
# zstyle ':omz:update' mode disabled  # disable automatic updates
# zstyle ':omz:update' mode auto      # update automatically without asking
# zstyle ':omz:update' mode reminder  # just remind me to update when it's time

# Uncomment the following line to change how often to auto-update (in days).
# zstyle ':omz:update' frequency 13

# Uncomment the following line if pasting URLs and other text is messed up.
# DISABLE_MAGIC_FUNCTIONS="true"

# Uncomment the following line to disable colors in ls.
# DISABLE_LS_COLORS="true"

# Uncomment the following line to disable auto-setting terminal title.
# DISABLE_AUTO_TITLE="true"

# Uncomment the following line to enable command auto-correction.
# ENABLE_CORRECTION="true"

# Uncomment the following line to display red dots whilst waiting for completion.
# You can also set it to another string to have that shown instead of the default red dots.
# e.g. COMPLETION_WAITING_DOTS="%F{yellow}waiting...%f"
# Caution: this setting can cause issues with multiline prompts in zsh < 5.7.1 (see #5765)
# COMPLETION_WAITING_DOTS="true"

# Uncomment the following line if you want to disable marking untracked files
# under VCS as dirty. This makes repository status check for large repositories
# much, much faster.
# DISABLE_UNTRACKED_FILES_DIRTY="true"

# Uncomment the following line if you want to change the command execution time
# stamp shown in the history command output.
# You can set one of the optional three formats:
# "mm/dd/yyyy"|"dd.mm.yyyy"|"yyyy-mm-dd"
# or set a custom format using the strftime function format specifications,
# see 'man strftime' for details.
# HIST_STAMPS="mm/dd/yyyy"

# Would you like to use another custom folder than $ZSH/custom?
# ZSH_CUSTOM=/path/to/new-custom-folder

# Which plugins would you like to load?
# Standard plugins can be found in $ZSH/plugins/
# Custom plugins may be added to $ZSH_CUSTOM/plugins/
# Example format: plugins=(rails git textmate ruby lighthouse)
# Add wisely, as too many plugins slow down shell startup.
#plugins=(git)
plugins=(
  git
  zsh-autosuggestions
  zsh-syntax-highlighting
)

source $ZSH/oh-my-zsh.sh
source ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh

# User configuration

# export MANPATH="/usr/local/man:$MANPATH"

# You may need to manually set your language environment
# export LANG=en_US.UTF-8

# Preferred editor for local and remote sessions
# if [[ -n $SSH_CONNECTION ]]; then
#   export EDITOR='vim'
# else
#   export EDITOR='mvim'
# fi

# Compilation flags
# export ARCHFLAGS="-arch x86_64"

# Set personal aliases, overriding those provided by oh-my-zsh libs,
# plugins, and themes. Aliases can be placed here, though oh-my-zsh
# users are encouraged to define aliases within the ZSH_CUSTOM folder.
# For a full list of active aliases, run `alias`.
#
# Example aliases
# alias zshconfig="mate ~/.zshrc"
# alias ohmyzsh="mate ~/.oh-my-zsh"

# lin start ===

#export RBENV_ROOT=$(brew --prefix rbenv) 
#export PATH=$RBENV_ROOT/bin:$PATH
#eval "$(rbenv init -)"

eval "$(/opt/homebrew/bin/brew shellenv)"
#export RUBY_CONFIGURE_OPTS="--with-openssl-dir=$(brew --prefix openssl@1.1)"
export RBENV_ROOT=$(brew --prefix rbenv)
export PATH=$RBENV_ROOT/bin:$PATH
eval "$(rbenv init -)"

export OPENSSL_ROOT=$(brew --prefix openssl@1.1)
export PATH="$OPENSSL_ROOT/bin:$PATH"
export LDFLAGS="-L$OPENSSL_ROOT/lib"
export CPPFLAGS="-I$OPENSSL_ROOT/include"
export PKG_CONFIG_PATH="$OPENSSL_ROOT/lib/pkgconfig"
export RUBY_CONFIGURE_OPTS="--with-openssl-dir=$OPENSSL_ROOT"


#export RUBY_CONFIGURE_OPTS="--with-openssl-dir=$(brew --prefix openssl@1.1)"
#export LDFLAGS="-L/opt/homebrew/opt/readline/lib:$LDFLAGS"
#export CPPFLAGS="-I/opt/homebrew/opt/readline/include:$CPPFLAGS"
#export PKG_CONFIG_PATH="/opt/homebrew/opt/readline/lib/pkgconfig:$PKG_CONFIG_PATH"
#export optflags="-Wno-error=implicit-function-declaration"
#export LDFLAGS="-L/opt/homebrew/opt/libffi/lib:$LDFLAGS"
#export CPPFLAGS="-I/opt/homebrew/opt/libffi/include:$CPPFLAGS"
#export PKG_CONFIG_PATH="/opt/homebrew/opt/libffi/lib/pkgconfig:$PKG_CONFIG_PATH"

# java 
export JAVA_8_HOME=$(/usr/libexec/java_home -v1.8)
export JAVA_17_HOME=$(/usr/libexec/java_home -v17)
export JAVA_HOME=$JAVA_17_HOME
export PATH=$PATH:$JAVA_HOME/bin
alias jdk8='export JAVA_HOME=$JAVA_8_HOME'
alias jdk17='export JAVA_HOME=$JAVA_17_HOME'


# ===== Flutter 开发环境配置 =====

# Flutter SDK (根据你的安装路径调整)
export FLUTTER_HOME="$HOME/flutter_sdks/flutter_3.29.0"
export PATH="$FLUTTER_HOME/bin:$PATH"

# Android SDK
export ANDROID_HOME="$HOME/Library/Android/sdk"
export ANDROID_SDK_ROOT="$ANDROID_HOME"
export PATH="$PATH:$ANDROID_HOME/platform-tools"
export PATH="$PATH:$ANDROID_HOME/tools"
export PATH="$PATH:$ANDROID_HOME/tools/bin"
export PATH="$PATH:$ANDROID_HOME/emulator"
export PATH="$PATH:$ANDROID_HOME/cmdline-tools/latest/bin"

export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn

# node nvm
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"

# proxy
proxy() {
    local port=${2:-7897}  # 默认端口 7897
    case "$1" in
        on)
            export https_proxy="http://127.0.0.1:$port"
            export http_proxy="http://127.0.0.1:$port"
            export all_proxy="socks5://127.0.0.1:$port"
            echo "✅ 代理已启用 (端口: $port)"
            # 检测代理是否真正生效
            if ! curl -s --connect-timeout 3 --max-time 5 https://www.google.com > /dev/null; then
                echo "⚠️  警告: 无法通过代理访问 Google，可能代理未运行或端口错误"
                echo "   请检查 是否已启动并监听 $port 端口"
            else
                echo "🌐 代理连接测试：成功"
            fi
            ;;
        off)
            unset https_proxy http_proxy all_proxy
            echo "📴 代理已关闭"
            ;;
        status)
            if [ -n "$http_proxy" ]; then
                echo "🌐 代理状态: ON"
                echo "   HTTP: $http_proxy"
                echo "   HTTPS: $https_proxy"
                echo "   ALL: $all_proxy"
            else
                echo "📴 代理状态: OFF"
            fi
            ;;
        *)
            echo "用法: proxy [on|off|status] [端口号]"
            echo "示例: proxy on 7890    # 使用 7890 端口"
            echo "      proxy off        # 关闭代理"
            ;;
    esac
}


# lin end ===

