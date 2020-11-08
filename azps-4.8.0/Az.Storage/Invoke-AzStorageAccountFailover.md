---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221044"
---
# Invoke-AzStorageAccountFailover

## STRESZCZENIe
Wywołuje tryb failover konta magazynu.

## POLECENIA

### AccountName (domyślnie)
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountName
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Wywołuje tryb failover konta magazynu. Żądanie przejęcia awaryjnego można wyzwolić dla konta magazynu w przypadku problemów z dostępnością. Przejście do trybu failover jest wykonywane z podstawowego klastra konta magazynu w klastrze pomocniczym dla kont RA-GRS. Klaster pomocniczy stanie się podstawowym po przełączeniu do trybu failover.
Przed rozpoczęciem pracy awaryjnej zapoznaj się z następującym wpływem na konto magazynu: 1,1. Sprawdź czas ostatniej synchronizacji, korzystając z funkcji Pobierz statystykę usługi BLOB (Aby uzyskać statystykę https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) dotyczącą usługi tabeli ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) i uzyskać statystykę usługi kolejkowania) ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) dla Twojego konta. W przypadku inicjowania pracy awaryjnej możesz utracić dane, które mogą zostać utracone.
2. po przełączeniu do trybu failover typ konta magazynu zostanie przekonwertowany na lokalnie nadmiarowy magazyn (LRS). Możesz przekonwertować swoje konto, aby używać magazynu geograficznie nadmiarowego (GRS).
3. po ponownym włączeniu GRS dla konta magazynu firma Microsoft będzie replikować dane do nowego regionu pomocniczego. Czas replikacji zależy od ilości danych do zreplikowania. Pamiętaj, że w przypadku ładowania początkowego są dostępne opłaty za przepustowość. https://azure.microsoft.com/en-us/pricing/details/bandwidth/

## Przykłady

### Przykład 1: wywoływanie trybu failover dla konta magazynu
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

To polecenie umożliwia sprawdzenie ostatniej synchronizacji konta magazynu w celu przełączenia jej do trybu failover, a klaster pomocniczy stanie się podstawowym po przełączeniu do trybu failover. Ponieważ praca awaryjna zabiera dużo czasu, zaleca się jej uruchomienie w parametrze wewnętrznej bazy danych with AsJob, a następnie zaczekanie na zakończenie zadania.

## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle

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

### -Force
Wymuś przejęcie konta w trybie failover

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

### -Inputobject
Obiekt konta magazynu

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa konta magazynu.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

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
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount

## INFORMACYJN

## LINKI POKREWNE
