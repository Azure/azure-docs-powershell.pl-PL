---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 7a8c4bc3b875cb9072386784fe1c06730be89405
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050440"
---
# New-AzDiskConfig

## STRESZCZENIe
Tworzy konfigurowalny obiekt dyskowy.

## POLECENIA

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>]
 [-DiskMBpsReadWrite <Int64>] [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzDiskConfig** tworzy konfigurowalny obiekt dyskowy.

## Przykłady

### Przykład 1
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

Pierwsze polecenie tworzy lokalny pusty obiekt dyskowy o rozmiarze 5GB w Standard_LRS typ konta magazynu. Ustawia również typ systemu operacyjnego Windows i włącza ustawienia szyfrowania. Drugie i trzecie polecenia Ustaw klucz szyfrowania dysku i ustawienia klucza szyfrowania kluczy dla obiektu dysk. Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".

### Przykład 2
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
PS C:\> $diskSas = Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DurationInSecond 86400 -Access 'Write'
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ReadyToUpload'
PS C:\> AzCopy /Source:https://myaccount.blob.core.windows.net/mycontainer1 /Dest:$diskSas
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ActiveUpload'
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

Pierwsze polecenie tworzy obiekt dysku lokalnego do przekazania.
Drugie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".
Trzecie polecenie pobiera adres URL dla dysku.
Czwarte polecenie uzyskuje stan dysku.
Jeśli dysk jest w stanie "ReadyToUpload", użytkownik może przekazać dysk z przestrzeni dyskowej BLOB do adresu URL dysków SAS dysku przy użyciu AzCopy.
Podczas przekazywania stan dysku zmieni się na "ActiveUpload".
Ostatnie polecenie odwołuje dostęp do dysku w adresie URL SAS.

### Przykład 3
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

Tworzenie dysku z wersji obrazu galerii udostępnionej.  Identyfikator to identyfikator wersji obrazu galerii udostępnionej. Numer LUN jest potrzebny tylko wtedy, gdy źródłem jest dysk danych.

## PARAMETRÓW

### -Opcja
Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DiskEncryptionKey
Określa obiekt klucza szyfrowania dysku na dysku.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskEncryptionSetId
Określa identyfikator zasobu zestawu ustawień szyfrowania dysku, który ma być używany do włączania szyfrowania w stanie spoczynku.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskIOPSReadOnly
Łączna liczba IOPS, które będą dozwolone na wszystkich maszynach wirtualnych instalujących dysk udostępniony jako tylko do odczytu. Jedna operacja może przekazywać między 4K a 256k bajtami.

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskIOPSReadWrite
Liczba IOPS dozwolonych dla tego dysku; tylko dla dysków UltraSSD można tylko settablecie. Jedna operacja może przekazywać między 4K a 256k bajtami.

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskMBpsReadOnly
"opis": "całkowita przepływność (MB/s), która będzie dozwolona na wszystkich maszynach wirtualnych instalująca dysk udostępniony jako tylko do odczytu. MB/s oznacza, że miliony bajtów na sekundę-MB używa notacji ISO o uprawnieniach 10.

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskMBpsReadWrite
Przepustowość dozwolona dla tego dysku; tylko dla dysków UltraSSD można tylko settablecie. MB/s oznacza, że miliony bajtów na sekundę-MB używa notacji ISO o uprawnieniach 10.

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeGB
Określa rozmiar dysku w GB.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EncryptionSettingsEnabled
Włącz ustawienia szyfrowania.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EncryptionType
Typ klucza służący do szyfrowania danych dysku.  Dostępne wartości: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GalleryImageReference
Obiekt GalleryImageReference.  Wymagane w przypadku tworzenia z obrazu z galerii. Identyfikator będzie identyfikatorem ARM dla udostępnionej wersji obrazu w ramach korekty, z której ma zostać utworzony dysk.
Jeśli źródłem kopii jest jedna z dysków danych w obrazie galerii, wymagana jest jednostka LUN. Jeśli wartość null, dysk systemu operacyjnego obrazu zostanie skopiowany.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HyperVGeneration
Generowanie funkcji hypervisor maszyny wirtualnej. Dotyczy tylko dysków z systemem operacyjnym.  Dozwolone wartości to V1 i v2.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageReference
Określa odwołanie do obrazu na dysku.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyEncryptionKey
Określa klucz szyfrowania klucza na dysku.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Lokalizacja
Określa lokalizację.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxSharesCount
Maksymalna liczba maszyn wirtualnych, które można dołączyć do dysku w tym samym czasie.
Wartość większa niż jedna wskazuje, że dysk może być instalowany jednocześnie z wieloma maszynami wirtualnymi w tym samym czasie.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsType
Określa typ OS.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuName
Określa nazwę SKU konta magazynu.  Dostępne wartości to Standard_LRS, Premium_LRS, StandardSSD_LRS i UltraSSD_LRS.  UltraSSD_LRS można użyć tylko z wartością pustą dla parametru usługi.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceResourceId
Określa identyfikator zasobu źródłowego.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceUri
Określa źródłowy identyfikator URI.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountId
Określa identyfikator konta magazynu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Pary klucz-wartość w formie tabeli skrótów. Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UploadSizeInBytes
Określa rozmiar zawartości przekazanie, łącznie z stopką dysku VHD, gdy opcja ta jest przekazywana.  Ta wartość powinna znajdować się w zakresie od 20972032 (20 MiB + 512 bajtów dla stopki VHD) i 35183298347520 bajtów (32 TiB + 512 bajtów dla stopki VHD).

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Określa listę stref logicznych dla dysku.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. OperatingSystemTypes, Microsoft. Azure. Management. Framework

### System. Int32

### System. String []

### System. Collections. Hashtable

### Microsoft. Azure. Management. COMPUTE. MODELES. ImageDiskReference

### System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndSecretReference

### Microsoft. Azure. Management. COMPUTE. MODELES. KeyVaultAndKeyReference

## WYSYŁA

### Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK

## INFORMACYJN

## LINKI POKREWNE
