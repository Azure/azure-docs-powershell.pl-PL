---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: da6460bf0a1126a11345336e4d55c300728bbd66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203842"
---
# Add-AzKeyVaultKey

## SYNOPSIS
Tworzy klucz w magazynie kluczy lub importuje klucz do magazynu kluczy.

## SKŁADNIA

### InteractiveCreate (Default)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveImport
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInteractiveCreate
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInteractiveImport
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectCreate
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectImport
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInputObjectCreate
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInputObjectImport
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdCreate
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdImport
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmResourceIdCreate
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmResourceIdImport
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzKeyVaultKey** tworzy klucz w magazynie kluczy w magazynie kluczy platformy Azure lub importuje klucz do magazynu kluczy.
Użyj tego polecenia cmdlet, aby dodać klucze przy użyciu dowolnej z następujących metod:
- Tworzenie klucza w module zabezpieczeń sprzętu (HSM) w usłudze magazynu kluczy.
- Utwórz klucz w oprogramowaniu w usłudze magazynu kluczy.
- Importowanie klucza z własnego modułu zabezpieczeń sprzętu do hsm w usłudze magazynu kluczy.
- Zaimportuj klucz z pliku pfx na komputerze.
- Importowanie klucza z pliku pfx na komputerze do modułów zabezpieczeń sprzętu (HSM) w usłudze magazynu kluczy.
W przypadku dowolnej z tych operacji można podać atrybuty klucza lub zaakceptować ustawienia domyślne.
Jeśli utworzysz lub zaimportujesz klucz o takiej samej nazwie jak istniejący klucz w magazynie kluczy, klucz oryginalny zostanie zaktualizowany o wartości określone dla nowego klucza. Aby uzyskać dostęp do poprzednich wartości, można użyć specyficznego dla wersji URI dla tej wersji klucza. Aby uzyskać informacje na temat kluczowych wersji i struktury URI, zobacz [Informacje](http://go.microsoft.com/fwlink/?linkid=518560) o kluczach i tajemnicach w dokumentacji interfejsu API REST magazynu kluczy.
Uwaga: Aby zaimportować klucz z własnego modułu zabezpieczeń sprzętowych, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku byok) przy użyciu zestawu narzędzi BYOK magazynu kluczy platformy Azure. Aby uzyskać więcej informacji, zobacz [generuj i przesyłaj klucze HSM-Protected dla magazynu](http://go.microsoft.com/fwlink/?LinkId=522252)kluczy platformy Azure.
Najlepszym rozwiązaniem jest, aby po utworzeniu lub zaktualizowaniu klucza utworzyć jego kopię zapasową, używając polecenia cmdlet Backup-AzKeyVaultKey cmdlet. Nie ma funkcji przywracania, więc jeśli przypadkowo usuniesz klucz lub usuniesz go, a następnie zmienisz zdanie, nie będzie można go odzyskać, chyba że masz jego kopię zapasową, która będzie można przywrócić.

## PRZYKŁADY

### Przykład 1. Tworzenie klucza
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

To polecenie tworzy klucz chroniony oprogramowaniem o nazwie ITSoftware w magazynie kluczy o nazwie Contoso.

### Przykład 2. Tworzenie klucza chronionego przez hsm
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

To polecenie tworzy klucz chroniony modułem HSM w magazynie kluczy o nazwie Contoso.

### Przykład 3. Tworzenie klucza z wartościami innymi niż domyślne
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

Pierwsze polecenie przechowuje wartości do odszyfrowywania i weryfikowania w $KeyOperations danych.
Drugie polecenie tworzy obiekt **DateTime** zdefiniowany w czasie UTC przy użyciu polecenia cmdlet **Get-Date.**
Ten obiekt określa czas za dwa lata. Polecenie przechowuje datę w $Expires zmienną. Aby uzyskać więcej informacji, wpisz `Get-Help Get-Date` .
Trzecie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date.** Ten obiekt określa bieżący czas UTC. Polecenie przechowuje datę w $NotBefore zmienną.
Ostatnie polecenie tworzy klucz o nazwie ITHsmNonDefault, który jest kluczem chronionym przez HSM. To polecenie określa wartości dozwolonych operacji na kluczach przechowywanych $KeyOperations. Polecenie określa czasy dla parametrów *Wygasa i* *NieBefore* utworzonych w poprzednich poleceniach oraz tagów o wysokim poziomie ważności i dla parametrów IT. Nowy klucz zostanie wyłączony. Możesz ją włączyć przy użyciu polecenia cmdlet **Set-AzKeyVaultKey.**

### Przykład 4. Importowanie klucza chronionego przez HSM
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

To polecenie importuje klucz o nazwie ITByok z lokalizacji, która jest określana przez parametr *KeyFilePath.* Importowany klucz jest kluczem chronionym przez hsm.
Aby zaimportować klucz z własnego modułu zabezpieczeń sprzętowych, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku byok) przy użyciu zestawu narzędzi BYOK magazynu kluczy platformy Azure.
Aby uzyskać więcej informacji, zobacz [generuj i przesyłaj klucze HSM-Protected dla magazynu](http://go.microsoft.com/fwlink/?LinkId=522252)kluczy platformy Azure.

### Przykład 5. Importowanie klucza chronionego oprogramowaniem
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Pierwsze polecenie konwertuje ciąg na bezpieczny ciąg za pomocą polecenia cmdlet **ConvertTo-SecureString,** a następnie zapisuje ten ciąg w $Password danych. Aby uzyskać więcej informacji, wpisz `Get-Help
ConvertTo-SecureString` .
Drugie polecenie tworzy hasło oprogramowania w magazynie kluczy Contoso. To polecenie określa lokalizację klucza i hasło przechowywane w programie $Password.

### Przykład 6. Importowanie klucza i przypisywanie atrybutów
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

Pierwsze polecenie konwertuje ciąg na bezpieczny ciąg za pomocą polecenia cmdlet **ConvertTo-SecureString,** a następnie zapisuje ten ciąg w $Password danych.
Drugie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date,** a następnie zapisuje ten obiekt w $Expires danych.
Trzecie polecenie tworzy zmienną $tags, aby ustawiać tagi o wysokim poziomie ważności i it.
Ostatnie polecenie importuje klucz jako klucz HSM z określonej lokalizacji. To polecenie określa czas wygaśnięcia przechowywany w programie $Expires hasło przechowywane w programie $Password i stosuje tagi przechowywane w $tags.

### Przykład 7. Generowanie klucza programu Exchange (KEK) dla funkcji "bring your own key" (BYOK)

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

Generuje klucz (nazywany kluczem programu Exchange ). KEK musi być kluczem RSA-HSM, który ma tylko operację klucza importu. Tylko wersja SKU magazynu kluczy Premium obsługuje klucze RSA-HSM.
Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys

## PARAMETERS

### -CurveName
Określa nazwę krzywej kryptografii krzywej wielokropka. Ta wartość jest prawidłowa, gdy typ_klucza to EC.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveCreate, InputObjectImport, HsmInputObjectCreate, ResourceIdImport, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### — miejsce docelowe
Określa, czy należy dodać klucz jako klucz chroniony oprogramowaniem, czy jako klucz chroniony przez HSM w usłudze magazynu kluczy.
Prawidłowe wartości to: HSM i Software.
Uwaga: Aby użyć funkcji HSM jako miejsca docelowego, należy mieć magazyn kluczy obsługujący hsm. Aby uzyskać więcej informacji o warstwach usług i możliwościach dla magazynu kluczy platformy Azure, zobacz witrynę internetową Ceny magazynu kluczy [platformy Azure.](http://go.microsoft.com/fwlink/?linkid=512521)
Ten parametr jest wymagany podczas tworzenia nowego klucza. W przypadku importowania klucza za pomocą parametru *KeyFilePath* ten parametr jest opcjonalny:
- Jeśli ten parametr nie zostanie określony, a to polecenie cmdlet importuje klucz z rozszerzeniem nazwy pliku byok, importuje ten klucz jako klucz chroniony przez moduł HSM. Polecenie cmdlet nie może zaimportować tego klucza jako klucza chronionego oprogramowaniem.
- Jeśli nie określisz tego parametru, a to polecenie cmdlet zaimresuje klucz z rozszerzeniem nazwy pliku pfx, zaimresuje ten klucz jako klucz chroniony oprogramowaniem.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - Wyłącz
Wskazuje, że dodajeny klucz jest ustawiony na początkowy stan wyłączenia. Próba użycia klucza nie powiedzie się. Użyj tego parametru, jeśli zamierzasz włączyć wstępnie klucze później.

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

### — Wygasa
Określa czas wygaśnięcia , jako obiekt **DateTime,** klucza, który dodaje to polecenie cmdlet. Ten parametr używa uniwersalnego czasu koordynowanej (UTC). Aby uzyskać obiekt **DateTime,** użyj polecenia cmdlet **Get-Date.** Aby uzyskać więcej informacji, wpisz `Get-Help Get-Date` . Jeśli nie określisz tego parametru, klucz nie wygaśnie.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - HsmName
Nazwa HSM. Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - HsmObject
Obiekt HSM.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -HsmResourceId
Identyfikator zasobu hsm.

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Obiekt magazynu.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyFilePassword
Określa hasło dla zaimportowanego pliku jako obiektu **SecureString.** Aby uzyskać obiekt **SecureString,** użyj polecenia cmdlet **ConvertTo-SecureString.** Aby uzyskać więcej informacji, wpisz `Get-Help ConvertTo-SecureString` . To hasło należy określić, aby zaimportować plik z rozszerzeniem nazwy pliku pfx.

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
Określa ścieżkę pliku lokalnego zawierającego klucz materiałów importowanych przez to polecenie cmdlet.
Prawidłowe rozszerzenia nazw plików to byok i pfx.
- Jeśli plik jest plikiem byok, klucz jest automatycznie chroniony przez moduły HSM po zakończeniu importowania i nie można zastąpić tego ustawienia domyślnego.
- Jeśli plik jest plikiem pfx, klucz jest automatycznie chroniony przez oprogramowanie po zaimportowaniu. Aby zastąpić to ustawienie domyślne, należy ustawić dla parametru *Destination* wartość HSM tak, aby klucz był chroniony przez hsm.
Określenie tego parametru jest *parametrem docelowym* opcjonalnym.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
Określa tablicę operacji, które można wykonać przy użyciu klucza, który dodaje to polecenie cmdlet.
Jeśli nie określisz tego parametru, będzie można wykonywać wszystkie operacje.
Dopuszczalne wartości dla tego parametru to rozdzielona przecinkami lista operacji klucza zgodnie ze specyfikacją klucza sieci [Web JSON (JWK):](http://go.microsoft.com/fwlink/?LinkID=613300)
- szyfrowanie
- odszyfrowywanie
- wrapKey
- unwrapKey
- znak
- weryfikuj
- importowanie (dotyczy tylko KEK, zobacz przykład 7)

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType
Określa typ klucza tego klucza. Podczas importowania kluczy BYOK wartość domyślna to "RSA".

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę klucza do dodania do magazynu kluczy. To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, która jest określana przez ten parametr, nazwy magazynu kluczy i bieżącego środowiska. Nazwa musi być ciągiem o długości od 1 do 63 znaków, który zawiera tylko wartości 0-9, a-z, A-Z i - (symbol kreski).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Określa czas jako obiekt **DateTime,** przed którym nie można użyć klucza. Ten parametr używa czasu UTC. Aby uzyskać obiekt **DateTime,** użyj polecenia cmdlet **Get-Date.** Jeśli nie określisz tego parametru, klucz może zostać użyty natychmiast.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu magazynu.

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Rozmiar
Rozmiar klucza RSA w bitach. Jeśli nie zostanie określona, usługa udostępni bezpieczny domyślny standard.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Tag
Pary klucz-wartość w postaci tabeli skrótu. Na przykład: @{key0="value0";key1=$null;key2="wartość2"}

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

### -VaultName
Określa nazwę magazynu kluczy, do którego to polecenie cmdlet dodaje klucz. To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, która jest określana przez ten parametr i bieżącego środowiska.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey

## NOTATKI

## LINKI POKREWNE

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Set-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)
