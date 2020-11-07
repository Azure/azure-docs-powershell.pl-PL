---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 07b5de12e042c81bb5f27c844d1fc8962453310a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719324"
---
# New-AzureRmEventHubNamespace

## STRESZCZENIe
Tworzy obszar nazw koncentratorów zdarzeń.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### NamespaceParameterSet (domyślny)
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### AutoInflateParameterSet
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-EnableAutoInflate]
 [-MaximumThroughputUnits] <Int32> [-WhatIf] [-Confirm]
```

## Opis
Polecenie cmdlet New-AzureRmEventHubNamespace tworzy nowy obszar nazw dla koncentratorów zdarzeń.

## Przykłady

### Przykład 1
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation 
```

Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` w obszarze MyResourceGroupName grupy zasobów \` \` .

### Przykład 2
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

Tworzy obszar nazw koncentratorów zdarzeń \` \` w określonej lokalizacji geograficznej moja \` Lokalizacja \` , w grupie zasoby \` MyResourceGroupName \` i funkcja autorozdęcie jest włączona z MaximumThroughputUnits 10.

## PARAMETRÓW

### — Lokalizacja
Lokalizacja obszaru geograficznego dla koncentratorów zdarzeń.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuCapacity
Jednostki przepływności centrum zdarzeń.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuName
Nazwa SKU obszaru nazw.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Hashtable, które reprezentują znaczniki zasobów.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoInflate
Wskazuje, czy funkcja autorozdęcie jest włączona

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumThroughputUnits
Górny limit jednostek przepływności, gdy funkcja podwyższanie jest włączona, vaule powinna należeć do zakresu od 0 do 20 jednostek przepływności.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa obszaru nazw EventHub.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## WEJŚCIOWE

### System. String
System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral; PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089 \] \] System. Collections. Hashtable

## WYSYŁA

### Microsoft. Azure. Commands. EventHub. modele. NamespaceAttributes

## INFORMACYJN

## LINKI POKREWNE

