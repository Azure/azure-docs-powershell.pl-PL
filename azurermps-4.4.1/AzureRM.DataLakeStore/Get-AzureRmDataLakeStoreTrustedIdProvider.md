---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: e95fd5e487fc29a40e48484b0a905def8356e260
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551052"
---
# Get-AzureRmDataLakeStoreTrustedIdProvider

## STRESZCZENIe
Pobiera określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.
Jeśli nie podano dostawcy, wyświetla listę wszystkich dostawców dla tego konta.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmDataLakeStoreTrustedIdProvider** pobiera określonego zaufanego dostawcę tożsamości w określonej usłudze Data Lake Store.
Jeśli nie podano dostawcy, wyświetla listę wszystkich dostawców dla tego konta.

## Przykłady

### Przykład 1: uzyskiwanie określonego zaufanego dostawcy tożsamości
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

Zwraca dostawcę o nazwie "Moja" z konta "ContosoADL".

### Przykład 2: Wyświetlanie listy wszystkich dostawców na koncie
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

Wyświetla listę wszystkich dostawców pod kontem "ContosoADL"

## PARAMETRÓW

### — Konto
Konto usługi Data Lake Store do pobrania zaufanego dostawcy tożsamości z

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

### -Name (nazwa)
Nazwa dostawcy zaufanej tożsamości do pobrania

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów, pod którą ma zostać pobrane określone konto zaufanego dostawcy tożsamości.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### DataLakeStoreTrustedIdProvider
Szczegóły określonego dostawcy zaufanej tożsamości.

### IList<DataLakeStoreTrustedIdProvider>
Lista zaufanych dostawców tożsamości na określonym koncie.

## INFORMACYJN

## LINKI POKREWNE

