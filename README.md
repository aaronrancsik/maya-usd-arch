# maya-usd
## Install
### 1. Clone this source.
`cd /tmp`
#### Choose one:
#### A. Git HTTPS 
`git clone https://github.com/aaronrancsik/maya-usd-arch.git`
#### B. Git SSH 
`git clone git@github.com:aaronrancsik/maya-usd-arch.git`
### 2. Get the source zip.
`cd /tmp/maya-usd-arch`

`cp /tmp/maya20221_BIG/Packages/MayaUSD2022-202106052251-73d6513-0.10.0-1.x86_64.rpm ./`
### 3. Create & install the package.
`makepkg -s`

`sudo pacman -U maya-usd-0.10.0-1-x86_64.pkg.tar.zst`

### 4. It's done.
