---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: cd540965b4de64b5fbdc5158faedf00f7a3516b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002801"
---
# Get-AzStorageAccountKey

## SYNOPSIS
Pobiera klucze dostępu dla konta magazynu platformy Azure.

## SKŁADNIA

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzStorageAccountKey** pobiera klucze dostępu dla konta magazynu platformy Azure.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie kluczy dostępu dla konta magazynu
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

To polecenie pobiera klucze dla określonego konta magazynu platformy Azure.

### Przykład 2. Uzyskiwanie określonego klucza dostępu dla konta magazynu
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### Przykład 3. Zawiera listę kluczy dostępu dla konta magazynu, w tym klucze Kerberos (jeśli włączono usługę Active Directory)
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

To polecenie pobiera klucze dla określonego konta magazynu platformy Azure.

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

### -ListKerbKey
Zawiera listę kluczy Kerberos (jeśli włączono usługę Active Directory) dla określonego konta magazynu.
Klucz Kerberos jest generowany na konto magazynu na podstawie uwierzytelniania opartego na tożsamości plików Azure za pomocą usługi domeny Azure Active Directory (Azure AD DS) lub usługi domenowej Active Directory (AD DS). Jest on używany jako hasło tożsamości zarejestrowanej w usłudze domeny, która reprezentuje konto magazynu. Klucz Kerberos nie zapewnia uprawnień dostępu do wykonywania jakichkolwiek operacji odczytu i zapisu na samolocie danych lub kontrolce na koncie magazynu.

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

### — Nazwa
Określa nazwę konta magazynu, dla którego to polecenie cmdlet uzyskuje klucze.

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

### Microsoft.Azure.Management.Storage.Models.StorageAccountKey

## NOTATKI

## LINKI POKREWNE

[New-azstorageAccountKey](./New-AzStorageAccountKey.md)


