---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054766"
---
# Set-AzureNetworkSecurityRule

## STRESZCZENIe
Dodaje lub modyfikuje regułę zabezpieczeń sieci w grupie zabezpieczeń sieci.

## POLECENIA

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureNetworkSecurityRule** umożliwia dodanie lub zmodyfikowanie reguły zabezpieczeń sieci Azure w grupie zabezpieczeń sieci.

## Przykłady

## PARAMETRÓW

### -Action
Określa akcję dla reguły zabezpieczeń sieci.
Prawidłowe wartości to: Allow i Deny.

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

### -DestinationAddressPrefix
Określa adres IP Classless subdomain Routing (CIDR) dla docelowego zakresu adresów IP dla reguły zabezpieczeń sieci.
Gwiazdka (*) określa dowolny adres IP.

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

### -DestinationPortRange
Określa zakres portów docelowych dla reguły zabezpieczeń sieci.
Prawidłowe wartości zawierają liczby całkowite z zakresu od 0 do 65535.
Możesz określić pojedynczą wartość lub określić zakres w formacie LowerNumber-HigherNumber.
Łącznik oddziela dwie wartości.

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

### -Name (nazwa)
Określa nazwę reguły zabezpieczeń sieci, którą to polecenie cmdlet dodaje lub modyfikuje.

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

### -NetworkSecurityGroup
Określa grupę zabezpieczeń sieci, którą to polecenie cmdlet modyfikuje.
Aby uzyskać obiekt **INetworkSecurityGroup** , użyj polecenia cmdlet Get-AzureNetworkSecurityGroup.

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Priority (priorytet)
Określa priorytet reguły zabezpieczeń sieci.
Prawidłowe wartości to: liczba całkowita z zakresu od 100 do 4096.

```yaml
Type: Int32
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

### -Protocol (protokół)
Określa protokół dla reguły zabezpieczeń sieci.
Prawidłowe wartości: 

- PROTOKOŁ 
- OBSŁUGIWANE 
- *

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

### -SourceAddressPrefix
Określa adres CIDR źródłowego zakresu adresów IP dla reguły zabezpieczeń sieci.
Gwiazdka (*) określa dowolny adres IP.

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

### -SourcePortRange
Określa zakres portów źródłowych dla reguły zabezpieczeń sieci.
Prawidłowe wartości zawierają liczby całkowite z zakresu od 0 do 65535.
Możesz określić pojedynczą wartość lub określić zakres w formacie LowerNumber-HigherNumber.
Łącznik oddziela dwie wartości.

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

### -Type
Określa typ połączenia dla reguły zabezpieczeń sieci.
Prawidłowe wartości to: przychodzące i wychodzące.

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

[Remove-AzureNetworkSecurityRule](./Remove-AzureNetworkSecurityRule.md)


