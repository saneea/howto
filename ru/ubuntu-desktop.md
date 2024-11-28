# Ubuntu Desktop

## Ярлыки запуска приложений

### Главное меню
Каждый ярлык реализуется как `*.desktop` файл расположенный в `/usr/share/applications`

Пример `*.desktop` файла
```properties
[Desktop Entry]
Name=Idea
GenericName=Idea
Keywords=code;coding;idea;jet;brains;
Exec=idea
Icon=/usr/bin/idea.svg
Terminal=false
Type=Application
PrefersNonDefaultGPU=true
X-KDE-RunOnDiscreteGpu=true
Categories=Development;IDE;
```
