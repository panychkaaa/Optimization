# I use

1) Активировать учетную запись администратора (Командная строка: net user administrator или Администратор /active:yes)

3) Отключить уведомления операционной системы
4) Таймер событий высокой точности - HPET (Командная строка: bcdedit /set useplatformtick Yes, bcdedit /set disabledynamictick yes, bcdedit /enum)
5) Timer Resolution (Нужное значение: 0.500 ms)
6) Interrupt Affinity Policy (Не обязательно)
7) MSI Mode
8) Отключить автоматическое обновление
9) Отключить брандмауэр (HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\mpssvc - Start = 4)
10) Отключить акселерацию мыши (HKEY_USERS\.DEFAULT\Control Panel\Mouse - MouseSpeed, MouseThreshold1,2 = 0)
11) Активировать "Максимальную производительность" (Командная строка: powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61)
12) Отключить фоновые приложения
13) Отключить визуальные эффекты
14) Отключить индексирование файлов
15) Отключить Superfetch (Служба: SysMain)
16) Отключить экономию энергии (Диспетчер устройств)
17) Отключить протокол "IPv6"
18) Отключить сервисы работающие в фоновом режиме (Google Chrome)
19) Отключить аппаратное ускорение (Google Chrome)
20) Изменить "DNS" (Cloudflare: 1.1.1.1 и 1.0.0.1)
21) Отключить "Исправление масштабирования для приложений"
22) Выбрать режим управления электропитанием "Предпочтителен режим максимальной производительности" (Панель управления nvidia: dwm.exe, explorer.exe)
23) Активировать "Игровой режим" и "Планирование графического процессора с аппаратным ускорением"
24) Электропитание (USB 3 Link Power Mangement - Off, Минимальное число ядер в состоянии простоя - 100%, Разрешить состояние снижения питания - Авто, 
Пороговое значение повышения состояния простоя процессора - 100%, Пороговое значение понижения состояния простоя процессора - 100%, Минимальное состояние процессора - 100%, 
Максимальное состояние процессора - 100%)

- MSI Afterburner
- AIDA64
- CPU-Z
- CrystalDiskInfo
- DDU
- GPU-Z
- HWiNFO
- Interrupt Affinity Policy
- LatencyMon
- MSI Mode
- NVCleanstall
- Nvidia inspector
- PowerSettingsExplorer
- Process Explorer
- SDIO
- TimerResolution
- TCPOptimizer
- Win 10 Tweaker
- WinCry
