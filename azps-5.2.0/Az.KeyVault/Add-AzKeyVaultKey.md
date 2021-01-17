---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 6cea7f2584de3a27be2cee36c3f32fd792564160
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346690"
---
# Add-AzKeyVaultKey

## STRESZCZENIe
Tworzy klucz w magazynie kluczy lub importuje klucz do magazynu kluczy.

## POLECENIA

### InteractiveCreate (domyślny)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveImport
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
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
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
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
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
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

## Opis
Polecenie cmdlet **Add-AzKeyVaultKey** tworzy klucz w magazynie kluczy w magazynie kluczy Azure lub importuje klucz do magazynu kluczy.
Za pomocą tego polecenia cmdlet można dodawać klucze przy użyciu dowolnej z poniższych metod:
- Utwórz klucz w sprzęcie sprzętowym modułu zabezpieczeń (HSM) w usłudze Magazyn kluczy.
- Utwórz klucz w oprogramowaniu w usłudze Magazyn kluczy.
- Zaimportuj klucz z własnego sprzętu sprzętowego modułu zabezpieczeń (HSM), aby HSMs w usłudze magazynu kluczy.
- Importowanie klucza z pliku PFX na komputerze.
- Zaimportuj klucz z pliku PFX na komputerze do modułów zabezpieczeń sprzętowych (HSMs) w usłudze Magazyn kluczy.
W przypadku dowolnej z tych operacji możesz podać atrybuty klucza lub zaakceptować ustawienia domyślne.
W przypadku utworzenia lub zaimportowania klucza o takiej samej nazwie jak istniejący klucz w magazynie kluczy oryginalny klucz zostanie zaktualizowany o wartości określone dla nowego klucza. Dostęp do poprzednich wartości można uzyskać przy użyciu identyfikatora URI specyficznego dla wersji dla tej wersji klucza. Aby uzyskać informacje na temat wersji kluczowych i struktury identyfikatora URI, zobacz [Informacje o kluczach i hasłach](http://go.microsoft.com/fwlink/?linkid=518560) w dokumentacji interfejsu API w magazynie kluczy.
Uwaga: Aby zaimportować klucz z własnego sprzętowego modułu zabezpieczeń, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku BYOK) przy użyciu narzędzia BYOK magazynu kluczy platformy Azure. Aby uzyskać więcej informacji, zobacz [sposób generowania i transferowania kluczy HSM-Protected dla magazynu kluczy platformy Azure](http://go.microsoft.com/fwlink/?LinkId=522252).
Najlepszym rozwiązaniem jest wykonanie kopii zapasowej klucza po jego utworzeniu lub zaktualizowaniu za pomocą polecenia cmdlet Backup-AzKeyVaultKey. Nie ma żadnych funkcji usuwania zmian, więc jeśli przypadkowo usuniesz klucz lub usuniesz go, a następnie zmienisz zdanie, nie będzie można odzyskać klucza, chyba że masz kopię zapasową, którą możesz przywrócić.

## Przykłady

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

To polecenie tworzy klucz chroniony oprogramowaniem o nazwie ITSoftware w magazynie kluczy o nazwie contoso.

### Przykład 2: Tworzenie klucza chronionego przy użyciu modułu HSM
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

To polecenie tworzy klucz chroniony przez HSM w magazynie kluczy o nazwie contoso.

### Przykład 3: Tworzenie klucza z wartościami niedomyślnymi
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

Pierwsze polecenie zapisuje wartości w postaci odszyfrowania i weryfikacji w zmiennej $KeyOperations.
Drugie polecenie tworzy obiekt **DateTime** , zdefiniowany w formacie UTC, przy użyciu polecenia cmdlet **Get-Date** .
Ten obiekt Określa godzinę w przyszłości w dwóch latach. Polecenie zapisuje tę datę w zmiennej $Expires. Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .
Trzecie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** . Ten obiekt określa bieżący czas UTC. Polecenie zapisuje tę datę w zmiennej $NotBefore.
Ostatnie polecenie tworzy klucz o nazwie ITHsmNonDefault, który jest kluczem chronionym przy użyciu modułu HSM. W poleceniu są określone wartości dozwolonych kluczowych operacji przechowywanych $KeyOperations. Polecenie określa czasy, w jakich parametry *Expires* i *NotBefore* zostały utworzone w poprzednich poleceniach, oraz znaczniki wysokiej wagi i. Nowy klucz jest wyłączony. Możesz ją włączyć za pomocą polecenia cmdlet **Set-AzKeyVaultKey** .

### Przykład 4: Importowanie klucza chronionego przez HSM
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

To polecenie importuje klucz o nazwie ITByok z lokalizacji, w której określono parametr Key *FilePath* . Importowany klucz jest kluczem chronionym przy użyciu modułu HSM.
Aby zaimportować klucz z własnego sprzętowego modułu zabezpieczeń, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku BYOK) przy użyciu przybornika kluczy usługi Azure BYOK.
Aby uzyskać więcej informacji, zobacz [sposób generowania i transferowania kluczy HSM-Protected dla magazynu kluczy platformy Azure](http://go.microsoft.com/fwlink/?LinkId=522252).

### Przykład 5: Importowanie klucza chronionego oprogramowaniem
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

Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Password. Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .
Drugie polecenie tworzy hasło oprogramowania w magazynie kluczy contoso. Polecenie określa lokalizację klucza i hasło przechowywane w $Password.

### Przykład 6: Importowanie klucza i przypisywanie atrybutów
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

Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Password.
Drugie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** , a następnie zapisuje ten obiekt w zmiennej $Expires.
Trzecie polecenie tworzy zmienną $tags, aby ustawić znaczniki wysokiej wagi i je.
Polecenie ostatnie importuje klucz jako klucz HSM z określonej lokalizacji. Polecenie określa czas wygaśnięcia przechowywany w $Expires i hasło przechowywane w $Password i stosuje Tagi przechowywane w $tags.

### Przykład 7: generowanie klucza wymiany kluczy (KEK) dla funkcji "Dobierz własny klucz" (BYOK)

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

Generuje klucz (nazywany kluczem wymiany kluczy (KEK)). KEK musi być kluczem modułu RSA-HSM, który ma tylko operację importowania klucza. Tylko klucze modułu HSM RSA obsługują tylko Magazyn kluczy Premium.
Więcej informacji znajdziesz w sekcji https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys

## PARAMETRÓW

### -Zakrętname
Określa nazwę krzywej kryptografii krzywej eliptycznej, która jest prawidłowa, gdy właściwość KeyType ma wartość EC.

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -Miejsce docelowe
Określa, czy chcesz dodać ten klucz jako klucz chroniony oprogramowaniem, czy klucz chroniony HSM w usłudze magazynu kluczy.
Prawidłowe wartości to: HSM i Software.
Uwaga: Aby używać modułu HSM jako miejsca docelowego, musisz mieć kluczowy magazyn obsługujący HSMs. Aby uzyskać więcej informacji na temat warstw usług i funkcji magazynu kluczy platformy Azure, zobacz [witrynę sieci Web usługi Azure Key](http://go.microsoft.com/fwlink/?linkid=512521)about.
Ten parametr jest wymagany podczas tworzenia nowego klucza. Jeśli importujesz klucz za pomocą parametru *FilePath* , ten parametr jest opcjonalny:
- Jeśli ten parametr nie jest określony, a polecenie cmdlet powoduje zaimportowanie klucza z rozszerzeniem nazwy pliku BYOK, powoduje to zaimportowanie tego klucza jako klucza chronionego przy użyciu modułu HSM. Polecenie cmdlet nie może zaimportować tego klucza jako klucza chronionego oprogramowaniem.
- Jeśli ten parametr nie jest określony, a polecenie cmdlet spowoduje zaimportowanie klucza o rozszerzeniu nazwy pliku PFX, program zaimportuje klucz jako klucz chroniony oprogramowaniem.

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

### -Disable
Wskazuje, że dodawany klawisz jest ustawiony na początkowy stan wyłączony. Każda próba użycia tego klawisza zakończy się niepowodzeniem. Tego parametru należy użyć, jeśli wstępnie załadowano klucze, które mają być później włączone.

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

### -Wygasa
Określa czas wygaśnięcia jako obiekt **DateTime** dla klucza, który jest dodawany przez to polecenie cmdlet. W tym parametrze jest używany uniwersalny czas koordynowany (UTC). Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** . Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` . Jeśli nie określisz tego parametru, klucz nie wygasa.

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

### -HsmName
Nazwa modułu HSM. Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.

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

### -HsmObject
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
Identyfikator zasobu modułu HSM.

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

### -Inputobject
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
Określa hasło importowanego pliku jako obiekt **SecureString** . Aby uzyskać obiekt **SecureString** , użyj polecenia cmdlet **ConvertTo-SecureString** . Aby uzyskać więcej informacji, wpisz tekst `Get-Help ConvertTo-SecureString` . Musisz określić to hasło, aby zaimportować plik z rozszerzeniem nazwy pliku PFX.

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

### -FilePath
Określa ścieżkę pliku lokalnego zawierającego kluczowe materiały importowane przez to polecenie.
Prawidłowe rozszerzenia nazw plików to. BYOK i. pfx.
- Jeśli plik jest plikiem BYOK, po zakończeniu importu klucz jest automatycznie chroniony przez HSMs i nie można zastąpić tego ustawienia domyślnego.
- Jeśli plik jest plikiem pfx, po zakończeniu importowania klucz jest automatycznie chroniony przez oprogramowanie. Aby zastąpić to ustawienie domyślne, ustaw parametr *lokalizacja_docelowa* na HSM, tak aby klucz był chroniony za pomocą modułu HSM.
Po określeniu tego parametru parametr *docelowy* jest opcjonalny.

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
Określa tablicę operacji, które można wykonać przy użyciu klucza, który jest dodawany przez to polecenie cmdlet.
Jeśli nie podano tego parametru, można wykonać wszystkie operacje.
Dopuszczalne wartości tego parametru to rozdzielana przecinkami lista podstawowych operacji, które zdefiniowano w [specyfikacji klucza internetowego JSON (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300):
- szyfrowane
- Szyfruj
- wrapKey
- unwrapKey
- zapisywania
- sprawdzić
- Importowanie (tylko w przypadku KEK, zobacz przykład 7)

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
Określa typ klucza dla tego klucza.

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

### -Name (nazwa)
Określa nazwę klucza, który ma zostać dodany do magazynu kluczy. To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska. Nazwa musi zawierać ciąg od 1 do 63 znaków, który zawiera tylko 0-9, a-z, a-Z i-(symbol kreski).

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
Określa czas (w postaci obiektu **DateTime** ), przed którym nie można użyć klucza. Ten parametr używa czasu UTC. Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** . Jeśli ten parametr nie jest określony, klucz może być natychmiast wykorzystany.

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

### -Size
Rozmiar klucza RSA w bitach. Jeśli nie zostanie określona, usługa będzie dostarczać bezpieczne ustawienia domyślne.

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

### -Tag
Pary klucz-wartość w formie tabeli skrótów. Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}

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

### -Magazynname
Określa nazwę magazynu kluczy, do którego jest dodawany klucz polecenia. To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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

### Microsoft. Azure. Commands. platforming. models. PSKeyVault

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. platforming. models. PSKeyVaultKey

## INFORMACYJN

## LINKI POKREWNE

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Set-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)
