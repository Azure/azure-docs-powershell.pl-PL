---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 860e87063810251075341cd1eddd013870734384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542136"
---
# Set-AzureRmStorageAccount

## STRESZCZENIe
Modyfikuje konto magazynu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### StorageEncryption (domyślny)
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### KeyvaultEncryption
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmStorageAccount** modyfikuje konto usługi Azure Storage.
Za pomocą tego polecenia cmdlet można zmodyfikować typ konta, zaktualizować domenę klienta lub ustawić Tagi na koncie magazynu.

## Przykłady

### Przykład 1: Ustawianie typu konta magazynu
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

To polecenie ustawia typ konta magazynu na Standard_RAGRS.

### Przykład 2: Ustawianie domeny niestandardowej dla konta magazynu
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

To polecenie ustawia niestandardową domenę dla konta magazynu.

### Przykład 3: Włączanie szyfrowania obiektów blob i usług plików
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

To polecenie umożliwia włączenie szyfrowania obiektu BLOB i pliku dla konta magazynu.

### Przykład 4: Ustawianie wartości warstwy dostępu
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

Polecenie ustawia wartość w warstwie dostępu jako schłodzić.

### Przykład 4: Ustawianie niestandardowej domeny i tagów
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

Polecenie ustawia wartość w warstwie dostępu jako schłodzić.

### Przykład 5: Włączanie szyfrowania w usługach BLOB za pomocą magazynu typu
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

To polecenie umożliwia włączenie szyfrowania obiektu BLOB przy użyciu nowego utworzonego magazynu.

### Przykład 6: wyłączenie szyfrowania w usługach plików za pomocą zestawu źródeł klucza "Microsoft. Storage"
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

To polecenie wyłącza szyfrowanie usług plików za pomocą zestawu źródeł klucza "Microsoft. Storage"

## PARAMETRÓW

### -AccessTier
Określa warstwę dostępu konta magazynu, które jest modyfikowane przez to polecenie cmdlet.
Dopuszczalne wartości tego parametru to: gorące i chłodzone.

Zmiana warstwy dostępu może spowodować dodatkowe opłaty.
Aby uzyskać więcej informacji, zobacz Usługa Azure Blob Storage: warstwy magazynowania dla urządzeń typu hot i chłodn https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .
Jeśli typ konta magazynu to magazyn, nie określaj tego parametru.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignIdentity
Wygeneruj i przypisz nową tożsamość konta magazynu dla tego konta magazynu do użycia z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDomainName
Określa nazwę domeny niestandardowej.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableEncryptionService
Wskazuje, czy to polecenie cmdlet wyłącza szyfrowanie usługi magazynu w usłudze magazynu.
Usługa Azure BLOB i usługi Azure File Services są obsługiwane.

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableEncryptionService
Wskazuje, czy to polecenie cmdlet umożliwia szyfrowanie usługi magazynu w usłudze magazynu.
Usługa Azure BLOB i usługi Azure File Services są obsługiwane.

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Wskazuje, czy konto magazynu umożliwia tylko ruch https.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Zmiana warstwy dostępu może spowodować dodatkowe opłaty.
Aby uzyskać więcej informacji, zobacz Usługa Azure Blob Storage: warstwy magazynowania dla urządzeń typu hot i chłodn https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .
Jeśli typ konta magazynu to magazyn, nie określaj tego parametru.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Type: ActionPreference
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
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NazwaKlucza
Dysk źródłowy klucza szyfrowania konta magazynu # NazwaKlucza

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyvaultEncryption
Określa, czy należy ustawić źródło klucza szyfrowania konta magazynu na Microsoft. lub nie.
Jeśli określisz wartość KeyName, wersja klucza i KeyvaultUri, Źródło klucza szyfrowania konta magazynu zostanie również ustawione na Microsoft. Pogoda dla magazynu danych ten parametr jest ustawiony lub nie.
```yaml
Type: SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultUri
KeyVaultUria klucza źródłowego klucza szyfrowania konta magazynu

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wersja-
Wersja klucza magazynu klucza szyfrowania konta magazynu

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę konta magazynu, które ma zostać zmodyfikowane.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, w której należy zmodyfikować konto magazynu.

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

### -SkuName
Określa nazwę SKU konta magazynu.
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

Nie można zmieniać typów Standard_ZRS i Premium_LRS na inne typy kont.
Nie można zmienić innych typów kont na Standard_ZRS lub Premium_LRS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEncryption
Czy chcesz ustawić źródło klucza szyfrowania konta magazynu na Microsoft. Storage, czy nie.

```yaml
Type: SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Jeśli określisz wartość BlobStorage dla parametru *Kind* polecenia cmdlet New-AzureRmStorageAccount, musisz określić wartość parametru *AccessTier* .

Jeśli określisz wartość określającą miejsce do magazynowania dla tego parametru *typu* , nie określaj parametru *AccessTier* .

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UseSubDomain
Wskazuje, czy włączyć weryfikację pośredniego rekordu CName.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmStorageAccount](./Get-AzureRmStorageAccount.md)

[Nowe — AzureRmStorageAccount](./New-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)
