# WindowsVirtualize
Заметки по настройке виртуализации Windows

## Выключение виртуализации для VMWare Workstation

1. Деактивировать Hyper-V в настройках компонентов windows
2. С помощью cmd запустить команду: 
```
bcdedit /set hypervisorlaunchtype off
```
3. С помощью powershell деактивировать Hyper-V:
```
Disable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-All
```
## Включение виртуализации
1. В cmd запустить команду:
```
bcdedit /set hypervisorlaunchtype auto
```
2. С помощью powershell активировать Hyper-V:
```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-All
```

> [!IMPORTANT]
> Все команды следует выполнять от имени администратора.
