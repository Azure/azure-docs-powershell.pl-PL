---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 97994eb9898f5eca3e8f7f3015e2ce96845d5c24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182274"
---
# New-AzApplicationInsightsContinuousExport

## SYNOPSIS
Tworzenie nowej konfiguracji eksportu ciągłego szczegółowych informacji o aplikacji dla zasobu szczegółowych informacji o aplikacjach

## SKŁADNIA

### ComponentNameParameterSet (Domyślne)
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ComponentObjectParameterSet
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdParameterSet
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Tworzenie nowej konfiguracji eksportu ciągłego szczegółowych informacji o aplikacji dla zasobu szczegółowych informacji o aplikacjach

## PRZYKŁADY

### Przykład 1. Tworzenie nowej konfiguracji eksportu ciągłego dla zasobu szczegółowych informacji o aplikacjach
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

Utwórz nową konfigurację eksportu ciągłego szczegółowych informacji o aplikacji, aby wyeksportować typy dokumentów "Żądanie" i "Śledzenie" do magazynu zawierającego "testcontainer" w koncie magazynu "teststorageaccount" w grupie zasobów "grupa testowa". Token SAS musi być prawidłowy i mieć uprawnienie do zapisu w kontenerze, w przeciwnym razie funkcja eksportu ciągłego nie będzie działać. Jeśli token SAS wygasł, funkcja eksportu ciągłego przestanie działać.

## PARAMETERS

### -ApplicationInsightsComponent
Obiekt składnika Szczegółowe informacje o aplikacji.

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### -DocumentType
Typy dokumentów, które wymagają wyeksportowania.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Nazwa składnika.

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator składnika szczegółowych informacji aplikacji.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - StorageAccountId
Identyfikator konta magazynu docelowego.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageLocation
Identyfikator lokalizacji przechowywania docelowego.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageSASUri
Dane Uri SAS magazynu docelowego.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration

## NOTATKI

## LINKI POKREWNE
