---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 24c9f9631f1a37e218ff8ddf27ad0de54f2d9dbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975425"
---
# Get-AzDataFactoryHub

## SYNOPSIS
Pobiera informacje o centrach w usłudze Azure Data Factory.

## SKŁADNIA

### ByFactoryName (Default)
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzDataFactoryHub** pobiera informacje o centrach w usłudze Azure Data Factory.
Jeśli określisz nazwę centrum, to polecenie cmdlet pobiera informacje o tym centrum.
Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich koncentratorach w factory danych.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich koncentratorów danych
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

To polecenie pobiera wszystkie koncentratory danych w grupie zasobów platformy Azure o nazwie ADFResourceGroup i factory data factory o nazwie ADFDataFactory.

### Przykład 2. Uzyskiwanie określonego centrum danych
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

To polecenie pobiera informacje o centrum o nazwie MyDataHub w grupie zasobów platformy Azure o nazwie ADFResourceGroup i usłudze data factory o nazwie ADFDataFactory.

## PARAMETERS

### -DataFactory
Określa obiekt **PSDataFactory.**
To polecenie cmdlet pobiera informacje o koncentratorach w zakładzie danych, które określa ten parametr.

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
To polecenie cmdlet pobiera informacje o koncentratorach w zakładzie danych, które określa ten parametr.

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
Określa nazwę centrum, o którym mają być informacje.

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
To polecenie cmdlet pobiera informacje o centrach należących do grupy, które określa ten parametr.

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

### System.String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.DataFactories.Models.PSHub

## NOTATKI
* Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki

## LINKI POKREWNE

[New-AzDataFactoryHub](./New-AzDataFactoryHub.md)

[Remove-AzDataFactoryHub](./Remove-AzDataFactoryHub.md)


