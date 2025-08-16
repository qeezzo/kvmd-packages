```bash
gpg --full-generate-key
# Please select what kind of key you want:
#    (1) RSA and RSA (default)
# What keysize do you want? 4096
# Please specify how long the key should be valid.
#          0 = key does not expire
# Key does not expire at all
# Is this correct? (y/N) y
# Then enter Name, Email, Passphrase

gpg --list-keys
gpg --armor --export YOUR_KEY > buildenv/public.key
```

```bash
rm repos/rpi4/latest/kvmd
make build
scp repos/rpi4/kvmd-3.291-1-any.pkg.tar.xz spyder@raspberrypi:/home/spyder
```