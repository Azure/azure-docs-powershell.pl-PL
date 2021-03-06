---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 31729843425f2360f1716e2b0faffc72715b9a81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707605"
---
# Get-AzStorageUsage

## STRESZCZENIe
Pobiera użycie zasobu magazynu dla bieżącej subskrypcji.

## POLECENIA

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzStorageUsage** pobiera użycie zasobów w usłudze Azure Storage dla bieżącej subskrypcji.

## Przykłady

### Przykład 1: uzyskiwanie użycia zasobów magazynowania w określonej lokalizacji
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

To polecenie uzyskuje użycie zasobów magazynowania w określonej lokalizacji w ramach bieżącej subskrypcji.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### — Lokalizacja
Wskaż, aby pobrać użycie zasobów magazynowania w określonej lokalizacji.
Jeśli nie określono tego pola, będziesz mieć dostęp do zasobów magazynowania we wszystkich lokalizacjach w ramach abonamentu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Management. Storage. models. PSUsage

## INFORMACYJN

## LINKI POKREWNE

[Polecenia cmdlet usługi Azure Storage Manager](./Az.Storage.md)


