---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: b01ed80385726660198d3f6fbb20ab1e5ec57dfe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893065"
---
# Add-AzKeyVaultKey

## STRESZCZENIe
Tworzy klucz w magazynie kluczy lub importuje klucz do magazynu kluczy.

## POLECENIA

### Utwórz (domyślne)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Przywoz
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
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

W przypadku utworzenia lub zaimportowania klucza o takiej samej nazwie jak istniejący klucz w magazynie kluczy oryginalny klucz zostanie zaktualizowany o wartości określone dla nowego klucza. Dostęp do poprzednich wartości można uzyskać przy użyciu identyfikatora URI specyficznego dla wersji dla tej wersji klucza. Aby uzyskać informacje na temat wersji kluczowych i struktury identyfikatora URI, zobacz [Informacje o kluczach andSecrets](http://go.microsoft.com/fwlink/?linkid=518560) w dokumentacji interfejsu API w magazynie kluczy.

Uwaga: Aby zaimportować klucz z własnego sprzętowego modułu zabezpieczeń, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku BYOK) przy użyciu narzędzia BYOK magazynu kluczy platformy Azure. Aby uzyskać więcej informacji, zobacz [sposób generowania i transferowania kluczy HSM-Protected dla magazynu kluczy platformy Azure](http://go.microsoft.com/fwlink/?LinkId=522252).

Najlepszym rozwiązaniem jest wykonanie kopii zapasowej klucza po jego utworzeniu lub zaktualizowaniu za pomocą polecenia cmdlet Backup-AzKeyVaultKey. Nie ma żadnych funkcji usuwania zmian, więc jeśli przypadkowo usuniesz klucz lub usuniesz go, a następnie zmienisz zdanie, nie będzie można odzyskać klucza, chyba że masz kopię zapasową, którą możesz przywrócić.

## Przykłady

### Przykład 1. Tworzenie klucza
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

To polecenie tworzy klucz chroniony oprogramowaniem o nazwie ITSoftware w magazynie kluczy o nazwie contoso.

### Przykład 2: Tworzenie klucza chronionego przy użyciu modułu HSM
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

To polecenie tworzy klucz chroniony przez HSM w magazynie kluczy o nazwie contoso.

### Przykład 3: Tworzenie klucza z wartościami niedomyślnymi
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

Pierwsze polecenie zapisuje wartości w postaci odszyfrowania i weryfikacji w zmiennej $KeyOperations.

Drugie polecenie tworzy obiekt **DateTime** , zdefiniowany w formacie UTC, przy użyciu polecenia cmdlet **Get-Date** .
Ten obiekt Określa godzinę w przyszłości w dwóch latach. Polecenie zapisuje tę datę w zmiennej $Expires. Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .

Trzecie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** . Ten obiekt określa bieżący czas UTC. Polecenie zapisuje tę datę w zmiennej $NotBefore.

Ostatnie polecenie tworzy klucz o nazwie ITHsmNonDefault, który jest kluczem chronionym przy użyciu modułu HSM. W poleceniu są określone wartości dozwolonych kluczowych operacji przechowywanych $KeyOperations. Polecenie określa czasy, w jakich parametry *Expires* i *NotBefore* zostały utworzone w poprzednich poleceniach, oraz znaczniki wysokiej wagi i. Nowy klucz jest wyłączony. Możesz ją włączyć za pomocą polecenia cmdlet **Set-AzKeyVaultKey** .

### Przykład 4: Importowanie klucza chronionego przez HSM
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

To polecenie importuje klucz o nazwie ITByok z lokalizacji, w której określono parametr Key *FilePath* . Importowany klucz jest kluczem chronionym przy użyciu modułu HSM.

Aby zaimportować klucz z własnego sprzętowego modułu zabezpieczeń, musisz najpierw wygenerować pakiet BYOK (plik z rozszerzeniem nazwy pliku BYOK) przy użyciu przybornika kluczy usługi Azure BYOK.
Aby uzyskać więcej informacji, zobacz [sposób generowania i transferowania kluczy HSM-Protected dla magazynu kluczy platformy Azure](http://go.microsoft.com/fwlink/?LinkId=522252).

### Przykład 5: Importowanie klucza chronionego oprogramowaniem
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Password. Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .

Drugie polecenie tworzy hasło oprogramowania w magazynie kluczy contoso. Polecenie określa lokalizację klucza i hasło przechowywane w $Password.

### Przykład 6: Importowanie klucza i przypisywanie atrybutów
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

Pierwsze polecenie konwertuje ciąg na ciąg w bezpiecznym ciągu przy użyciu polecenia cmdlet **ConvertTo-SecureString** , a następnie zapisuje ten ciąg w zmiennej $Password.

Drugie polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** , a następnie zapisuje ten obiekt w zmiennej $Expires.

Trzecie polecenie tworzy zmienną $tags, aby ustawić znaczniki wysokiej wagi i je.

Polecenie ostatnie importuje klucz jako klucz HSM z określonej lokalizacji. Polecenie określa czas wygaśnięcia przechowywany w $Expires i hasło przechowywane w $Password i stosuje Tagi przechowywane w $tags.

## PARAMETRÓW

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

### -Miejsce docelowe
Określa, czy chcesz dodać ten klucz jako klucz chroniony oprogramowaniem, czy klucz chroniony HSM w usłudze magazynu kluczy.
Prawidłowe wartości to: HSM i Software.

Uwaga: Aby używać modułu HSM jako miejsca docelowego, musisz mieć kluczowy magazyn obsługujący HSMs. Aby uzyskać więcej informacji na temat warstw usług i funkcji magazynu kluczy platformy Azure, zobacz [witrynę sieci Web usługi Azure Key](http://go.microsoft.com/fwlink/?linkid=512521)about.

Ten parametr jest wymagany podczas tworzenia nowego klucza. Jeśli importujesz klucz za pomocą parametru *FilePath* , ten parametr jest opcjonalny:

- Jeśli ten parametr nie jest określony, a polecenie cmdlet powoduje zaimportowanie klucza z rozszerzeniem nazwy pliku BYOK, powoduje to zaimportowanie tego klucza jako klucza chronionego przy użyciu modułu HSM. Polecenie cmdlet nie może zaimportować tego klucza jako klucza chronionego oprogramowaniem.

- Jeśli ten parametr nie jest określony, a polecenie cmdlet spowoduje zaimportowanie klucza o rozszerzeniu nazwy pliku PFX, program zaimportuje klucz jako klucz chroniony oprogramowaniem.

```yaml
Type: String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Import
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
Type: SwitchParameter
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
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyFilePassword
Określa hasło importowanego pliku jako obiekt **SecureString** . Aby uzyskać obiekt **SecureString** , użyj polecenia cmdlet **ConvertTo-SecureString** . Aby uzyskać więcej informacji, wpisz tekst `Get-Help ConvertTo-SecureString` . Musisz określić to hasło, aby zaimportować plik z rozszerzeniem nazwy pliku PFX.

```yaml
Type: SecureString
Parameter Sets: Import
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
Type: String
Parameter Sets: Import
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

- Szyfrowane
- Szyfruj
- Pakuj
- Odwinięcie
- Zapisywania
- Sprawdzić

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę klucza, który ma zostać dodany do magazynu kluczy. To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska. Nazwa musi zawierać ciąg od 1 do 63 znaków, który zawiera tylko 0-9, a-z, a-Z i-(symbol kreski).

```yaml
Type: String
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
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Pary klucz-wartość w formie tabeli skrótów. Na przykład:

@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Magazynname
Określa nazwę magazynu kluczy, do którego jest dodawany klucz polecenia. To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. platforming. MODELES.

## INFORMACYJN

## LINKI POKREWNE

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Set-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)
