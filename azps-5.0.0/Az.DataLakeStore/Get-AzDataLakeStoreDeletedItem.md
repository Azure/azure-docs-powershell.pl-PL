---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305628"
---
# Get-AzDataLakeStoreDeletedItem

## STRESZCZENIe
Wyszukuje usunięte wpisy w koszu, które pasują do filtru.

## POLECENIA

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzDataLakeStoreDeletedItem** przeszukuje usunięte pliki lub foldery w usłudze Data Lake Store, które pasują do danego filtru.
Wyświetla następujące atrybuty elementów usuniętych — OriginalPath, TrashDirPath, Type, CreationTime.
Może to być długotrwała operacja, ponieważ może być konieczne przeszukanie milionów plików w koszu i uruchomienie jej jako zadania.
Przestroga: usuwanie plików jest najlepszym rozwiązaniem. Nie ma gwarancji, że plik może zostać przywrócony po jego usunięciu. Korzystanie z tego interfejsu API jest włączone za pośrednictwem whitelisting. Jeśli Twoje konto usługi ADL nie jest whitelisted, użycie tego interfejsu API spowoduje zgłoszenie wyjątku niezaimplementowane. Aby uzyskać więcej informacji i uzyskać pomoc, skontaktuj się z pomocą techniczną firmy Microsoft.

## Przykłady

### Przykład: uzyskiwanie szczegółowych informacji o pliku z usługi Data Lake Store
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## PARAMETRÓW

### — Konto
Określa nazwę konta usługi Data Lake Store.

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

### -AsJob
Uruchom polecenie cmdlet w tle.

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

### -Count
Określa liczbę wyników, które użytkownik chce znaleźć. Kwerenda jest uruchamiana do momentu znalezienia wyników zliczania lub przeszukania całego kosza, co zdarza się najpierw.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Filter
Określa zapytanie wyszukiwania. Dokładniejsze wyniki są bardziej szczegółowe.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### System. Collections. Generic. list<Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreDeletedItem>

## INFORMACYJN

## LINKI POKREWNE

[Restore-AzDataLakeStoreDeletedItem](./Restore-AzDataLakeStoreDeletedItem.md)