---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 70899AAC-BF64-4FFA-9DAF-92E859D0B271
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3b30172f947c1c8bf39a8be84039d9166d6ea290
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055380"
---
# Set-AzureVNetGateway

## STRESZCZENIe
Włącza lub wyłącza bramę sieci VPN dla sieci wirtualnej usługi Azure.

## POLECENIA

### Connect (domyślnie)
```
Set-AzureVNetGateway [-Connect] -VNetName <String> -LocalNetworkSiteName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Zamyka
```
Set-AzureVNetGateway [-Disconnect] -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureVNetGateway** włącza lub wyłącza bramę wirtualnej sieci prywatnej (VPN) dla sieci wirtualnej usługi Azure.
Brama sieci wirtualnej to punkt końcowy sieci VPN umożliwiający połączenie z siecią wirtualną.
Określ parametr *Connect* lub *Disconnect* , aby włączyć lub wyłączyć połączenie VPN między lokalną lokacją sieci lokalnej a siecią wirtualną.

## Przykłady

### Przykład 1: Włączanie bramy sieci wirtualnej dla sieci wirtualnej
```
PS C:\> Set-AzureVNetGateway -Connect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

To polecenie włącza bramę sieci wirtualnej między wirtualną siecią Azure o nazwie ContosoProdNet a urządzeniem sieci VPN dla lokalnej lokacji sieciowej o nazwie ContosoBranchOffice.

### Przykład 2: wyłączenie bramy sieci wirtualnej dla sieci wirtualnej
```
PS C:\> Set-AzureVNetGateway -Disconnect -VnetName "ContosoProdNet" -LocalNetworkSiteName "ContosoBranchOffice"
```

To polecenie wyłącza bramę sieci wirtualnej między wirtualną siecią Azure o nazwie ContosoProdNet a urządzeniem sieci VPN dla lokalnej lokacji sieciowej o nazwie ContosoBranchOffice.

## PARAMETRÓW

### -Connect
Wskazuje, że to polecenie cmdlet włącza połączenie VPN między siecią wirtualną a lokacją sieci lokalnej.

```yaml
Type: SwitchParameter
Parameter Sets: Connect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disconnect
Wskazuje, że to polecenie cmdlet wyłącza połączenie VPN między siecią wirtualną a lokacją sieci lokalnej.

```yaml
Type: SwitchParameter
Parameter Sets: Disconnect
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalNetworkSiteName
Określa nazwę lokalnej lokacji sieciowej, dla której to polecenie cmdlet włączy lub wyłącza połączenie VPN.

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
Określa sieć wirtualną, w której to polecenie cmdlet włącza lub wyłącza połączenie VPN.

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

[Remove-AzureVNetGateway](./Remove-AzureVNetGateway.md)

[Resetowanie — AzureVNetGateway](./Reset-AzureVNetGateway.md)

[Zmienianie rozmiaru — AzureVNetGateway](./Resize-AzureVNetGateway.md)


