---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052053"
---
# Set-AzPublicIpAddress

## STRESZCZENIe
Aktualizuje publiczny adres IP.

## POLECENIA

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzPublicIpAddress** aktualizuje publiczny adres IP.

## Przykłady

### 1: Zmienianie metody przydzielania publicznego adresu IP
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Pierwsze polecenie pobiera zasób publiczny adres IP z nazwą $publicIPName w grupie zasób $rgName.
Drugie polecenie ustawia metodę przydziału obiektu publicznego adresu IP na wartość "static".
Polecenie Set-AzPublicIPAddress powoduje zaktualizowanie zasobu publicznego adresu IP za pomocą zaktualizowanego obiektu i zmodyfikowanie metody alokacji na wartość "static". Publiczny adres IP przydzielono natychmiast.

### 2: Dodawanie etykiety domeny DNS dla publicznego adresu IP
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Pierwsze polecenie pobiera zasób publiczny adres IP z nazwą $publicIPName w grupie zasób $rgName.
Drugie polecenie ustawia właściwość DomainNameLabel na wymagany prefiks DNS.
Polecenie Set-AzPublicIPAddress aktualizuje zasób publiczny adres IP za pomocą zaktualizowanego obiektu. DomainNameLabel & FQDN są modyfikowane zgodnie z oczekiwaniami.
    
### 3: Zmienianie etykiety domeny DNS dla publicznego adresu IP
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Pierwsze polecenie pobiera zasób publiczny adres IP z nazwą $publicIPName w grupie zasób $rgName.
Drugie polecenie ustawia właściwość DomainNameLabel na wymagany prefiks DNS.
Polecenie Set-AzPublicIPAddress aktualizuje zasób publiczny adres IP za pomocą zaktualizowanego obiektu. DomainNameLabel & FQDN są modyfikowane zgodnie z oczekiwaniami.

## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
Określa publiczny obiekt adresu IP reprezentujący stan, w którym powinien być ustawiony publiczny adres IP.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Network. models. PSPublicIpAddress

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSPublicIpAddress

## INFORMACYJN

## LINKI POKREWNE

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[Nowe — AzPublicIpAddress](./New-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)


