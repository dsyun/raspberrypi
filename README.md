# raspberrypi magicmirror 

MMM-AssistantMk install error

/MMM-AssistantMk2 $ ./node_modules/.bin/electron-rebuild

An unhandled error occurred inside electron-rebuild
Unable to find electron-prebuilt's version number, either install it or specify an explicit version

Error: Unable to find electron-prebuilt's version number, either install it or specify an explicit version
    at Object.<anonymous> (/home/pi/MagicMirror/modules/MMM-AssistantMk2/node_modules/electron-rebuild/lib/src/cli.js:81:19)
    at Generator.next (<anonymous>)
    at /home/pi/MagicMirror/modules/MMM-AssistantMk2/node_modules/electron-rebuild/lib/src/cli.js:8:71
    at new Promise (<anonymous>)
    at __awaiter (/home/pi/MagicMirror/modules/MMM-AssistantMk2/node_modules/electron-rebuild/lib/src/cli.js:4:12)
    at /home/pi/MagicMirror/modules/MMM-AssistantMk2/node_modules/electron-rebuild/lib/src/cli.js:70:8
    at Object.<anonymous> (/home/pi/MagicMirror/modules/MMM-AssistantMk2/node_modules/electron-rebuild/lib/src/cli.js:146:4)
    at Module._compile (internal/modules/cjs/loader.js:689:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:700:10)
    at Module.load (internal/modules/cjs/loader.js:599:32)


solved


If then, try this.(For Raspbian Buster or GCC 8 user)

sudo apt-get install gcc-7 g++-7
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-7 10 --slave /usr/bin/g++ g++ /usr/bin/g++-7
sudo update-alternatives --config gcc

reinstall
