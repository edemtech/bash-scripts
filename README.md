# bash-scripts

# Bash scripts:

alias gs='git status'
alias lf='ls -F'
alias gl='git log —decorate —graph —all —oneline'
alias gl1='git log —decorate —graph —oneline'
alias go='git checkout'
alias gc='git commit -m'
alias gca='git commit -a -m'
alias gd='git diff'
alias gm='git merge'
alias grh='git reset —hard'
alias gp='git push'
alias gf='git fetch'
alias grh1='git reset —hard HEAD~1'
alias ml='tail /var/tmp/php.mail.log -n'
alias links='ls /tools/ -all'
alias gss='git show —stat'
alias gr='grep -R —color'
alias gh1='go HEAD~1'
alias al='cat /etc/bashrc'
alias ls='ls -all'
alias grep='grep —color'
alias hosts='cat ~/.ssh/configs'

parse_git_branch() {
     git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "
