---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050101"
---
# Update-AzKeyVaultSecret

## STRESZCZENIe
Aktualizuje atrybuty klucza tajnego w magazynie kluczy.

## POLECENIA

### Domyślne (domyślnie)
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Inputobject
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Update-AzKeyVaultSecret** umożliwia aktualizowanie edytowalnych atrybutów klucza tajnego w magazynie kluczy.

## Przykłady

### Przykład 1: modyfikowanie atrybutów tajności
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

Pierwsze cztery polecenia definiują atrybuty daty wygaśnięcia, NotBefore Data, Tagi i typ kontekstu oraz przechowują atrybuty w zmiennych.
Polecenie ostatnie modyfikuje atrybuty wpisu tajnego o nazwie HR w magazynie kluczy o nazwie ContosoVault, korzystając z przechowywanych zmiennych.

### Przykład 2: usuwanie znaczników i typu zawartości dla wpisu tajnego
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

To polecenie usuwa znaczniki i typ zawartości określonej wersji sekretu o nazwie HR w magazynie kluczy o nazwie contoso.

### Przykład 3: wyłączanie bieżącej wersji kluczy tajnych, których imiona i nazwiska zaczynają się od niej
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

Pierwsze polecenie zapisuje wartość ciągu contoso w zmiennej $Vault.
Drugie polecenie zapisuje wartość ciągu w zmiennej $Prefix.
W trzecim poleceniu jest używane polecenie cmdlet Get-AzKeyVaultSecret w celu uzyskania kluczy tajnych w określonym magazynie kluczy, a następnie przekazanie tych kluczy tajnych do polecenia cmdlet **WHERE-Object** . Polecenie cmdlet **WHERE-Object** filtruje klucze tajne dla nazw, które zaczynają się od znaków. Polecenie przełączy klucze tajne, które pasują do filtru Update-AzKeyVaultSecret polecenia cmdlet, co powoduje wyłączenie ich.

### Przykład 4: Ustawianie typu zawartości dla wszystkich wersji klucza tajnego
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

Pierwsze trzy polecenia definiują zmienne tekstowe, które mają być używane dla parametrów *magazynname* , *name* i *ContentType* . W czwartym poleceniu jest używane polecenie cmdlet Get-AzKeyVaultKey w celu uzyskania określonych kluczy i przeprzewody klawiszy do polecenia cmdlet Update-AzKeyVaultSecret w celu ustawienia typu zawartości na wartość XML.

## PARAMETRÓW

### -Type
Typ zawartości klucza tajnego.
Jeśli nie zostanie określona, istniejąca wartość typu zawartości sekretu pozostanie niezmieniona.
Usuń istniejącą wartość typu zawartości, określając pusty ciąg.

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

### -Enable
Jeśli jest obecny, włącz klucz tajny, jeśli wartość jest równa prawda.
Wyłącz klucz tajny, jeśli wartość jest równa FAŁSZ.
Jeśli nie określono tej wartości, istniejąca wartość stanu włączenia/wyłączenia klucza tajnego pozostaje bez zmian.

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
Czas wygaśnięcia klucza tajnego w czasie UTC.
Jeśli nie podano tego parametru, istniejąca wartość czasu wygaśnięcia klucza tajnego pozostanie niezmieniona.

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

### -Inputobject
Obiekt tajny

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa tajna.
Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i sekretu.

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Czas UTC, przed upływem którego nie można użyć klucza.
Jeśli nie podano tego parametru, istniejąca wartość atrybutu NotBefore tajnego wpisu pozostaje niezmieniona.

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

### -PassThru
Polecenie cmdlet domyślnie nie zwraca obiektu.
Jeśli ten przełącznik jest określony, zwraca tajny obiekt.

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
Obiekt Hashtable reprezentujący Tagi tajne.
Jeśli nie określono, istniejące znaczniki sekretu pozostaną niezmienione.
Usuń znacznik, określając pustą tablicę.

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
Nazwa magazynu.
Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Wersja tajna.
Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranego środowiska, tajnej nazwy i tajnej wersji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
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

### Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecretIdentityItem

## WYSYŁA

### Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecret

## INFORMACYJN

## LINKI POKREWNE
