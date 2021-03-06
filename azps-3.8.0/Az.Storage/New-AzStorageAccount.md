---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c88e56a485f9e42daf229667ab4c07d7a7464578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052112"
---
# New-AzStorageAccount

## STRESZCZENIe
Tworzy konto magazynu.

## POLECENIA

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzStorageAccount** umożliwia utworzenie konta usługi Azure Storage.

## Przykłady

### Przykład 1. Tworzenie konta magazynu
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

To polecenie tworzy konto magazynu dla nazwy grupy zasobów moja grupa zasobów.

### Przykład 2: Tworzenie konta magazynu obiektów BLOB przy użyciu BlobStorage i AccessTier na gorąco
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

To polecenie tworzy konto magazynu obiektów blob z BlobStorage i gorącą AccessTier

### Przykład 3: Tworzenie konta magazynu za pomocą StorageV2, a następnie Wygeneruj i przypisz tożsamość do magazynu danych platformy Azure.
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

To polecenie tworzy konto magazynu o rodzaju StorageV2.  Generuje także i przypisuje tożsamość, która może być używana do zarządzania kluczami kont za pośrednictwem usługi Azure Keys.

### Przykład 4: Tworzenie konta magazynu przy użyciu NetworkRuleSet z notacji JSON
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

To polecenie tworzy konto magazynu z właściwością NetworkRuleSet w notacji JSON.

### Przykład 5: Tworzenie konta magazynu z włączoną hierarchiczną przestrzenią nazw.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

To polecenie tworzy konto magazynu z włączoną hierarchiczną przestrzenią nazw.

### Przykład 6: Tworzenie konta magazynu za pomocą uwierzytelniania usług domenowych w usłudze Azure w usłudze Microsoft Files i włączanie dużego udziału plików.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

To polecenie tworzy konto magazynu z uwierzytelnianiem usługi Azure Files w usłudze Azure i umożliwia włączenie dużego udziału plików..

### Przykład 8: Tworzenie konta magazynu za pomocą usługi kolejkowania i tabeli Użyj klucza szyfrowania z zakresem kont.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account
```

To polecenie tworzy konto magazynu z usługą kolejkowania i tabel, korzystając z klucza szyfrowania z zakresem kont, a więc kolejki i tabele będą używać tego samego klucza szyfrowania z obiektem BLOB i usługą plików. Następnie uzyskasz właściwości konta magazynu i wyświetlenie klucza szyfrowania dla kolejki i usługi Table.

## PARAMETRÓW

### -AccessTier
Określa warstwę dostępu konta magazynu tworzonego przez to polecenie cmdlet.
Dopuszczalne wartości tego parametru to: gorące i chłodzone.
W przypadku określenia wartości BlobStorage dla parametru *Kind* należy określić wartość parametru *AccessTier* . Jeśli określisz wartość określającą miejsce do magazynowania dla tego parametru *typu* , nie określaj parametru *AccessTier* .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -EnableAzureActiveDirectoryDomainServicesForFile
Włącz uwierzytelnianie usługi domenowe Active Directory Azure na platformie Azure dla konta magazynu.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHierarchicalNamespace
Wskazuje, czy konto magazynu umożliwia włączenie hierarchicznego obszaru nazw.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Wskazuje, czy konto magazynu umożliwia tylko ruch HTTPS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableLargeFileShare
Wskazuje, czy konto magazynu może obsługiwać duże udziały plików o wydajności większej niż 5 TiB. Po włączeniu konta nie można wyłączyć funkcji. Obecnie obsługiwane tylko dla typów replikacji LRS i ZRS, dzięki czemu konwersje kont na konta z nadmiarowością geograficzną nie będą możliwe. Więcej informacji https://go.microsoft.com/fwlink/?linkid=2086047

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

### -EncryptionKeyTypeForQueue
Ustawianie klucza szyfrowania dla kolejki. Wartość domyślna to usługa.
— Konto: Kolejka zostanie zaszyfrowana przy użyciu klucza szyfrowania z zakresem kont. -Service: kolejka będzie zawsze szyfrowana za pomocą kluczy Service-Managed. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyTypeForTable
Ustawianie klucza szyfrowania dla tabeli. Wartość domyślna to usługa.
- Konto: tabela zostanie zaszyfrowana przy użyciu klucza szyfrowania z zakresem kont. 
- Usługa: tabela zawsze będzie szyfrowana przy użyciu kluczy Service-Managed. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kind
Określa rodzaj konta magazynu tworzonego przez to polecenie cmdlet.
Dopuszczalne wartości tego parametru to:
- Chowan. Ogólne konto magazynu, które obsługuje przechowywanie obiektów blob, tabel, kolejek, plików i dysków.
- StorageV2. Konto magazynu ogólnego celu w wersji 2 (GPv2), które obsługuje obiekty blob, tabele, kolejki, pliki i dyski, z zaawansowanymi funkcjami, takimi jak warstwy danych.
- BlobStorage. Konto magazynu obiektów BLOB obsługujące tylko przechowywanie obiektów BLOB.
- BlockBlobStorage. Blokuj konto magazynu obiektów blob, które obsługuje tylko przechowywanie bloków bloków BLOB.
- FileStorage. Konto magazynu plików obsługujące tylko przechowywanie plików.
Wartość domyślna to StorageV2.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
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
Position: 3
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
NetworkRuleSet jest używana do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych, a także do ustawiania wartości właściwości sieci, takich jak usługi, które mogą pomijać reguły, oraz sposobu obsługi żądań niezgodnych z żadną określoną regułą.

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
- Standard_LRS. Magazyn lokalny-nadmiarowy.
- Standard_ZRS. Miejsce do magazynowania nadmiarowych stref.
- Standard_GRS. Magazyn Geograficznie nadmiarowy.
- Standard_RAGRS. Dostęp do odczytu geograficznie zapasowego miejsca.
- Premium_LRS. Premium miejsce do magazynowania.
- Premium_ZRS. Strefa Premium-nadmiarowe miejsce do magazynowania.
- Standard_GZRS-nadmiarowe miejsce w strefie geograficznej.
- Standard_RAGZRS — dostęp do odczytu Geograficznie nadmiarowy obszar magazynu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze. Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
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
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount

## INFORMACYJN

## LINKI POKREWNE

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)
