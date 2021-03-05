---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 80a471b88856ff4c7425e89fd6e5b73168370789
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998509"
---
# Set-AzDataFactorySliceStatus

## SYNOPSIS
Ustawia stan wycinków dla zestawu danych w usłudze Azure Data Factory.

## SKŁADNIA

### ByFactoryName (Default)
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzDataFactorySliceStatus** ustawia stan wycinków dla zestawu danych w usłudze Azure Data Factory.

## PRZYKŁADY

### Przykład 1. Ustawianie stanu wszystkich wycinków
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

To polecenie ustawia stan wszystkich wycinków dla zestawu danych o nazwie DAWikiAggregatedData do oczekiwania w fabrycznej bazie danych o nazwie WikiADF.
Parametr *UpdateType* ma wartość UpstreamInPipeline, więc polecenie ustawia stan każdego wycinka dla zestawu danych i wszystkich zestawów danych zależnych.
Zestawy danych zależnych są używane jako zestawy danych wejściowych dla działań w potoku.
To polecenie zwraca wartość $True.

## PARAMETERS

### -DataFactory
Określa obiekt **PSDataFactory.**
To polecenie cmdlet modyfikuje stan wycinków należących do fabrycznej transmisji danych, które określa ten parametr.

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
To polecenie cmdlet modyfikuje stan wycinków należących do fabrycznej transmisji danych, które określa ten parametr.

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

### -DatasetName
Określa nazwę zestawu danych, dla którego to polecenie cmdlet modyfikuje wycinki.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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

### -EndDateTime
Określa koniec okresu jako obiekt **DateTime.**
Tym razem jest to koniec wycinka danych.
Aby uzyskać więcej informacji na **temat obiektów DateTime,** wpisz `Get-Help Get-Date` tekst.
*Wartość EndDateTime* musi zostać określona w formacie ISO8601, jak podano w poniższych przykładach: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (pacyficzny czas standardowy) Domyślnym projektem strefy czasowej jest czas UTC.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet modyfikuje stan wycinków należących do grupy, która jest określana przez ten parametr.

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

### -StartDateTime
Określa początek okresu jako obiekt **DateTime.**
Tym razem jest to początek wycinka danych.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Status
Określa stan, który ma zostać przypisany do wycinka danych.
Dopuszczalne wartości dla tego parametru to:
- Oczekiwanie.
Wycinek danych oczekuje na weryfikację przed przetworzeniem przez zasady sprawdzania poprawności. 
- Gotowe.
Przetwarzanie danych zostało ukończone, a wycinek danych jest gotowy.
- InProgress (Ruch wychodzący).
Przetwarzanie danych jest w toku. 
- Niepowodzenie.
Przetwarzanie danych nie powiodło się.
- Pominięte.
Pominięto przetwarzanie wycinka danych.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateType
Określa typ aktualizacji wycinka.
Dopuszczalne wartości dla tego parametru to:
- Osoba.
Ustawia stan każdego wycinka dla zestawu danych w określonym zakresie czasu. 
- UpstreamInPipeline.
Ustawia stan każdego wycinka dla zestawu danych i wszystkich zależnych zestawów danych, które są używane jako zestawy danych wejściowych dla działań w potoku.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## DANE WYJŚCIOWE

### System.Boolean

## NOTATKI
* Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki

## LINKI POKREWNE

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


