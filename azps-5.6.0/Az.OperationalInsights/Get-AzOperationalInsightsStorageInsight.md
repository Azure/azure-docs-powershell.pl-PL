---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: adbe725557ccf1535a83f5f411cfdc44fd69c6a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981690"
---
# Get-AzOperationalInsightsStorageInsight

## SYNOPSIS
Pobiera informacje o szczegółowych informacjach o przestrzeni dyskowej.

## SKŁADNIA

### ByWorkspaceName (Domyślna)
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByWorkspaceObject
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzOperationalInsightsStorageInsight pobiera** informacje o istniejącej wiedzę na temat magazynu.
Jeśli zostanie określona nazwa szczegółowej informacji o magazynie, to polecenie cmdlet pobiera informacje o tym szczegółowe informacje o magazynie.
Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich szczegółowych informacjach dotyczących magazynu w obszarze roboczym.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie szczegółowych informacji o przestrzeni dyskowej według nazwy
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

To polecenie pobiera szczegółowe informacje o magazynie o nazwie MyStorageInsight z obszaru roboczego o nazwie ContosoWorkspace.

### Przykład 2. Uzyskiwanie szczegółowych informacji o magazynie przy użyciu obiektu obszaru roboczego
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

Pierwsze polecenie używa polecenia cmdlet **Get-AzOperationalInsightsWorkspace** w celu uzyskania obszaru roboczego szczegółowych informacji operacyjnych, a następnie zapisuje go w $Workspace danych.
Drugie polecenie pobiera szczegółowe informacje o przestrzeni dyskowej o nazwie MyStorageInsight dla obszaru roboczego w $Workspace.

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
Określa nazwę szczegółowej informacji o magazynie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.

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

### — Obszar roboczy
Określa obszar roboczy zawierający szczegółowe informacje o przestrzeni dyskowej.

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
Określa nazwę obszaru roboczego zawierającego szczegółowe informacje o magazynie.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight

## NOTATKI

## LINKI POKREWNE

[Polecenia cmdlet usługi Azure Operational Insights](./Az.OperationalInsights.md)


