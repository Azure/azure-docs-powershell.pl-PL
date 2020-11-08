---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054591"
---
# Get-AzureRemoteAppVpnDeviceConfigScript

## STRESZCZENIe
Pobiera skrypt konfiguracji urządzenia sieci VPN funkcji Azure RemoteApp.

## POLECENIA

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRemoteAppVpnDeviceConfigScript** Pobiera skrypt konfiguracji urządzenia wirtualnej sieci prywatnej (VPN) usługi Azure RemoteApp.

## Przykłady

### Przykład 1: uzyskiwanie skryptu konfiguracji dla urządzenia sieci VPN
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

To polecenie zwraca skrypt lub plik konfiguracji służący do skonfigurowania urządzenia sieci wirtualnej o nazwie ContosoVNet.
Ten skrypt lub plik konfiguracyjny powinien zostać uruchomiony lub załadowany na urządzenie sieci VPN w typowy sposób dla tego urządzenia.
Zapoznaj się z dostawcą urządzenia VPN, aby uzyskać unikatowe wymagania dla każdego urządzenia.

## PARAMETRÓW

### -OSFamily
Określa rodzinę systemu operacyjnego (OS), która działa na platformie urządzenia.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Platform
Określa platformę urządzenia.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vendor
Określa dostawcę urządzenia sieci VPN.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VNetName
Określa nazwę sieci wirtualnej usługi Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRemoteAppVpnDevice](./Get-AzureRemoteAppVpnDevice.md)


