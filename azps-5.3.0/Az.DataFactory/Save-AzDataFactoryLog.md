---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503649"
---
# Save-AzDataFactoryLog

## STRESZCZENIe
Pobiera pliki dziennika z przetwarzania usługi Azure HDInsight.

## POLECENIA

### ByFactoryName (domyślny)
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Save-AzDataFactoryLog** umożliwia pobieranie plików dziennika skojarzonych z przetwarzaniem usługi Azure HDInsight dla projektów świni lub Hive oraz dla niestandardowych aktywności na lokalnym dysku twardym.
Uruchom polecenie cmdlet Get-AzDataFactoryRun, aby uzyskać identyfikator działania dla wycinka danych, a następnie użyj tego identyfikatora w celu pobrania plików dziennika z magazynu dużych obiektów binarnych (BLOB) skojarzonego z klastrem usługi HDInsight.
Jeśli nie określisz parametru *DownloadLogs* , polecenie cmdlet zwróci tylko lokalizację plików dziennika.
Jeśli określisz *DownloadLogs* bez określania katalogu wyjściowego (parametr *wyjściowy* ), pliki dziennika zostaną pobrane do domyślnego folderu dokumenty.
Jeśli określisz *DownloadLogs* razem z folderem wyjściowym (*wyjściem*), pliki dziennika zostaną pobrane do określonego folderu.

## Przykłady

### Przykład 1: zapisywanie plików dziennika w określonym folderze
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

To polecenie zapisuje pliki dziennika dla działania uruchomionego z IDENTYFIKATORem 841b77c9-d56c-48d1-99a3-8c16c3e77d39, w którym działanie należy do potoku w fabryce danych o nazwie LogProcessingFactory w grupie zasobów o nazwie ADF.
Pliki dziennika są zapisywane w folderze C:\Test.

### Przykład 2: zapisywanie plików dziennika w folderze dokumenty domyślne
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

To polecenie zapisuje pliki dziennika w folderze dokumenty (ustawienie domyślne).

### Przykład 3: Uzyskiwanie lokalizacji plików dziennika
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

To polecenie zwraca lokalizację plików dziennika.
Zauważ, że nie podano *DownloadLogs* .

## PARAMETRÓW

### -DataFactory
Określa obiekt **PSDataFactory** .

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

### -Datafactoryname
Określa nazwę fabryki danych.
To polecenie cmdlet pobiera pliki dziennika dla fabryki danych, którą określa ten parametr.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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
Jeśli nie określono folderu *wyjściowego* , pliki są zapisywane w folderze dokumenty pod podfolderem.

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

### -ID
Określa identyfikator działania dla wycinka danych.
Użyj polecenia cmdlet Get-AzDataFactoryRun, aby uzyskać identyfikator.

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
To polecenie cmdlet umożliwia utworzenie fabryki danych należącej do grupy, którą ten parametr określa.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. datafactors. models. PSRunLogInfo

## INFORMACYJN
* Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki

## LINKI POKREWNE

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Get-AzDataFactoryPipeline](./Get-AzDataFactoryPipeline.md)

[Nowe — AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend — AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


