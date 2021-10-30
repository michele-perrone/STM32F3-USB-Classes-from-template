# STM32F3 USB Classes from template
The goal of this project is to provide a decent collection of guidelines for creating working USB classes to be used by STM32F3 MCUs by starting from the clean template provided by ST. The template can be retrieved by downloading the firmware package. Another goal is to demonstrate the process with the creation of a USB MIDI Class which should work out of the box.   
## USB CDC Class
Strategy:   
1. Create a clean STM32F3 Discovery project with STM32CubeIDE, peripherals initialized to default mode. The important thing is to have the user USB port enabled (USB FS), but not USB Device class selected (commit [96b7e58118a8e7295219f0b2bf272d08bb8437e1](https://github.com/michele-perrone/STM32F3-USB_CDC-from-template/commit/96b7e58118a8e7295219f0b2bf272d08bb8437e1))
2. Add to the project the clear USB Class template, provided by ST in the firmware folder. Put the files in the exact same place where CubeIDE places them. Rename them to match the filenames of the CDC class (commit [e3b3add08c9947f8ff604fccf922febdf672e7c4](https://github.com/michele-perrone/STM32F3-USB_CDC-from-template/commit/e3b3add08c9947f8ff604fccf922febdf672e7c4))
3. Delete the aforementioned templated code and make CubeIDE generate the working CDC class code. This is done by selecting the CDC class in the CubeIDE configurator (commit [70374633c031386eb78ffd36fd4ad3dee94dfb97](https://github.com/michele-perrone/STM32F3-USB_CDC-from-template/commit/70374633c031386eb78ffd36fd4ad3dee94dfb97))
4. Analyze the diff between commits in points **2.** and **3.**, so we can clearly figure out what is needed to create a working CDC class from the template code. Since we have previously placed the template code into the same directories and with the same filenames and CubeIDE does, we "trick" git into considering these files as modified and not replaced.
## USB AUDIO Class
Same stratagy:
1. Commit [d5e741e2c77f207465bfbee9861499ae8c9ccd14](https://github.com/michele-perrone/STM32F3-USB-Classes-from-template/commit/d5e741e2c77f207465bfbee9861499ae8c9ccd14)
2. Commit [589b691e77170278b5587a6955627acf53d6f8ff](https://github.com/michele-perrone/STM32F3-USB-Classes-from-template/commit/589b691e77170278b5587a6955627acf53d6f8ff)
3. Commit [e34a95fb31b90af3d64fc89eb66eb54f5af5e685](https://github.com/michele-perrone/STM32F3-USB-Classes-from-template/commit/e34a95fb31b90af3d64fc89eb66eb54f5af5e685)
## USB MIDI Class
Once it's perfectly clear what exactly is needed to write USB classes that work, I can start writing the USB MIDI class.
