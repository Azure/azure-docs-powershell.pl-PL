---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054456"
---
# Remove-AzureVNetGateway

## STRESZCZENIe
Usuwa bramę VPN.

## POLECENIA

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureVNetGateway** Usuwa istniejącą bramę wirtualnej sieci prywatnej (VPN) dla sieci wirtualnej.

## Przykłady

### Przykład 1: usunięcie bramy sieci wirtualnej
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

To polecenie powoduje usunięcie bramy sieci wirtualnej z sieci wirtualnej o nazwie ContosoVN07.

## PARAMETRÓW

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet. Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

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

### -VNetName
Określa sieć wirtualną, w której to polecenie cmdlet usuwa bramę VPN.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureVNetGateway](./Get-AzureVNetGateway.md)

[Nowe — AzureVNetGateway](./New-AzureVNetGateway.md)

[Resetowanie — AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Zmienianie rozmiaru — AzureVNetGateway](./Resize-AzureVNetGateway.md)

[Set-AzureVNetGatewayKey](./Set-AzureVNetGatewayKey.md)


