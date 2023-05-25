# Погнале

- Активировать учетную запись администратора (Командная строка: net user administrator или Администратор /active:yes)
- Отключить уведомления операционной системы
- Таймер событий высокой точности - HPET (Командная строка: bcdedit /set useplatformtick Yes, bcdedit /set disabledynamictick yes, bcdedit /enum)
- Timer Resolution (Нужное значение: 0.500 ms)
- Interrupt Affinity Policy (Видеокарта и хост контроллер: по разным ядрам)
- MSI Mode
- Отключить автоматическое обновление
- Отключить брандмауэр (HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\mpssvc - Start = 4)
- Отключить акселерацию мыши (HKEY_USERS\.DEFAULT\Control Panel\Mouse - MouseSpeed, MouseThreshold1,2 = 0)
- Активировать "Максимальную производительность" (Командная строка: powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61)
- Отключить фоновые приложения
- Отключить визуальные эффекты
- Отключить индексирование файлов
- Отключить Superfetch (Служба: SysMain)
- Отключить экономию энергии (Диспетчер устройств)
- Отключить протокол "IPv6"
- Отключить сервисы работающие в фоновом режиме (Google Chrome)
- Отключить аппаратное ускорение (Google Chrome)
- Изменить "DNS" (Cloudflare: 1.1.1.1 и 1.0.0.1)
- Отключить "Исправление масштабирования для приложений"
- Выбрать режим управления электропитанием "Предпочтителен режим максимальной производительности" (Панель управления nvidia: dwm.exe, explorer.exe)
- Отключить "Игровой режим" и "Планирование графического процессора с аппаратным ускорением"
- Электропитание (USB 3 Link Power Mangement - Off, Минимальное число ядер в состоянии простоя - 100%, Разрешить состояние снижения питания - Авто, 
Пороговое значение повышения состояния простоя процессора - 100%, Пороговое значение понижения состояния простоя процессора - 100%, Минимальное состояние процессора - 100%, 
Максимальное состояние процессора - 100%)

# Полезные программы

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
