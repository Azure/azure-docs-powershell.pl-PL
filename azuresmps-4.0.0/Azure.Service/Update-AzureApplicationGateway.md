---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054810"
---
# Update-AzureApplicationGateway

## STRESZCZENIe
Umożliwia zaktualizowanie bramy aplikacji.

## POLECENIA

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Update-AzureApplicationGateway** umożliwia zaktualizowanie istniejącej bramy aplikacji.

## Przykłady

### Przykład 1: modyfikowanie bramy aplikacji przy użyciu jej nazwy
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

Pierwsze polecenie zatrzymuje bramkę Application Gateway o nazwie ApplicationGateway06.
Aby można było zmodyfikować sieć wirtualną lub podsieci, Brama aplikacji musi zostać zatrzymana.

Drugie polecenie modyfikuje podsieć wirtualną i podsieci dla bramy Application Gateway o nazwie ApplicationGateway06.

### Przykład 2: modyfikowanie dodatkowych właściwości bramy aplikacji
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

To polecenie modyfikuje liczbę wystąpień, rozmiar bramy i opis bramy Application Gateway o nazwie ApplicationGateway06.
To polecenie nie powoduje zmiany sieci wirtualnej ani podsieci dla bramy aplikacji.
Dlatego nie trzeba zatrzymywać bramy aplikacji przed uruchomieniem tego polecenia.

### Przykład 3: modyfikowanie bramy aplikacji za pomocą potoku
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway06 przy użyciu polecenia cmdlet **Get-AzureApplicationGateway** .
Polecenie zapisuje je w zmiennej $ApplicationGateway.

Drugie polecenie przypisuje Właściwość **GatewaySize** wartość średnia.

Polecenie ostatnie przekazuje zaktualizowaną $ApplicationGateway do bieżącego polecenia cmdlet.

## PARAMETRÓW

### — Opis
Określa opis, który ten polecenie cmdlet przypisuje bramie aplikacji.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GatewaySize
Określa rozmiar, który ten polecenie cmdlet przypisuje bramie aplikacji.
Prawidłowe wartości:

- Mała
- Pożywkę
- Większej

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceCount
Określa liczbę wystąpień, które to polecenie cmdlet przypisuje bramie aplikacji.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę bramy aplikacji, która jest aktualizowana przez to polecenie cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Podsieci
Określa tablicę podsieci, w których to polecenie cmdlet wdraża bramę aplikacji.

Nie można aktualizować podsieci, gdy Brama aplikacji jest uruchomiona.
Aby zatrzymać bramę Application Gateway, użyj polecenia cmdlet Stop-AzureApplicationGateway.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VnetName
Określa sieć wirtualną, w której to polecenie cmdlet wdraża bramę aplikacji.

Nie można zaktualizować sieci wirtualnej, gdy Brama Application Gateway jest uruchomiona.
Aby zatrzymać bramę Application Gateway, użyj pola **stop-AzureApplicationGateway**.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. platformy windowsazure. Management. ApplicationGateway. MODELES. ApplicationGatewayOperationResponse

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[Nowe — AzureApplicationGateway](./New-AzureApplicationGateway.md)

[Remove-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[Start — AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Zatrzymaj — AzureApplicationGateway](./Stop-AzureApplicationGateway.md)
