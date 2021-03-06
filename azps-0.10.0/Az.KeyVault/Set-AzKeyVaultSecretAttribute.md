---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
ms.openlocfilehash: 719f0676b87cf785785b0adfbfde71ad2a6b965b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891245"
---
# Set-AzKeyVaultSecretAttribute

## STRESZCZENIe
Aktualizuje atrybuty klucza tajnego w magazynie kluczy.

## POLECENIA

```
Set-AzKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzKeyVaultSecretAttribute** aktualizuje atrybuty edytowalne klucza tajnego w magazynie kluczy.

## Przykłady

### Przykład 1: modyfikowanie atrybutów tajności
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

Pierwsze cztery polecenia definiują atrybuty daty wygaśnięcia, NotBefore Data, Tagi i typ kontekstu oraz przechowują atrybuty w zmiennych.

Polecenie ostatnie modyfikuje atrybuty wpisu tajnego o nazwie HR w magazynie kluczy o nazwie ContosoVault, korzystając z przechowywanych zmiennych.

### Przykład 2: usuwanie znaczników i typu zawartości dla wpisu tajnego
```
PS C:\>Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

To polecenie usuwa znaczniki i typ zawartości określonej wersji sekretu o nazwie HR w magazynie kluczy o nazwie contoso.

### Przykład 3: wyłączanie bieżącej wersji kluczy tajnych, których imiona i nazwiska zaczynają się od niej
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzKeyVaultSecretAttribute -Enable $False
```

Pierwsze polecenie zapisuje wartość ciągu contoso w zmiennej $Vault.

Drugie polecenie zapisuje wartość ciągu w zmiennej $Prefix.

W trzecim poleceniu jest używane polecenie cmdlet Get-AzKeyVaultSecret w celu uzyskania kluczy tajnych w określonym magazynie kluczy, a następnie przekazanie tych kluczy tajnych do polecenia cmdlet **WHERE-Object** . Polecenie cmdlet **WHERE-Object** filtruje klucze tajne dla nazw, które zaczynają się od znaków. Polecenie przełączy klucze tajne, które pasują do filtru Set-AzKeyVaultSecretAttribute polecenia cmdlet, co powoduje wyłączenie ich.

### Przykład 4: Ustawianie typu zawartości dla wszystkich wersji klucza tajnego
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzKeyVaultSecretAttribute -ContentType $ContentType
```

Pierwsze trzy polecenia definiują zmienne tekstowe, które mają być używane dla parametrów *magazynname* , *name* i *ContentType* . W czwartym poleceniu jest używane polecenie cmdlet Get-AzKeyVaultKey w celu uzyskania określonych kluczy i przeprzewody klawiszy do polecenia cmdlet Set-AzKeyVaultSecretAttribute w celu ustawienia typu zawartości na wartość XML.

## PARAMETRÓW

### -Type
Określa typ zawartości wpisu tajnego. Jeśli nie określisz tego parametru, nie zmienisz typu zawartości bieżącego klucza tajnego. Aby usunąć istniejący typ zawartości, określ pusty ciąg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### -Enable
Wskazuje, czy włączyć klucz tajny. Określ $False, aby wyłączyć klucz tajny lub $True w celu włączenia klucza tajnego. Jeśli ten parametr nie jest określony, nie ma żadnej zmiany w stanie włączenia lub wyłączenia bieżącego klucza tajnego.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wygasa
Określa datę i godzinę unieważnienia klucza tajnego.

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

### -Name (nazwa)
Określa nazwę wpisu tajnego. To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza tajnego na podstawie nazwy, jaką ten parametr określa, nazwę magazynu kluczy i obecne środowisko.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotBefore
Określa uniwersalny czas koordynowany (UTC), przed którym nie można użyć klucza tajnego.
Jeśli nie określisz tego parametru, nie zmienisz atrybutu NotBefore bieżącego klucza tajnego.

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

### -PassThru
Zwraca obiekt reprezentujący element, z którym pracujesz.
Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.

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
Określa nazwę magazynu kluczy do zmodyfikowania.
To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, którą ten parametr określa, oraz obecnie wybranego środowiska.

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

### -Version
Określa wersję wpisu tajnego.
To polecenie cmdlet konstruuje nazwę FQDN wpisu tajnego na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, tajnej nazwy i tajnej wersji.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
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

### Microsoft. Azure. Commands. model. modeli. Secret
Zwraca wartość Microsoft. Azure. Commands. Stream. models. Secret, jeśli jest określony PassThru. W przeciwnym razie zwraca wartość Nothing.

## INFORMACYJN

## LINKI POKREWNE

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)
