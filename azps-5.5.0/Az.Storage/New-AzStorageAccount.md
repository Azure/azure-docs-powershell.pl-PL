---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0e1243765064717c6e0030b437c07a176a232f44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195771"
---
# New-AzStorageAccount

## SYNOPSIS
Tworzy konto magazynu.

## SKŁADNIA

### AzureActiveDirectoryDomainServicesForFile (domyślne)
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### ActiveDirectoryDomainServicesForFile
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzStorageAccount** tworzy konto usługi Azure Storage.

## PRZYKŁADY

### Przykład 1. Tworzenie konta magazynu
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

To polecenie tworzy konto magazynu dla nazwy grupy zasobów MyResourceGroup.

### Przykład 2. Tworzenie konta magazynu obiektów blob przy użyciu obiektów BlobStorage Kind i hot AccessTier
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

To polecenie tworzy konto magazynu obiektów blob, które z obiektami BlobStorage Kind i hot AccessTier

### Przykład 3. Utwórz konto magazynu przy użyciu urządzenia Kind StorageV2, a następnie wygeneruj i przypisz tożsamość dla usługi Azure KeyVault.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

To polecenie tworzy konto magazynu z magazynem typu V2.  Generuje ona również i przypisuje tożsamość, za pomocą których można zarządzać kluczami kont za pośrednictwem usługi Azure KeyVault.

### Przykład 4. Tworzenie konta magazynu za pomocą zestawu NetworkRuleSet z JSON
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

To polecenie tworzy konto magazynu, które ma właściwość NetworkRuleSet z JSON

### Przykład 5. Tworzenie konta magazynu z włączoną hierarchiczną przestrzenią nazw.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

To polecenie tworzy konto magazynu z włączoną hierarchiczną przestrzenią nazw.

### Przykład 6. Tworzenie konta magazynu przy użyciu usługi Azure Files AAD DS Authentication i włączanie dużego udziału plików.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

To polecenie umożliwia utworzenie konta magazynu z uwierzytelnianiem AAD DS plików platformy Azure i włączenie dużego udziału plików.

### Przykład 7. Tworzenie konta magazynu z włączym uwierzytelnianiem usługi domenowej Active Directory w plikach.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

To polecenie powoduje utworzenie konta magazynu z możliwością uwierzytelniania usługi domenowej Active Directory z plikiami.

### Przykład 8. Tworzenie konta magazynu przy użyciu klucza szyfrowania z zakresu konta i wymaganego szyfrowania infrastruktury przy użyciu usługi kolejki i usługi tabel.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

To polecenie tworzy konto magazynu z kluczem szyfrowania w zakresie konta i usługą tabel i wymagać szyfrowania infrastruktury, więc kolejka i tabela będą używać tego samego klucza szyfrowania z usługą obiektów blob i plików, a usługa zastosuje pomocniczą warstwę szyfrowania z kluczami zarządzanymi platformy dla danych w spoczynku.
Następnie uzyskaj właściwości konta magazynu i wyświetl typ klucza szyfrowania usługi kolejki i tabeli oraz wartość RequireInfrastructureEncryption.

### Przykład 9. Tworzenie konta MinimumTlsVersion i AllowBlobPublicAccess
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

Polecenie utwórz konto z wartościami MinimumTlsVersion i AllowBlobPublicAccess, a następnie pokaż 2 właściwości utworzonego konta. 

### Przykład 10. Tworzenie konta magazynu z ustawieniem RoutingPreference
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

To polecenie tworzy konto magazynu z ustawieniem RoutingPreference: PublishMicrosoftEndpoint i PublishInternetEndpoint jako prawda oraz RoutingChoice jako MicrosoftRouting.

## PARAMETERS

### -AccessTier
Określa warstwę dostępu dla konta magazynu, które tworzy to polecenie cmdlet.
Dopuszczalne wartości dla tego parametru to: Hot (Hot) i Cool (Cool).
Jeśli dla parametru *Kind* określisz wartość parametru BlobStorage, musisz określić wartość *parametru AccessTier.* W przypadku określenia wartości parametru Storage (Magazyn) dla tego *parametru nie* należy określać *parametru AccessTier.*

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

### -ActiveDirectoryAzureStorageSid
Określa identyfikator zabezpieczeń (SID) dla magazynu platformy Azure. Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainGuid
Określa identyfikator GUID domeny. Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainName
Określa domenę podstawową, dla których autorytatywny jest serwer DNS usługi AD. Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainSid
Określa identyfikator zabezpieczeń (SID). Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryForestName
Określa las usługi Active Directory do uzyskania. Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryNetBiosDomainName
Określa nazwę domeny NetBIOS. Ten parametr musi zostać ustawiony, gdy parametr -EnableActiveDirectoryDomainServicesForFile ma wartość true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowBlobPublicAccess
Zezwalaj na dostęp publiczny do wszystkich obiektów blob lub kontenerów na koncie magazynu. Domyślna interpretacja dotyczy tej właściwości.

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

### — AsJob
Uruchamianie polecenia cmdlet w tle

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
Wygeneruj i przypisz nowe konto magazynu Identity do tego konta magazynu do używania z usługami zarządzania kluczami, na przykład Azure KeyVault.

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
Wartość domyślna to Magazyn.

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

### -EnableActiveDirectoryDomainServicesForFile
Włącz uwierzytelnianie usługi domenowej Active Directory w plikach Azure dla konta magazynu.

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAzureActiveDirectoryDomainServicesForFile
Włącz uwierzytelnianie usługi domen usługi Azure Active Directory dla konta magazynu.

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHierarchicalNamespace
Wskazuje, czy konto magazynu umożliwia korzystanie z hierarchicznej przestrzeni nazw.

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
Wskazuje, czy konto magazynu może obsługiwać duże udziały plików o pojemności większej niż 5 tib. Po włączeniu konta nie można wyłączyć tej funkcji. Obecnie obsługiwane są tylko typy replikacji LRS i ZRS, przez co konwersja kont na geograficznie nadmiarowe konta nie będzie możliwa. Dowiedz się więcej w https://go.microsoft.com/fwlink/?linkid=2086047

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
Ustaw typ klucza szyfrowania dla kolejki. Wartość domyślna to Service (Usługa).
-Konto: Kolejka zostanie zaszyfrowana przy użyciu klucza szyfrowania z zakresu konta. -Service: Kolejka zawsze będzie zaszyfrowana za pomocą Service-Managed kluczy. 

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
Ustaw typ klucza szyfrowania dla tabeli. Wartość domyślna to Service (Usługa).
- Konto: Tabela zostanie zaszyfrowana przy użyciu klucza szyfrowania z zakresu konta. 
- Usługa: Tabela będzie zawsze zaszyfrowana przy Service-Managed kluczach. 

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

### — Rodzaj
Określa rodzaj konta magazynu, które tworzy to polecenie cmdlet.
Dopuszczalne wartości dla tego parametru to:
- Miejsce do magazynowania. Konto magazynu ogólnego przeznaczenia, które obsługuje magazyn obiektów blob, tabel, kolejek, plików i dysków.
- StorageV2. Konto magazynu ogólnego przeznaczenia w wersji 2 (GPv2), które obsługuje obiekty blob, tabele, kolejki, pliki i dyski, z zaawansowanymi funkcjami, na przykład warstwami danych.
- BlobStorage. Konto magazynu obiektów blob, które obsługuje tylko magazyn obiektów blob.
- BlockBlobStorage. Blokuj konto magazynu obiektów blob, które obsługuje tylko magazyn obiektów blob blokowych.
- FileStorage. Konto magazynu plików, które obsługuje tylko przechowywanie plików.
Wartość domyślna to StorageV2.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Określa lokalizację konta magazynu do utworzenia.

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

### -MinimumTlsVersion
Minimalna wersja TLS, która jest dozwolona w żądaniach przechowywania. Domyślna interpretacja tej właściwości to TLS 1.0.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę konta magazynu do utworzenia.

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
Zestaw NetworkRuleSet służy do definiowania zestawu reguł konfiguracji dla zapór i sieci wirtualnych, a także do określania wartości właściwości sieciowych, takich jak usługi mogące pomijać reguły i sposób obsługi żądań, które nie są zgodne z żadnymi zdefiniowanymi regułami.

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

### -PublishInternetEndpoint
Wskazuje, czy punkty końcowe magazynu routingu internetowego mają zostać opublikowane.

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

### -PublishMicrosoftEndpoint
Wskazuje, czy punkty końcowe magazynu routingu firmy Microsoft mają zostać opublikowane.

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

### -ResourceGroupName
Określa nazwę grupy zasobów, w której chcesz dodać konto magazynu.

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

### - RoutingChoice
Wybór routingu określa rodzaj routingu sieciowego wybierany przez użytkownika. Możliwe wartości: "MicrosoftRouting", "InternetRouting"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKUName
Określa nazwę sKU konta magazynu, które tworzy to polecenie cmdlet.
Dopuszczalne wartości dla tego parametru to:
- Standard_LRS. Lokalnie nadmiarowa przestrzeń dyskowa.
- Standard_ZRS. Nadmiarowa przestrzeń dyskowa bez stref.
- Standard_GRS. Magazyn nadmiarowy geograficznie.
- Standard_RAGRS. Odczytywanie nadmiarowej geoprzesyłki dostępu.
- Premium_LRS. Premium lokalnie nadmiarowe miejsce do magazynowania.
- Premium_ZRS. Nadmiarowa przestrzeń dyskowa premium.
- Standard_GZRS — nadmiarowa geograficznie nadmiarowa przestrzeń dyskowa bez stref.
- Standard_RAGZRS — odczyt nadmiarowy geograficznie nadmiarowy magazyn strefy.

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

### — Tag
Pary klucz-wartość w postaci tabeli skrótów ustawionej jako tagi na serwerze. Na przykład: @{key0="value0";key1=$null;key2="wartość2"}

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
Wskazuje, czy należy włączyć pośrednie sprawdzanie poprawności CName.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## NOTATKI

## LINKI POKREWNE

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)
