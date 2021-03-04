---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 9f52e2a709e2518dbc749b20afc97125e9b3ae64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975418"
---
# Get-AzDataFactoryLinkedService

## SYNOPSIS
Pobiera informacje o usługach połączonych w usłudze Azure Data Factory.

## SKŁADNIA

### ByFactoryName (Default)
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzDataFactoryLinkedService** pobiera informacje o usługach połączonych w usłudze Azure Data Factory.
Jeśli określisz nazwę usługi połączonej, to polecenie cmdlet pobiera informacje o tej połączonej usłudze.
Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich połączonych usługach w zakładzie danych.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie informacji o wszystkich połączonych usługach
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

To polecenie pobiera informacje o wszystkich połączonych usługach w factory danych o nazwie WikiADF, a następnie przekazuje połączone usługi do polecenia cmdlet Format-List przy użyciu operatora potoku.
To polecenie cmdlet s formatuje wyniki.
Aby uzyskać więcej informacji, wpisz `Get-Help Format-List` .

### Przykład 2. Uzyskiwanie informacji o konkretnej połączonej usłudze
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

To polecenie pobiera informacje o połączonej usłudze o nazwie HDILinkedService w zakładzie danych o nazwie WikiADF.

### Przykład 3. Uzyskiwanie informacji o określonej połączonej usłudze przez określenie parametru DataFactory
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

Pierwsze polecenie używa Get-AzDataFactory cmdlet w celu uzyskania bazy danych o nazwie ContosoFactory, a następnie zapisuje ją w $DataFactory danych.
Drugie polecenie pobiera informacje o połączonej usłudze dla fabrycznych danych przechowywanych w usłudze $DataFactory, Format-Table następnie przekazuje te informacje do polecenia cmdlet Format-Table przy użyciu operatora potoku.
**Format-Table** formatuje dane wyjściowe jako zestaw danych przy użyciu określonych właściwości jako kolumn zestawu danych.

## PARAMETERS

### -DataFactory
Określa obiekt **PSDataFactory.**
To polecenie cmdlet pobiera usługi połączone, które należą do fabrycznej usługi danych, która określa ten parametr.

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
To polecenie cmdlet pobiera usługi połączone, które należą do fabrycznej usługi danych, która określa ten parametr.

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

### — Nazwa
Określa nazwę połączonej usługi, o której mają być uzyskiwanie informacji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet pobiera usługi połączone, które należą do grupy, której parametr określa.

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

### Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService

## NOTATKI
* Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki

## LINKI POKREWNE

[New-AzDataFactoryLinkedService](./New-AzDataFactoryLinkedService.md)

[Remove-AzDataFactoryLinkedService](./Remove-AzDataFactoryLinkedService.md)


