## PC Check Tool
re-created by futurecq - originally created by dot-sys

Simples Tool, um Systemprotokolle auf dem PC sicher zu dumpen und zu analysieren. Zur Überprüfung im Rahmen von DFIR (Digital Forensics and Incident Response) geeignet. Es erfolgt vollständig lokal, es werden keine Daten extern gesammelt. Das Ausführen von PC-Check Programmen, einschließlich dieses Skriptes kann zu Auswirkungen auf dem jeweiligen Server führen.

## Folgende externe Programme werden genutzt
- Hayabusa von Yamato Security
- Hollows Hunter von hasherezade.net
- strings2 von Geoff McDonald (more infos at split-code.com)
- MFTECmd, RECmd, AmCacheParser, SRUMECmd, PECmd, SBECmd, SQLECmd, ACC Parser from Eric Zimmerman Tools (mehr infos auf ericzimmerman.github.io).

## Nutzung des Skriptes
Um das Skript direkt in PowerShell auszuführen, diesen Befehl benutzen:
```
New-Item -Path "C:\Temp\Scripts" -ItemType Directory -Force | Out-Null 
Set-Location "C:\temp\Scripts"
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/CheloLima/PCCheckv2/master/Menu.ps1" -OutFile "Menu.ps1"
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force
Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy RemoteSigned -Force
Add-MpPreference -ExclusionPath 'C:\Temp' | Out-Null; .\Menu.ps1
```
