---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: c27319e368223b00ba17caf9d408e6a1010c766d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994456"
---
# Update-AzDataLakeAnalyticsComputePolicy

## SYNOPSIS
Aktualizuje regułę zasad obliczeniowych usługi Data Lake Analytics dla określonej jednostki AAD.

## SKŁADNIA

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
**Aktualizacja-AzDataLakeAnalyticsComputePolicy** aktualizuje określoną regułę zasad obliczeniowych dla określonej jednostki AAD na koncie usługi Azure Data Lake Analytics.

## PRZYKŁADY

### Przykład 1. Aktualizowanie jednej reguły w zasadach obliczania
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

To polecenie aktualizuje zasady o nazwie "myPolicy" na koncie "contosoadla", aby upewnić się, że użytkownik nie może przesłać żadnego zadania z więcej niż 5 jednostkami analizy.

### Przykład 2. Tworzenie zasad obliczania z aktualizacją obu reguł
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

To polecenie tworzy zasady o nazwie "myPolicy" na koncie "contosoadla", aby upewnić się, że użytkownik nie może przesłać żadnego zadania z więcej niż 5 jednostkami analizy lub o priorytecie niższym niż 100

## PARAMETERS

### — Konto
Nazwa konta, dla których mają być aktualizowane zasady obliczania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
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

### -MaxAnalyticsUnitsPerJob
Maksymalna liczba jednostek analizy na zadanie w ramach tych zasad. Musi zostać określony parametr MinPriorityPerJob lub oba parametry.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinPriorityPerJob
Minimalny priorytet obsługiwany dla każdego zadania w tych zasadach. Musi zostać określony parametr MaxAnalyticsUnitsPerJob lub oba parametry.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Nazwa zasad obliczania do zaktualizowania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów, w której istnieje konto.
Opcjonalne i podejmie próbę odnajdowania, jeśli nie zostanie podany.

```yaml
Type: System.String
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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy

## NOTATKI

## LINKI POKREWNE
