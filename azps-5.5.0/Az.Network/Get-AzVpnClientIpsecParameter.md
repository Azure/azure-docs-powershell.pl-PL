---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191915"
---
# Get-AzVpnClientIpsecParameter

## SYNOPSIS
Pobiera parametry Ipsec sieci VPN ustawione w wirtualnej bramie sieciowej dla połączeń Typuj z witryną.

## SKŁADNIA

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Wirtualna brama sieciowa to obiekt reprezentujący bramę na platformie Azure.
Polecenie **cmdlet Get-AzVpnClientIpsecParameters** zwraca obiekt parametrów ipsec połączenia vpn ustawiony na bramie na platformie Azure na podstawie nazwy bramy i nazwy grupy zasobów.

## PRZYKŁADY

### Przykład 1. Pobiera parametry ipsec połączenia vpn ustawione w wirtualnej bramie sieciowej dla połączeń typu Punkt z witryną.
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

Zwraca obiekt parametrów ipsec sieci vpn ustawionych w wirtualnej bramie sieciowej o nazwie "myGateway" w grupie zasobów "myRG".

## PARAMETERS

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

### — Nazwa
Nazwa zasobu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters

## NOTATKI

## LINKI POKREWNE

[New-AzVpnClientIpsecParameters](./New-AzVpnClientIpsecParameter.md)

[Remove-AzVpnClientIpsecParameters](./Remove-AzVpnClientIpsecParameter.md)

[Set-AzVpnClientIpsecParameters](./Set-AzVpnClientIpsecParameter.md)
