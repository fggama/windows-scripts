# Utiles para obtener información en Windows
Scripts, ordenes, etc. Para administración por línea de comandos de s.o. Windows

## Borrar datos en los espacios no utilizados de disco en Windows 10
>``cipher /W:e:\``

## Variables de entorno
``CMD: echo %path%``

Accede al entorno  
``PS: Set-Location Env:``

Lista variables de entorno  
``PS Env:\> ls``  
``PS Env:\> Get-ChildItem``

Imprime el valor de _path_  
``$Env:path``

## Puertos USB de solo lectura
>- Windows Registry Editor Version 5.00
>- [HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\StorageDevicePolicies] "WriteProtect"=dword:00000000

## Route
``route -p add 10.10.100.0 mask 255.255.255.0 213.169.1.99 metric 10``  
``route -p add 10.10.90.0 mask 255.255.255.0 213.169.0.117 metric 30``

``[VPN-casa] route add 10.0.0.0 mask 255.255.0.0 10.8.0.245 IF 16``
``[VPN-casa] route add 213.169.0.0 mask 255.255.240.0  10.1.118.2 IF 82``

## Lista de Interfaces
``netsh int ipv4 show interfaces``
``Get-WMIObject Win32_NetworkAdapterConfiguration | Select-Object Caption, Description, InterfaceIndex, IPAddress | Format-List``

