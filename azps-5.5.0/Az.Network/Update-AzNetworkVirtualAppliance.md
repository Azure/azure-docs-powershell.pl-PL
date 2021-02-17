---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 3522e5d41cf110dcf7e9715b5483f61e2199a9a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191538"
---
# Update-AzNetworkVirtualAppliance

## SYNOPSIS
Aktualizowanie lub zmienianie zasobu urządzenia wirtualnego sieci.

## SKŁADNIA

```
Update-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String>
 [-Sku <PSVirtualApplianceSkuProperties>] [-VirtualApplianceAsn <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Ta Update-AzNetworkVirtualAppliance zmodyfikuje zasób wirtualnego urządzenia sieciowego.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Update-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -VirtualApplianceAsn 1234
```

Zmodyfikuj numer ASN urządzenia wirtualnego.

### Przykład 2

Aktualizowanie lub zmienianie zasobu urządzenia wirtualnego sieci. (wygenerowane automatycznie)

<!-- Aladdin Generated Example -->
```powershell
Update-AzNetworkVirtualAppliance -Name nva -ResourceGroupName testrg -Sku <PSVirtualApplianceSkuProperties>
```

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

### — Wymuszanie
Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób

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

### — Nazwa
Nazwa zasobu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
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

### - SKU
SKU urządzenia wirtualnego.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Tag
Tabela skrótów reprezentująca tagi zasobów.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualApplianceAsn
Numer ASN urządzenia wirtualnego.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties

### System.Int32

### System.Collections.Hashtable

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance

## NOTATKI

## LINKI POKREWNE
