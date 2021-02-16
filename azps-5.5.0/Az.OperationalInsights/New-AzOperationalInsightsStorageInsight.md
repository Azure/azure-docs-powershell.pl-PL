---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184098"
---
# New-AzOperationalInsightsStorageInsight

## SYNOPSIS
Tworzy szczegółowe informacje o przestrzeni dyskowej wewnątrz obszaru roboczego.

## SKŁADNIA

### ByWorkspaceName (Domyślna)
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByWorkspaceObject
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzOperationalInsightsStorageInsight** tworzy nową analizę przestrzeni dyskowej w istniejącym obszarze roboczym.

## PRZYKŁADY

### Przykład 1. Tworzenie szczegółowych informacji o przestrzeni dyskowej według nazwy
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

Pierwsze polecenie używa Get-AzStorageAccount cmdlet w celu uzyskania konta magazynu o nazwie ContosoStorage, a następnie zapisuje je w $Storage danych.
Drugie polecenie przekazuje konto magazynu w programie $Storage do polecenia cmdlet Get-AzStorageAccountKey przy użyciu operatora potoku w celu uzyskania określonego klucza konta magazynu, $StorageKey następnie zapisuje je w zmiennej $StorageKey magazynu. W tym przykładzie jest pobierany pierwszy klucz. Aby pobrać drugi z nich, użyj wartości[1] zamiast Wartość[0].
Końcowe polecenie tworzy szczegółowe informacje o przestrzeni dyskowej o nazwie MyStorageInsight w obszarze roboczym o nazwie MyWorkspace.
Ta analiza miejsca do magazynowania pobiera dane z tabeli WADWindowsEventLogsTable w określonym zasobie konta magazynu.

### Przykład 2. Tworzenie szczegółowych informacji o magazynie przy użyciu obiektu obszaru roboczego
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

Pierwsze polecenie używa Get-AzOperationalInsightsWorkspace cmdlet w celu uzyskania obszaru roboczego o nazwie MyWorkspace, a następnie zapisuje go w $Workspace danych.
Drugie polecenie używa Get-AzStorageAccount cmdlet w celu uzyskania określonego konta magazynu, a następnie zapisuje je w $Storage magazynu.
Trzecie polecenie przekazuje konto magazynu w programie $Storage do polecenia cmdlet Get-AzStorageAccountKey przy użyciu operatora potoku w celu uzyskania określonego klucza, a następnie zapisuje je w $StorageKey danych. W tym przykładzie jest pobierany pierwszy klucz. Aby pobrać drugi z nich, użyj wartości[1] zamiast Wartość[0].
Końcowe polecenie tworzy szczegółowe informacje o magazynie o nazwie MyStorageInsight w obszarze roboczym zdefiniowanym w $Workspace.
Szczegółowe informacje o magazynie zużywają dane z tabeli WADWindowsEventLogsTable w określonym zasobie konta magazynu.

## PARAMETERS

### — Containers
Określa listę kontenerów zawierających dane.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### — Wymuszanie
Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.

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
Określa nazwę szczegółowych informacji o magazynie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountKey
Określa klucz dostępu dla konta magazynu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountResourceId
Określa zasób Azure konta magazynu.
Można to pobrać, wykonując polecenie cmdlet Get-AzStorageAccount uzyskanie dostępu do *parametru Id* wyniku.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Tabele
Określa listę tabel, które dostarczają dane.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Obszar roboczy
Określa obszar roboczy dla nowej szczegółowych informacji o przestrzeni dyskowej.

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
Określa nazwę istniejącego obszaru roboczego.

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

### System.String

### System.String[]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight

## NOTATKI

## LINKI POKREWNE

[Polecenia cmdlet usługi Azure Operational Insights](./Az.OperationalInsights.md)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


