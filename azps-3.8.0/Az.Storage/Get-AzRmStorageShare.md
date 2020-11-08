---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 2ef5ddb4a260f4749d6ccca6fa964f5e205c4b4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051268"
---
# Get-AzRmStorageShare

## STRESZCZENIe
Pobiera lub wyświetla udziały plików magazynu.

## POLECENIA

### AccountName (domyślnie)
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AccountName
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ShareResourceId
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzRmStorageShare** Pobiera lub wyświetla udziały plików magazynu.

## Przykłady

### Przykład 1: pobieranie udziału plików magazynu przy użyciu nazwy konta magazynu i nazwy udziału
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

To polecenie pobiera udział plików magazynu z nazwą konta magazynu i nazwą udziału.

### Przykład 2: wyświetlanie wszystkich udziałów plików magazynu na koncie magazynu
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
share2   myStorageAccount   myResourceGroup   "0x8D6FF862774FE57" 5120     2019-07-03 07:14:57Z
```

To polecenie wyświetla wszystkie udziały plików magazynu konta magazynu z nazwą konta magazynu.

### Przykład 3: Pobierz kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Get-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

To polecenie pobiera kontener obiektu blob magazynu z obiektem konta magazynu i nazwą kontenera.

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

### -Name (nazwa)
Nazwa udziału

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: False
Position: Named
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

### -ResourceId
Wprowadź identyfikator zasobu udziału pliku.

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccount
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

### -StorageAccountName
Nazwa konta magazynu.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount

## WYSYŁA

### Microsoft. Azure. Commands. Management. Storage. models. PSShare

## INFORMACYJN

## LINKI POKREWNE
