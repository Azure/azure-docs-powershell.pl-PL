---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: 254d9a012bd3539242e560511e23975acb68b4bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002657"
---
# New-AzStorageAccountKey

## SYNOPSIS
Ponowne generowanie klucza magazynu dla konta magazynu platformy Azure.

## SKŁADNIA

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzStorageAccountKey** ponownie generuje klucz magazynu dla konta usługi Azure Storage.

## PRZYKŁADY

### Przykład 1. Ponowne generowanie klucza magazynu
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

To polecenie ponownie generuje klucz magazynu dla określonego konta magazynu.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -KeyName
Określa klucz do ponownego wygenerowania.
Dopuszczalne wartości dla tego parametru to:
- klawisz1
- klawisz 2
- kerb1
- kerb2

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2, kerb1, kerb2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę konta magazynu, dla którego ma być ponownie wygenerowany klucz magazynu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej konto magazynu.

```yaml
Type: System.String
Parameter Sets: (All)
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

## DANE WYJŚCIOWE

### Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult

## NOTATKI

## LINKI POKREWNE

[Get-AzstorageAccountKey](./Get-AzStorageAccountKey.md)
