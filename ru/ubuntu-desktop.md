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

## Автозагрузка

### Способ через *.desktop файл

Каждое приложение в автозагрузке реализуется как `*.desktop` файл расположенный в `~/.config/autostart`

Пример `*.desktop` файла для Syncthing
```properties
[Desktop Entry]
Name=Start Syncthing
GenericName=File synchronization
Comment=Starts the main syncthing process in the background.
Exec=syncthing serve --no-browser --logfile=default
Icon=syncthing
Terminal=false
Type=Application
Keywords=synchronization;daemon;
Categories=Network;FileTransfer;P2P
```

Часто удобно не создавать новый `*.desktop` файл, а сделать софт-линк на существующий

```shell
ln -s /usr/share/applications/syncthing-start.desktop ~/.config/autostart/syncthing-start.desktop
```