- Активировать учетную запись администратора (Командная строка: net user administrator или Администратор /active:yes)
- Отключить уведомления операционной системы
- Таймер событий высокой точности - HPET (Командная строка: bcdedit /set useplatformtick Yes, bcdedit /set disabledynamictick yes, bcdedit /enum)
- MSI Mode
- Отключить автоматическое обновление
- Отключить брандмауэр (HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\mpssvc - Start = 4)
- Отключить акселерацию мыши (HKEY_USERS\.DEFAULT\Control Panel\Mouse - MouseSpeed, MouseThreshold1,2 = 0)
- Активировать "Максимальную производительность" (Командная строка: powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61)
- Отключить фоновые приложения: Настройки
- Отключить визуальные эффекты
- Отключить индексирование файлов
- Отключить Superfetch (Служба: SysMain)
- Отключить экономию энергии: Get-WmiObject MSPower_DeviceEnable -Namespace root\wmi | ForEach-Object { $_.enable = $false; $_.psbase.put(); }
- Отключить протокол "IPv6"
- Отключить сервисы работающие в фоновом режиме (Google Chrome)
- Отключить аппаратное ускорение (Google Chrome)
- Изменить "DNS" (Cloudflare: 1.1.1.1 и 1.0.0.1)
- Отключить "Исправление масштабирования для приложений"
- Выбрать режим управления электропитанием "Предпочтителен режим максимальной производительности" (Панель управления nvidia: dwm.exe, explorer.exe)
- Электропитание (USB 3 Link Power Mangement - Off, Минимальное состояние процессора - 100%, Максимальное состояние процессора - 100%)
- Юзеры: netplwiz
- bcdedit /set disabledynamictick yes
- bcdedit /set useplatformclock false
- tpm.msc
-taskschd.msc
- gpedit.msc
- msinfo32
- netsh interface ipv4 show subinterfaces
- netsh interface ipv4 set subinterface Ethernet mtu=1492 store=persistent
- PowerShell Disable-NetAdapterPowerManagement -Name "*"
- PowerShell Set-NetOffloadGlobalSetting -PacketCoalescingFilter Disabled
](https://msdl.gravesoft.dev/

- Изменить: HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control -> SvcHostSplitThresholdInKB
- Планировщик задач (убрать лишнее): Application Experience, Autochk, Customer Experience Improvement Program, DiskDiagnostic, Maintenance, Windows Defender
- Удалить все лишние приложения Windows
- Выключить: powercfg /h off
- Выключить: SearchHost.exe
- Удалить: Get-AppxPackage Microsoft.XboxGamingOverlay | Remove-AppxPackage
- Выключить через MSI Mode: RemappingSupported
- Выключить через MSI Mode (USB): D3ColdSupported
- MSI-X (IrqPolicySpreadMessagesAcrossAllProcessors) прерывания - 2048
- Win32PrioritySeparationTool - 42
- Планирование графического процессора с аппаратным ускорением - Выкл.
- Игровой режим - Вкл. (Ryzen!!!)
- В окне без рамки (Directx 12)
- Изменить настройки контроля учетных записей
- Отключить стиль указателя мыши
- Отключить службы в безопастном режиме (WinDefend mpsdrv WdBoot WdFilter MpsSvc MDCoreSvc wscsvc webthreatdefusersvc BDESVC)
- Удалить службы sc delete (dmwappushservice DiagTrack UdkUserSvc)
- Активировать учетную запись администратора (Командная строка: net user administrator или Администратор /active:yes)
- Отключить уведомления операционной системы
- Отключить фоновые приложения
- Отключить визуальные эффекты
- Отключить индексирование файлов
- Отключить "Исправление масштабирования для приложений"
- Выбрать режим управления электропитанием "Предпочтителен режим максимальной производительности" (Панель управления nvidia: dwm.exe, explorer.exe)
- Электропитание (USB 3 Link Power Mangement - Off)
- Отключить экономию энергии USB(Диспетчер задач)

gpedit.msc: DWM, Smart screen, Синхронизация
gpedit.msc: Конфигурация компьютера > Административные шаблоны > Компоненты Windows > Сборки для сбора данных и предварительные сборки > Разрешить телеметрию
gpedit.msc: Конфигурация компьютера > Система > Управление питанием > Регулирование мощности
gpedit.msc: Конфигурация компьютера > Административные шаблоны > Компоненты Windows > Конфиденциальность приложения > Фоновые приложения выключить

-> PowerShell: Get-WmiObject MSPower_DeviceEnable -Namespace root\wmi | ForEach-Object { $_.enable = $false; $_.psbase.put(); }

Cloudflare DNS: 1.1.1.1 , 1.0.0.1

PowerShell Disable-NetAdapterPowerManagement -Name "*"
PowerShell Set-NetOffloadGlobalSetting -PacketCoalescingFilter Disabled

Проверка: Get-NetOffloadGlobalSetting
Проверка (LAN): netsh interface tcp show global

netsh interface ipv4 show subinterfaces
netsh interface ipv4 set subinterface Ethernet mtu=1492 store=persistent

tpm.msc
taskschd.msc
gpedit.msc
netplwiz
msinfo32

shell:startup

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsRuntime\ActivatableClassId\Windows.Gaming.GameBar.PresenceServer.Internal.PresenceWriter

bcdedit /set nx AlwaysOff
bcdedit /set bootmenupolicy legacy
bcdedit /set hypervisorlaunchtype off
bcdedit /set useplatformtick yes
bcdedit /set disabledynamictick yes
bcdedit /set useplatformclock false
bcdedit /set tscsyncpolicy enhanced legacy

HKEY_CURRENT_USER\SOFTWARE\Microsoft\GameBar - gamemode
HKEY_CURRENT_USER\System\GameConfigStore\Children\
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\AppCompatFlags\Layers

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System -> EnableLinkedConnections - 1 (Видимость сетевых папок)

HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Class\{4d36e968-e325-11ce-bfc1-08002be10318}\0000
"DisableDynamicPstate"=dword:00000001

powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61

powercfg /L
powercfg -delete
powercfg -import "The full path to your .pow file"

Где хранятся обновления Windows: %windir%\SoftwareDistribution\Download)
