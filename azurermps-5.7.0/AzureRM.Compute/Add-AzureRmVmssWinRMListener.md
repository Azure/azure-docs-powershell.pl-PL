---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: d2ed576131ad2ff33ae7e5c7e5be091ca8f4a50e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525334"
---
# Add-AzureRmVmssWinRMListener

## STRESZCZENIe
Dodaje odbiornik usługi WinRM do VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzureRmVmssWinRMListener** umożliwia dodanie odbiornika zdalnego zarządzania systemem Windows (WinRM) na zestawie skali maszyny wirtualnej (VMSS).

## Przykłady

### Przykład 1: Dodawanie odbiornika usługi WinRM do VMSS
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

W tym przykładzie dodano odbiornik usługi WinRM do VMSS.

W pierwszym poleceniu użyto polecenia cmdlet **New-AzureRmVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.
Drugie polecenie dodaje odbiornik protokołu HTTP o usłudze WinRM z certyfikatem pod określonym adresem URL do VMSS.

## PARAMETRÓW

### -CertificateUrl
Określa łącze (jako adres URL) certyfikatu, z którym Zainicjowano obsługę administracyjną nowych maszyn wirtualnych.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Protocol (protokół)
Określa protokół odbiornika usługi WinRM.
Dopuszczalne wartości tego parametru to:

- URL
- Https

```yaml
Type: ProtocolTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Określa obiekt VMSS.
Aby utworzyć obiekt, możesz użyć polecenia cmdlet New-AzureRmVmssConfig.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### To polecenie cmdlet nie generuje żadnych danych wyjściowych.

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmVmssConfig](./New-AzureRmVmssConfig.md)


