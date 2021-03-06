---
title: "Daftar Command di Terminal iOS"
description: "Daftar command yang bisa digunakan di iOS, beberapa adalah command tambahan yang aku install belakangan"
date: 2020-01-29T00:36:19+09:00
draft: false
---

## Daftar Command di Terminal iOS

Cara mendapatkan daftar:
- Hubungkan perangkat iOS dengan komputer (ubuntu)
- Jalankan perintah:

```bash
compgen -c > command
```

Daftar perintah akan disimpan dalam file bernama `command`

Karena daftar perintahnya belum urut sesuai alfabet, maka aku urutkan dengan perintah:

```
sort -k1.1,1.1 command > fix
```
file yang bernama `fix` adalah hasil sorting daftar command sesuai alfabet.

Berikut ini adalah daftarnya:

```
!
.
:
BTAvrcp
BTAvrcp.sbin
BTLEServer
BTLEServer.sbin
BTMap
BTMap.sbin
BTPbap
BTPbap.sbin
BlueTool
BlueTool.sbin
DumpBasebandCrash
PerfPowerServicesExtended
WirelessRadioManagerd
WirelessRadioManagerd.sbin
[
[
[[
]]
abmlite
absd
absd.sbin
ac
accton
activator
addNetworkInterface
addNetworkInterface.sbin
addgnupghome
afktool
alias
applygnupgdefaults
apt
apt-cache
apt-cdrom
apt-config
apt-extracttemplates
apt-ftparchive
apt-get
apt-key
apt-mark
apt-sortpkgs
arch
aslmanager
aslmanager.sbin
asn1Coding
asn1Decoding
asn1Parser
autopoint
b2sum
base32
base64
basename
basenc
bash
bashbug
bg
bind
bluetoothd
bluetoothd.sbin
brctl
break
builtin
bunzip2
bzcat
bzip2
bzip2recover
caller
captoinfo
case
cat
cd
certtool
cfprefsd
cfprefsd.sbin
cfversion
chcon
chgrp
chmod
chown
chown
chown
chroot
ckksctl
cksum
clear
cmp
comm
command
compgen
complete
compopt
continue
coproc
cp
csplit
curl
curl-config
cut
cycc
cynject
date
db_archive
db_checkpoint
db_convert
db_deadlock
db_dump
db_hotbackup
db_load
db_log_verify
db_printlog
db_recover
db_replicate
db_stat
db_tuner
db_upgrade
db_verify
dd
declare
defaults
dev_mkdb
df
diff
diff3
dir
dircolors
dirmngr
dirmngr-client
dirname
dirs
disown
distnoted
distnoted.sbin
dmesg
do
done
dpkg
dpkg-deb
dpkg-divert
dpkg-maintscript-helper
dpkg-query
dpkg-split
dpkg-statoverride
dpkg-trigger
dselect
du
dumpsexp
dynamic_pager
echo
echo
ecidecid
edquota
egrep
elif
else
enable
env
envsubst
esac
eval
exec
exit
expand
export
expr
factor
fairplayd.H2
false
false
fc
fdisk
fg
fgrep
fi
file
filecoordinationd
filecoordinationd.sbin
fileproviderctl
find
fmt
fold
footprint
for
fsck
fsck.sbin
fsck_apfs
fsck_apfs.sbin
fsck_exfat
fsck_exfat.sbin
fsck_hfs
fsck_hfs.sbin
fsck_msdos
fsck_msdos.sbin
fstyp
fstyp_msdos
fstyp_ntfs
fstyp_udf
function
funzip
getconf
getopt
getopts
gettext
gettext.sh
gettextize
getty
git
git-cvsserver
git-receive-pack
git-shell
git-upload-archive
git-upload-pack
gnutls-cli
gnutls-cli-debug
gnutls-serv
gpg
gpg-agent
gpg-connect-agent
gpg-error
gpg-error-config
gpg-wks-server
gpgconf
gpgparsemail
gpgrt-config
gpgscm
gpgsm
gpgtar
gpgv
grep
groups
gssc
gunzip
gzexe
gzip
halt
hash
hdik
head
help
hidutil
history
hmac256
hostid
hostinfo
hpmdiagnose
icleaner
id
idn2
if
in
infocmp
infotocap
install
iomfsetgamma
ioreg
ioreg.sbin
iostat
ipconfig
ipconfig.sbin
jobs
join
kbdebug
kbxutil
kill
kill
killall
ksba-config
launchctl
launchctl
launchd
launchd.sbin
ldid
ldrestart
let
libassuan-config
libgcrypt-config
link
ln
local
locate
login
logname
logout
ls
ls
lsdiagnose
lz4
lz4c
lz4cat
lzcat
lzcmp
lzdiff
lzegrep
lzfgrep
lzgrep
lzless
lzma
lzmadec
lzmainfo
lzmore
mDNSResponder
mDNSResponder.sbin
mDNSResponderHelper
mDNSResponderHelper.sbin
mapfile
md5sum
mediaserverd
mediaserverd.sbin
mkdir
mkfifo
mkfile
mknod
mktemp
mktemp
mount
mount.sbin
mount_apfs
mount_apfs.sbin
mount_devfs
mount_fdesc
mount_hfs
mount_hfs.sbin
mount_nfs
mount_tmpfs
mpicalc
msgattrib
msgcat
msgcmp
msgcomm
msgconv
msgen
msgexec
msgfilter
msgfmt
msggrep
msginit
msgmerge
msgunfmt
msguniq
mv
ncurses6-config
ncursesw6-config
nettle-hash
nettle-lfib-stream
nettle-pbkdf2
newfs_apfs
newfs_apfs.sbin
newfs_hfs
newfs_hfs.sbin
nfsstat
ngettext
nice
nl
nohup
nologin
notifyd
notifyd.sbin
nproc
npth-config
numfmt
nvram
nvram.sbin
ocsptool
od
otctl
p11-kit
p11tool
pager
pagesize
passwd
paste
pathchk
pcre2-config
pcre2grep
pcre2test
pfctl
pfctl.sbin
pinky
pkcs1-conv
plistutil
popd
powerlogHelperd
pppd
pppd.sbin
pr
printenv
printf
printf
ps
psktool
ptx
pushd
pwd
pwd
pwd_mkdb
quota
quotacheck
quotaon
racoon
racoon.sbin
read
readarray
readlink
readonly
realpath
reboot
recode-sr-latin
renice
repquota
reset
return
rm
rmdir
rtadvd
rtadvd.sbin
runcon
sbdidlaunch
sbreload
scp
script
scutil
scutil.sbin
sdiff
sed
select
seq
set
sexp-conv
sftp
sh
sha1sum
sha224sum
sha256sum
sha384sum
sha512sum
shift
shopt
shred
shuf
sleep
snappy
sort
source
spindump
spindump.sbin
split
srptool
ssh
ssh-add
ssh-agent
ssh-keygen
ssh-keyscan
sshd
startupfiletool
stat
stdbuf
stty
su
sum
suspend
sw_vers
switch
sync
sysctl
sysdiagnose
syslogd
syslogd.sbin
tac
tail
tailspin
tar
tar
taskinfo
tee
test
test
then
tic
time
time
timeout
times
toe
touch
tput
tr
trap
true
true
truncate
trust
tset
tsort
tty
twackup
type
typeset
uicache
uiduid
uiopen
ulimit
umask
umount
umount.distrib
unalias
uname
uncompress
unexpand
uniq
unlink
unlz4
unlzma
unrar
unset
until
unxz
unzip
unzipsfx
update-alternatives
updatedb
uptime
users
vdir
vifs
vipw
vm_stat
vsdbutil
wait
watchgnupg
wc
wget
which
while
who
whoami
wifid
wifid.sbin
xargs
xgettext
xmlwf
xz
xzcat
xzcmp
xzdec
xzdiff
xzegrep
xzfgrep
xzgrep
xzless
xzmore
yat2m
yes
zcat
zcmp
zdiff
zdump
zegrep
zfgrep
zforce
zgrep
zic
zless
zmore
znew
zprint
{
}

```

Semoga bermanfaat. Terima kasih.
