# STM32F3 USB CDC from template
Create a working USB CDC class starting from the clear template provided by ST.   
Strategy:   
1. Create a clean STM32F3 Discovery project with STM32CubeIDE, peripherals initialized to default mode. USB FS in enabled by default (commit [96b7e58118a8e7295219f0b2bf272d08bb8437e1](https://github.com/michele-perrone/STM32F3-USB_CDC-from-template/commit/96b7e58118a8e7295219f0b2bf272d08bb8437e1))
2. Add to the project the clear USB Class template, provided by ST in the firmware folder. Put the files in the exact same place where CubeIDE places them. Rename them to match the filenames of the CDC class (commit [e3b3add08c9947f8ff604fccf922febdf672e7c4](https://github.com/michele-perrone/STM32F3-USB_CDC-from-template/commit/e3b3add08c9947f8ff604fccf922febdf672e7c4))
3. Delete the aforementioned templated code and make CubeIDE generate the working CDC class code. This is done by selecting the CDC class in the CubeIDE configurator (commit [70374633c031386eb78ffd36fd4ad3dee94dfb97](https://github.com/michele-perrone/STM32F3-USB_CDC-from-template/commit/70374633c031386eb78ffd36fd4ad3dee94dfb97)
4. Analyze the diff between commits in points **2.** and **3.**, so we can clearly figure out what is needed to create a working CDC class from the template code.
