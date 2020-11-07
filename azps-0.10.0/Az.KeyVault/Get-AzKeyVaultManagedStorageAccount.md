---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 70ee1aaf9fb082819c626c43ba5c08ad01f0f1d6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893045"
---
# Get-AzKeyVaultManagedStorageAccount

## STRESZCZENIe
Pobiera konta usługi Azure Storage zarządzane za pomocą magazynu kluczy.

## POLECENIA

### ByVaultName (domyślny)
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByAccountName
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Pobiera konto magazynu usługi Azure Storage zarządzane, jeśli określono nazwę konta, a klucze kont są zarządzane przez określony magazyn. Jeśli nazwa konta nie zostanie określona, na liście znajdują się wszystkie konta, których klucze są zarządzane przez określony magazyn.

## Przykłady

### Przykład 1: wyświetlanie wszystkich kont magazynu zarządzanych przez Magazyn kluczy
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'
```

Wyświetla listę wszystkich kont, których klucze zarządza magazynem magazynu.

### Przykład 2: Uzyskiwanie konta magazynu zarządzanego w magazynie kluczy
```
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

Pobiera szczegóły konta magazynu zarządzanego w magazynie kluczy "mystorageaccount", jeśli klucze są zarządzane przez magazyn "Moja magazyn"

## PARAMETRÓW

### -AccountName
Nazwa konta magazynu zarządzanego w magazynie kluczy. Polecenie cmdlet tworzy nazwę FQDN nazwy konta zarządzanego magazynu na podstawie nazwy magazynu, obecnie wybranego środowiska i zarządzanej nazwy konta magazynu.

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Magazynname
Nazwa magazynu.
Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. platforming. models. ManagedStorageAccount, Microsoft. Azure. Commands
Microsoft. Azure. Commands. platforming. models. ManagedStorageAccount

## INFORMACYJN

## LINKI POKREWNE

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

