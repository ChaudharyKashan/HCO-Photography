# HCO Photo Hide

A small local web app for password-protected image sharing. Images and generated codes are stored locally in `data.json` on the device running the app.

> Use only with images and devices you own or are authorized to manage.

## Termux installation

```bash
pkg update -y
pkg install python git -y

git clone https://github.com/ChaudharyKashan/HCO-Photography.git
cd HCO-Photography
python -m pip install -r requirements.txt
python HCO-Photo-Hide.py
```

The app will normally open the browser automatically. If it does not, open `http://127.0.0.1:8000` manually. Press `Ctrl+C` in Termux to stop the server.

### One-command start after installation

```bash
chmod +x start.sh
./start.sh
```

## LAN sharing

The terminal prints a network URL such as `http://192.168.1.10:8000`. Devices on the same Wi-Fi network can open that URL while the Termux server is running. Do not expose this server to the public internet without proper authentication and HTTPS.

## Change the port

```bash
HCO_PORT=8080 python HCO-Photo-Hide.py
```

## Linux

```bash
sudo apt update
sudo apt install -y python3 python3-pip git
git clone https://github.com/ChaudharyKashan/HCO-Photography.git
cd HCO-Photography
python3 -m pip install -r requirements.txt
python3 HCO-Photo-Hide.py
```

## Files

- `HCO-Photo-Hide.py` — local HTTP server and web interface
- `requirements.txt` — Python dependency list
- `start.sh` — Termux/Linux convenience launcher
- `data.json` — created automatically when the first image is saved

## License

See [Licence](Licence).
