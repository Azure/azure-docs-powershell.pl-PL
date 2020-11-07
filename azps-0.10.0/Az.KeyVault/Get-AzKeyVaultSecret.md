---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: b14e97ba09cba70a9ec571b2fbf1273de7157930
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893042"
---
# Get-AzKeyVaultSecret

## STRESZCZENIe
Pobiera klucze tajne w magazynie kluczy.

## POLECENIA

### ByVaultName (domyślny)
```
Get-AzKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretName
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretVersions
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedSecrets
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzKeyVaultSecret** pobiera klucze tajne w magazynie kluczy.
To polecenie cmdlet umożliwia pobieranie określonego hasła lub wszystkich kluczy tajnych w magazynie kluczy.

## Przykłady

### Przykład 1. Pobierz wszystkie bieżące wersje wszystkich kluczy tajnych w magazynie kluczy
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso'
```

To polecenie pobiera bieżące wersje wszystkich kluczy tajnych w magazynie kluczy o nazwie contoso.

### Przykład 2: pobieranie wszystkich wersji określonego hasła
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

To polecenie pobiera wszystkie wersje sekretu o nazwie ITSecret w magazynie kluczy o nazwie contoso.

### Przykład 3: uzyskiwanie bieżącej wersji określonego hasła
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

To polecenie pobiera aktualną wersję sekretu o nazwie ITSecret w magazynie kluczy o nazwie contoso.

### Przykład 4: uzyskiwanie określonej wersji określonego hasła
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

To polecenie pobiera określoną wersję sekretu o nazwie ITSecret w magazynie kluczy o nazwie contoso.

### Przykład 5: uzyskiwanie wartości zwykłego tekstu bieżącej wersji określonego klucza tajnego
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

Te polecenia uzyskują aktualną wersję sekretu o nazwie ITSecret, a następnie wyświetlają wartość zwykłego tekstu tego klucza tajnego.

### Przykład 6: pobieranie wszystkich kluczy tajnych, które zostały usunięte, ale nie zostały oczyszczone dla tego magazynu kluczy.
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

To polecenie pobiera wszystkie klucze tajne, które zostały wcześniej usunięte, ale nie zostały oczyszczone w magazynie kluczy o nazwie contoso.

### Przykład 7: Pobiera tajne ITSecret, który został usunięty, ale nie został odczyszczony dla tego magazynu kluczy.
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

To polecenie uzyskuje tajne ITSecret, który został wcześniej usunięty, ale nie został przeczyszczony w magazynie kluczy o nazwie contoso.
To polecenie zwróci metadane, takie jak Data usunięcia, oraz zaplanowaną datę przeczyszczania tego usuniętego klucza tajnego.

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

### -IncludeVersions
Wskazuje, że to polecenie cmdlet pobiera wszystkie wersje klucza tajnego.
Bieżąca wersja sekretu to pierwsza z nich na liście.
W przypadku określenia tego parametru należy również określić *nazwę* i parametry *magazynu* .

Jeśli nie określisz parametru *IncludeVersions* , to polecenie cmdlet pobiera aktualną wersję klucza tajnego o określonej *nazwie*.

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Określa, czy mają być pokazywane uprzednio usunięte klucze tajne w danych wyjściowych.

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę klucza tajnego do pobrania.

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Magazynname
Określa nazwę magazynu kluczy, do którego należy odpowiedni klucz tajny.
To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.

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
Określa wersję tajną.
To polecenie cmdlet konstruuje nazwę FQDN wpisu tajnego na podstawie nazwy magazynu kluczy, obecnie wybranego środowiska, tajnej nazwy i tajnej wersji.

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Ciąg

## WYSYŁA

### Lista<Microsoft. Azure. Commands. Data. models. SecretIdentityItem>, Microsoft. Azure. Commands. platforming. model. Secret, list<Microsoft. Azure. Commands. platform. modele. DeletedSecretIdentityItem>, Microsoft. Azure. Commands. DeletedSecret

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Cofanie — AzKeyVaultSecretRemoval](./Undo-AzKeyVaultSecretRemoval.md)

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

