---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: a82bec40d93b33385dfa9aa2b4a5c5d122e59aa2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708067"
---
# Set-AzServiceFabricUpgradeType

## STRESZCZENIe
Zmienianie typu uaktualnienia sieci szkieletowej usług dla klastra.

## POLECENIA

### Automatyczne
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Ręcznie
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Funkcja **Set-AzServiceFabricUpgradeType** umożliwia ustawienie typu uaktualnienia na automatyczny lub ręczny z określoną wersją kodu sieci szkieletowej usługi.

## Przykłady

### Przykład 1
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

To polecenie spowoduje ustawienie trybu uaktualniania klastra na wartość automatycznie.

## PARAMETRÓW

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

### -Name (nazwa)
Określ nazwę klastra.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Upgrademode
ClusterUpgradeMode

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Version
Wersja kodu klastra.

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. servicefabric. MODELES. ClusterUpgradeMode

## WYSYŁA

### Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster

## INFORMACYJN

## LINKI POKREWNE
