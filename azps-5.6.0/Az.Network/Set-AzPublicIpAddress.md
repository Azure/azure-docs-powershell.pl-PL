---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 33712b9813d6c23ed72097597d94a22bf7644992
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990949"
---
# Set-AzPublicIpAddress

## SYNOPSIS
Aktualizuje publiczny adres IP.

## SKŁADNIA

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzPublicIpAddress** aktualizuje publiczny adres IP.

## PRZYKŁADY

### 1. Zmienianie metody alokacji publicznego adresu IP
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Pierwsze polecenie pobiera publiczny zasób adresu IP z $publicIPName nazwami w grupie zasobów $rgName.
Drugie polecenie ustawia metodę alokacji publicznego obiektu adresu IP na "Statyczny".
Set-AzPublicIPAddress aktualizuje zasób publicznego adresu IP zaktualizowanym obiektem i modyfikuje metodę alokacji na "Statyczną". Publiczny adres IP jest przydzielany natychmiast.

### 2. Dodawanie etykiety domeny DNS publicznego adresu IP
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Pierwsze polecenie pobiera publiczny zasób adresu IP z $publicIPName nazwami w grupie zasobów $rgName.
Drugie polecenie ustawia właściwość DomainNameLabel na wymagany prefiks dns.
Set-AzPublicIPAddress aktualizuje zasób publicznego adresu IP zaktualizowanym obiektem. Nazwa_domeny & Fqdn są modyfikowane zgodnie z oczekiwaniami.
    
### 3. Zmienianie etykiety domeny DNS publicznego adresu IP
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Pierwsze polecenie pobiera publiczny zasób adresu IP z $publicIPName nazwami w grupie zasobów $rgName.
Drugie polecenie ustawia właściwość DomainNameLabel na wymagany prefiks dns.
Set-AzPublicIPAddress aktualizuje zasób publicznego adresu IP zaktualizowanym obiektem. Nazwa_domeny & Fqdn są modyfikowane zgodnie z oczekiwaniami.

## PARAMETERS

### — AsJob
Uruchamianie polecenia cmdlet w tle

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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
Określa publiczny obiekt adresu IP reprezentujący stan, dla którego należy ustawić publiczny adres IP.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## NOTATKI

## LINKI POKREWNE

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[New-AzPublicIpAddress](./New-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)


