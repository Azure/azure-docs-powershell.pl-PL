---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690302
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: fbc2c4cd56da23bef29716800316f479159af148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553263"
---
# Set-AzureKeyVaultKeyAttribute

## STRESZCZENIe
Aktualizuje atrybuty klucza w magazynie kluczy.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureKeyVaultKeyAttribute** aktualizuje atrybuty edytowalne klucza w magazynie kluczy.

## Przykłady

### Przykład 1: Zmodyfikuj klawisz, aby go włączyć, a następnie ustaw datę i Tagi wygasania.
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

Pierwsze polecenie tworzy obiekt **DateTime** przy użyciu polecenia cmdlet **Get-Date** . Ten obiekt Określa godzinę w przyszłości w dwóch latach. Polecenie zapisuje tę datę w zmiennej $Expires.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .

Drugie polecenie tworzy zmienną do przechowywania wartości znaczników o wysokiej ważności i księgowaniu.

Polecenie ostatnie modyfikuje klucz o nazwie ITSoftware. Polecenie włącza klucz, ustawia czas wygaśnięcia w czasie przechowywanym w $Expires i ustawia Tagi przechowywane w $Tags.

### Przykład 2: modyfikowanie klucza w celu usunięcia wszystkich znaczników
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

To polecenie usuwa wszystkie znaczniki dla określonej wersji klucza o nazwie ITSoftware.

## PARAMETRÓW

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

### -Enable
Określa, czy należy włączyć lub wyłączyć klucz. Wartość $True umożliwia włączenie klucza. Wartość $False wyłącza klucz. Jeśli nie podano tego parametru, to polecenie cmdlet nie powoduje zmiany stanu klucza.

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

### -Wygasa
Określa czas wygaśnięcia jako obiekt **DateTime** dla klucza, który jest aktualizowany przez to polecenie cmdlet. W tym parametrze jest używany uniwersalny czas koordynowany (UTC). Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** . Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyOps
Określa tablicę operacji, które można wykonać przy użyciu klucza, który jest dodawany przez to polecenie cmdlet.
Jeśli nie podano tego parametru, można wykonać wszystkie operacje.

Dopuszczalne wartości tego parametru to rozdzielana przecinkami lista podstawowych operacji, które zdefiniowano w specyfikacji klucza internetowego JSON. Wartości te (z uwzględnieniem wielkości liter) są następujące:

- szyfrowane
- Szyfruj
- Pakuj
- odwinięcie
- zapisywania
- sprawdzić
- wykonania
- przywrócenie

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

### -Name (nazwa)
Określa nazwę klucza do zaktualizowania. To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) klucza na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotBefore
Określa czas (w postaci obiektu **DateTime** ), przed którym nie można użyć klucza.
Ten parametr używa czasu UTC.
Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .

```yaml
Type: System.Nullable`1[System.DateTime]
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Magazynname
Określa nazwę magazynu kluczy, w którym to polecenie cmdlet modyfikuje klucz.
To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Określa wersję klucza.
To polecenie cmdlet konstruuje nazwę FQDN klucza na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, nazwy klucza i wersji klucza.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Microsoft. Azure. Commands. platforming. MODELES.

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)
