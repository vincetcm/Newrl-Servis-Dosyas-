**Açık tüm ekranları kapatın.**

```bash
pkill screen
```

**Servis dosyasını oluşturalım**

```bash
sudo tee $HOME/newrld.service > /dev/null <<EOF
[Unit]
Description=NEWRL Service
After=network.target
[Service]
Type=simple
WorkingDirectory=/root/newrl
ExecStart=/root/newrl/scripts/start.sh mainnet
Restart=always
RestartSec=5s
RemainAfterExit=no
LimitNOFILE=65535

[Install]
WantedBy=multi-user.target
EOF
```

**Servis dosyasını taşıyalım**

```bash
sudo mv $HOME/newrld.service /etc/systemd/system/
```

**Reload, aktifleştirme ve restart**
```bash
sudo systemctl daemon-reload

sudo systemctl enable newrld

sudo systemctl restart newrld
```

**Logları izlemk için bu komutu kullanın. CTRL+C ile kapatabilirsiniz.**
```bash
journalctl -u newrld -f -o cat
```

**Faydası olsuysa Güven skorunuzu esirgemeyin.**

0xc2f7f2337d821d39989c76ebfbda2cf78800bf88
