---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: edb2e94900d383675bd183c09df16e295828aae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705946"
---
# Set-AzDataFactoryPipelineActivePeriod

## STRESZCZENIe
Umożliwia skonfigurowanie aktywnego okresu wycinków danych.

## POLECENIA

### ByFactoryName (domyślny)
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzDataFactoryPipelineActivePeriod** umożliwia skonfigurowanie aktywnego okresu dla wycinków danych, które są przetwarzane przez potok w fabryce danych platformy Azure.
Jeśli używasz polecenia cmdlet Set-AzDataFactorySliceStatus, aby zmodyfikować stan wycinków dla zestawu danych, upewnij się, że godzina rozpoczęcia i godzina zakończenia wycinka są w aktywnym okresie potoku.
Po utworzeniu rurociągu możesz określić okres, w którym odbywa się przetwarzanie danych.
Określenie aktywnego okresu dla rurociągu określa czas trwania, w którym wycinki danych są przetwarzane na podstawie właściwości **dostępności** , które zostały zdefiniowane dla każdego zestawu danych fabryki danych.

## Przykłady

### Przykład 1: Konfigurowanie aktywnego okresu
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

To polecenie umożliwia skonfigurowanie aktywnego okresu wycinków danych, które potok o nazwie DPWikisample procesów.
Polecenie udostępnia punkty początkowe i końcowe wycinków danych jako wartości.
Polecenie zwraca wartość $True.

## PARAMETRÓW

### -Autorozpoznawanie
Wskazuje, że w tym poleceniu cmdlet jest używane automatyczne rozpoznawanie.

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

### -DataFactory
Określa obiekt **PSDataFactory** .
To polecenie cmdlet modyfikuje aktywny okres dla rurociągu należącego do fabryki danych, którą ten parametr określa.

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
To polecenie cmdlet modyfikuje aktywny okres dla rurociągu należącego do fabryki danych, którą ten parametr określa.

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

### -EndDateTime
Określa koniec okresu jako obiekt **DateTime** .
Przetwarzanie danych lub wycinki danych są przetwarzane w tym okresie.
Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .
*EndDateTime* należy określić w formacie ISO8601, tak jak w poniższych przykładach: 2015-01-01Z 2015-01-01T00:00:00Z z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00 – 08:00 (czas standardowy)

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

### -ForceRecalculate
Wskazuje, że polecenie cmdlet Wymusza ponowne obliczenie.

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

### -Pipelinename
Określa nazwę potoku.
To polecenie cmdlet ustawia aktywny okres dla rurociągu określanego przez ten parametr.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet modyfikuje aktywny okres dla rurociągu należącego do grupy, którą ten parametr określa.

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
Określa początek okresu jako obiekt **DateTime** .
Przetwarzanie danych lub wycinki danych są przetwarzane w tym okresie.
*StartDateTime* należy określić w formacie ISO8601.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## WYSYŁA

### System. Boolean

## INFORMACYJN
* Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki

## LINKI POKREWNE

[Nowe — AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)


