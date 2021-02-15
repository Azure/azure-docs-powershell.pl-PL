---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237939"
---
# Get-AzDnsZone

## SYNOPSIS
Pobiera strefę DNS.

## SKŁADNIA

### Domyślne (domyślne)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroup
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzDnsZone** pobiera strefę systemu nazw domen (DNS) z określonej grupy zasobów.
W przypadku określenia *parametru Name* zwracany jest jeden obiekt **DnsZone.**
Jeśli parametr Name  nie zostanie określony, zostanie zwrócona tablica zawierająca wszystkie strefy w określonej grupie zasobów.
Za pomocą obiektu **DnsZone** można zaktualizować strefę, na przykład można dodać do niego obiekty **RecordSet.**

## PRZYKŁADY

### Przykład 1. Uzyskiwanie strefy
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Ten przykład pobiera strefę DNS o nazwie myzone.com z określonej grupy zasobów, a następnie zapisuje ją w $Zone danych.

### Przykład 2. Uzyskiwanie wszystkich stref w grupie zasobów
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

W tym przykładzie wszystkie strefy DNS w określonej grupie zasobów są przechowywane w $Zones danych.

### Przykład 3. Uzyskiwanie wszystkich stref w subskrypcji
```
PS C:\> $Zones = Get-AzDnsZone
```

W tym przykładzie wszystkie strefy DNS w bieżącej subskrypcji platformy Azure są przechowywane w $Zones danych.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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
Określa nazwę strefy DNS do uzyskania.
Jeśli nie określisz wartości dla *parametru Name,* to polecenie cmdlet pobiera wszystkie strefy DNS w określonej grupie zasobów.
Jeśli parametr *ResourceGroupName* zostanie pominięty, to polecenie cmdlet pobiera wszystkie strefy DNS w bieżącej subskrypcji platformy Azure.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, która zawiera strefę DNS do uzyskania.
Jeśli nie określisz *parametru ResourceGroupName,* musisz również pominąć parametr *Name.*
W tym przypadku to polecenie cmdlet pobiera wszystkie strefy DNS w bieżącej subskrypcji platformy Azure.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Dns.DnsZone

## NOTATKI

## LINKI POKREWNE

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
