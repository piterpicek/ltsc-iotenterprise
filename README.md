# Activate Windows 10/11 Enterprise LTSC and LTSC IoT

Supported Versions:

- Windows 11 Enterprise LTSC IoT
- Windows 10 Enterprise LTSC

## 1. Copy Required Files

Extract and Copy these folders to the Destination Path:

```
C:\Windows\System32\spp\tokens\skus
```

Folder:

- csvlk-pack
- EnterpriseS
- IoTEnterpriseS

## 2. Open CMD by Run As Admin

```cmd
- For Scan new License added :
cscript.exe %windir%\system32\slmgr.vbs /rilc
cscript.exe %windir%\system32\slmgr.vbs /upk >nul 2>&1
cscript.exe %windir%\system32\slmgr.vbs /ckms >nul 2>&1
cscript.exe %windir%\system32\slmgr.vbs /cpky >nul 2>&1

- For Windows 10 :
cscript.exe %windir%\system32\slmgr.vbs /ipk M7XTQ-FN8P6-TTKYV-9D4CC-J462D

- For Windows 11 :
cscript.exe %windir%\system32\slmgr.vbs /ipk KBN8V-HFGQ4-MGXVD-347P6-PDQGT

- For Reconfigure LicenseManager
sc config LicenseManager start= auto & net start LicenseManager
sc config wuauserv start= auto & net start wuauserv

- To fix Activation change KMS Server
cscript.exe %windir%\system32\slmgr.vbs /skms kms.digiboy.ir
cscript.exe %windir%\system32\slmgr.vbs /ato
```

Notes:

- /skms parameter sets the Key Management Service (KMS) server.

- If kms.digiboy.ir doesn’t work, try one of these alternatives:

```
kms9.msguides.com
54.223.212.31
kms.cnlic.com
kms.chinancce.com
kms.ddns.net
franklv.ddns.net
k.zpale.com
m.zpale.com
mvg.zpale.com
kms.shuax.com
kensol263.imwork.net:1688
kms.loli.best
kms.vudy.net
```


# Bonus Get Back Microsoft Store 

```
LTSC-Add-MicrosoftStore -> click "Add-Store.cmd" (with Run as)
```

# 