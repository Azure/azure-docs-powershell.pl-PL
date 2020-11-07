---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 50384630658f7626ee02ca1dee223e82bf122ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719494"
---
# New-AzureRmStorageAccount

## STRESZCZENIe
Tworzy konto magazynu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmStorageAccount** umożliwia utworzenie konta usługi Azure Storage.

## Przykłady

### Przykład 1. Tworzenie konta magazynu
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS"
```

To polecenie tworzy konto magazynu dla nazwy grupy zasobów moja grupa zasobów.

### Przykład 2: Tworzenie konta magazynu obiektów BLOB używającego szyfrowania usługi magazynu
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

To polecenie tworzy konto magazynu obiektów BLOB korzystające z typu hot Access.
Konto ma włączone szyfrowanie usługi magazynowania w usłudze BLOB.

### Przykład 3: Tworzenie konta magazynu, które umożliwia szyfrowanie usługi magazynu w przypadku obiektów blob i usług plików oraz wygenerowanie i przypisanie tożsamości dla magazynu danych platformy Azure.
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

To polecenie tworzy konto magazynu z włączonym szyfrowaniem usługi magazynu w przypadku obiektów blob i usług plików.  Generuje także i przypisuje tożsamość, która może być używana do zarządzania kluczami kont za pośrednictwem usługi Azure Keys.

## PARAMETRÓW

### -AccessTier
Określa warstwę dostępu konta magazynu tworzonego przez to polecenie cmdlet.
Dopuszczalne wartości tego parametru to: gorące i chłodzone.

W przypadku określenia wartości BlobStorage dla parametru *Kind* należy określić wartość parametru *AccessTier* .

Jeśli określisz wartość określającą miejsce do magazynowania dla tego parametru *typu* , nie określaj parametru *AccessTier* .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignIdentity
Wygeneruj i przypisz nową tożsamość konta magazynu dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.

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

### -CustomDomainName
Określa nazwę domeny niestandardowej konta magazynu.
Wartość domyślna to Storage.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableEncryptionService
Wskazuje, czy to polecenie cmdlet umożliwia szyfrowanie usługi magazynu w usłudze magazynu.
Usługa Azure BLOB i usługi Azure File Services są obsługiwane.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Wskazuje, czy konto magazynu umożliwia tylko ruch https.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.

Dopuszczalne wartości tego parametru to:

- Kontynuacj
- Ignorować
- Inquire
- SilentlyContinue
- Przestaw
- Wykonywanie

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Określa zmienną informacyjną.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kind
Określa rodzaj konta magazynu tworzonego przez to polecenie cmdlet.
Dopuszczalne wartości tego parametru to:

- Chowan.
Ogólne konto magazynu, które obsługuje przechowywanie obiektów blob, tabel, kolejek, plików i dysków.
 
- BlobStorage.
Konto magazynu obiektów BLOB obsługujące tylko przechowywanie obiektów BLOB.
 

Wartość domyślna to Storage.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Określa lokalizację konta magazynu, które ma zostać utworzone.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę konta magazynu, które ma zostać utworzone.

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

### -NetworkRuleSet
Konto magazynu NetworkRuleSet

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, w której ma zostać dodane konto magazynu.

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

### -SkuName
Określa nazwę SKU konta magazynu tworzonego przez to polecenie cmdlet.
Dopuszczalne wartości tego parametru to:

- Standard_LRS.
Magazyn lokalny-nadmiarowy. 
- Standard_ZRS.
Miejsce do magazynowania nadmiarowych stref.
- Standard_GRS.
Magazyn Geograficznie nadmiarowy. 
- Standard_RAGRS.
Dostęp do odczytu geograficznie zapasowego miejsca. 
- Premium_LRS.
Premium miejsce do magazynowania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
W przypadku określenia wartości BlobStorage dla parametru *Kind* należy określić wartość parametru *AccessTier* .

Jeśli określisz wartość określającą miejsce do magazynowania dla tego parametru *typu* , nie określaj parametru *AccessTier* .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSubDomain
Wskazuje, czy włączyć weryfikację pośredniego rekordu CName.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
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

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmStorageAccount](./Get-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)

[Set-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)


