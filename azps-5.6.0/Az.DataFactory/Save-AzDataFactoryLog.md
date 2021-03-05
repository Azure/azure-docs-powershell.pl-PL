---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: eb2e3c9acd93e8b20c7bdf6f4ee04ef2910a3cbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006970"
---
# Save-AzDataFactoryLog

## SYNOPSIS
Pobiera pliki dziennika z przetwarzania usługi Azure HDInsight.

## SKŁADNIA

### ByFactoryName (Default)
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Save-AzDataFactoryLog** pobiera pliki dziennika skojarzone z przetwarzaniem usługi Azure HDInsight w projektach Prosia lub Gałąź albo na niestandardowe działania na lokalnym dysku twardym.
Najpierw uruchom polecenie cmdlet Get-AzDataFactoryRun w celu uzyskania identyfikatora działania uruchomionego dla wycinka danych, a następnie użyj tego identyfikatora do pobrania plików dziennika z magazynu danych dużego obiektu binarnego (BLOB) skojarzonego z klasterem HDInsight.
Jeśli parametr *DownloadLogs* nie zostanie określony, polecenie cmdlet po prostu zwróci lokalizację plików dziennika.
Jeśli określisz *wartości DownloadLogs* bez określenia katalogu wyjściowego (parametru *wyjściowego),* pliki dziennika zostaną pobrane do domyślnego folderu Dokumenty.
Jeśli oprócz folderu wyjściowego (Danychwyjściowych) określisz wartości *DownloadLogs,* pliki dziennika zostaną pobrane do określonego folderu.

## PRZYKŁADY

### Przykład 1. Zapisywanie plików dziennika w określonym folderze
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

To polecenie zapisuje pliki dziennika dla działania uruchamianego z identyfikatorem 841b77c9-d56c-48d1-99a3-8c16c3e77d39, gdzie działanie należy do potoku w fabrycznej układzie danych o nazwie LogProcessingFactory w grupie zasobów o nazwie ADF.
Pliki dziennika są zapisywane w folderze C:\Test.

### Przykład 2. Zapisywanie plików dziennika w domyślnym folderze Dokumenty
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

To polecenie zapisuje pliki dziennika w folderze Dokumenty (domyślnie).

### Przykład 3. Uzyskiwanie lokalizacji plików dziennika
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

To polecenie zwraca lokalizację plików dziennika.
Pamiętaj, że nie określono *listy DownloadLogs.*

## PARAMETERS

### -DataFactory
Określa obiekt **PSDataFactory.**

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Określa nazwę fabryki danych.
To polecenie cmdlet pobiera pliki dziennika dla fabrycznych danych, które określa ten parametr.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
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

### -DownloadLogs
Wskazuje, że to polecenie cmdlet pobiera pliki dziennika na komputer lokalny.
Jeśli *nie* określono folderu wyjściowego, pliki są zapisywane w folderze Dokumenty w podfolderze.

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

### — Identyfikator
Określa identyfikator działania uruchamianego dla wycinka danych.
Użyj Get-AzDataFactoryRun cmdlet, aby uzyskać identyfikator.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Dane wyjściowe
Określa folder wyjściowy, w którym są zapisywane pobrane pliki dziennika.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet tworzy grupę danych należącą do grupy, która jest określana przez ten parametr.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo

## NOTATKI
* Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki

## LINKI POKREWNE

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Get-AzDataFactoryPipeline](./Get-AzDataFactoryPipeline.md)

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


