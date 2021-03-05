---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d4296acd16b29640fa8925d8482cca012be27b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994792"
---
# Get-AzStorageTable

## SYNOPSIS
Wyświetla listę tabel magazynu.

## SKŁADNIA

### Nazwa_tabeli (domyślna)
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzStorageTable** wyświetla listę tabel magazynu skojarzonych z kontem magazynu na platformie Azure.

## PRZYKŁADY

### Przykład 1. Lista wszystkich tabel magazynu platformy Azure
```
PS C:\>Get-AzStorageTable
```

To polecenie pobiera wszystkie tabele magazynu dla konta magazynu.

### Przykład 2. Lista tabel magazynu platformy Azure przy użyciu symboli wieloznacznych
```
PS C:\>Get-AzStorageTable -Name table*
```

To polecenie używa symbolu wieloznacznego w celu uzyskania tabel magazynu, których nazwa zaczyna się od tabeli.

### Przykład 3. Lista tabel magazynu platformy Azure przy użyciu prefiksu nazwy tabeli
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

To polecenie używa *parametru Prefiks* w celu uzyskania tabel magazynu, których nazwa zaczyna się od tabeli.

## PARAMETERS

### — kontekst
Określa kontekst magazynowania.
Aby go utworzyć, możesz użyć New-AzStorageContext cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę tabeli.
Jeśli nazwa tabeli jest pusta, polecenie cmdlet wyświetla listę wszystkich tabel.
W przeciwnym razie wyświetla listę wszystkich tabel, które pasują do określonej nazwy lub wzorca nazw zwykłych.

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### —Prefiks
Określa prefiks użyty w nazwie tabeli lub tabel, które mają zostać użyte.
Dzięki temu można znaleźć wszystkie tabele, które zaczynają się od tego samego ciągu znaków, na przykład tabelę.

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## DANE WYJŚCIOWE

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable

## NOTATKI

## LINKI POKREWNE

[New-azstorageTable](./New-AzStorageTable.md)

[Remove-azstorageTable](./Remove-AzStorageTable.md)


