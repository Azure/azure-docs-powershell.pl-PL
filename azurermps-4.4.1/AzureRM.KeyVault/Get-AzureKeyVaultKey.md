---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://go.microsoft.com/fwlink/?LinkId=690297
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: 48d050623ea75bed1aee1b78a26bf81bf3305e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527561"
---
# Get-AzureKeyVaultKey

## STRESZCZENIe
Pobiera klucze magazynu kluczy.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ByVaultName (domyślny)
```
Get-AzureKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyName
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyVersions
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedKey
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureKeyVaultKey** pobiera klucze magazynu kluczy platformy Azure.
To polecenie cmdlet umożliwia pobieranie określonego pakietu **Microsoft. Azure. Commands. Key. MODELES** lub lista wszystkich obiektów **pakietu** kluczy w magazynie kluczy lub według wersji.

## Przykłady

### Przykład 1. pobieranie wszystkich kluczy w magazynie kluczy
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

To polecenie pobiera wszystkie klucze w magazynie kluczy o nazwie contoso.

### Przykład 2: uzyskiwanie bieżącej wersji klucza
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

To polecenie pobiera aktualną wersję klucza o nazwie ITPfx w magazynie kluczy o nazwie contoso.

### Przykład 3: pobieranie wszystkich wersji klucza
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

To polecenie pobiera wszystkie wersje klucza o nazwie ITPfx w kluczu vaultnamed contoso.

### Przykład 4: uzyskiwanie określonej wersji klucza
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

To polecenie pobiera określoną wersję klucza o nazwie ITPfx w magazynie kluczy o nazwie contoso.
Po uruchomieniu tego polecenia możesz sprawdzić różne właściwości klucza, przechodząc do obiektu $Key.

### Przykład 5: Uzyskaj wszystkie klucze, które zostały usunięte, ale nie zostały oczyszczone dla tego magazynu kluczy.
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

To polecenie pobiera wszystkie klucze, które zostały wcześniej usunięte, ale nie zostały oczyszczone w magazynie kluczy o nazwie contoso.

### Przykład 6: Pobiera klucze ITPfx, które zostały usunięte, ale nie zostały oczyszczone dla tego magazynu kluczy.
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

To polecenie pobiera klucze ITPfx, które zostały wcześniej usunięte, ale nie zostały oczyszczone w magazynie kluczy o nazwie contoso.
To polecenie zwróci metadane, takie jak Data usunięcia, oraz zaplanowaną datę przeczyszczania tego usuniętego klucza.

## PARAMETRÓW

### -IncludeVersions
Wskazuje, że to polecenie cmdlet pobiera wszystkie wersje klucza.
Bieżąca wersja klucza to pierwsza z nich na liście.
W przypadku określenia tego parametru należy również określić *nazwę* i parametry *magazynu* .

Jeśli nie określisz parametru *IncludeVersions* , to polecenie cmdlet pobiera bieżącą wersję klucza o określonej *nazwie*.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Określa, czy w wyniku mają być pokazywane uprzednio usunięte klucze.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę pakietu kluczy, który ma zostać wyświetlony.

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Magazynname
Określa nazwę magazynu kluczy, z którego to polecenie cmdlet pobiera klucze.
To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) magazynu kluczy na podstawie nazwy, jaką ten parametr określa i wybrane środowisko.

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
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Ciąg

## WYSYŁA

### Lista<Microsoft. Azure. Commands.. modele. KeyIdentityItem>, Microsoft. Azure. Commands. platforming. models. DeletedKeyIdentityItem, lista<Microsoft. Azure. Commands. Modeling. modele.>, Microsoft. Azure. Commands. DeletedKeyBundle

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[Cofanie — AzureKeyVaultKeyRemoval](./Undo-AzureKeyVaultKeyRemoval.md)

[Set-AzureKeyVaultKeyAttribute](./Set-AzureKeyVaultKeyAttribute.md)

