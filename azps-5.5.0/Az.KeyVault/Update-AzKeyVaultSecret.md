---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185363"
---
# Update-AzKeyVaultSecret

## SYNOPSIS
Aktualizuje atrybuty klucza tajnego w magazynie kluczy.

## SKŁADNIA

### Domyślne (domyślne)
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Update-AzKeyVaultSecret** aktualizuje edytowalne atrybuty klucza tajnego w magazynie kluczy.

## PRZYKŁADY

### Przykład 1. Modyfikowanie atrybutów tajnych
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

Pierwsze cztery polecenia definiują atrybuty daty wygaśnięcia, daty, tagów i typu kontekstowego NotBefore oraz przechowują atrybuty w zmiennych.
Ostatnie polecenie modyfikuje atrybuty klucza tajnego o nazwie HR w magazynie kluczy o nazwie ContosoVault przy użyciu zmiennych przechowywanych.

### Przykład 2. Usuwanie tagów i typu zawartości dla tajnych
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

To polecenie usuwa tagi i typ zawartości dla określonej wersji klucza tajnego o nazwie KADR w magazynie kluczy o nazwie Contoso.

### Przykład 3. Wyłączenie bieżącej wersji tajemnic, których nazwa zaczyna się od it
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

Pierwsze polecenie przechowuje wartość ciągu Contoso w $Vault zmienną.
Drugie polecenie przechowuje wartość ciągu IT w $Prefix zmienną.
Trzecie polecenie używa Get-AzKeyVaultSecret cmdlet w celu uzyskania sekretów określonego magazynu kluczy, a następnie przekazuje te tajemnice do polecenia cmdlet **Where-Object.** Polecenie **cmdlet Where-Object** odfiltrowuje sekrety nazw zaczynanych od znaków IT. Polecenie potokuje tajemnice, które pasują do filtru Update-AzKeyVaultSecret polecenie cmdlet, co spowoduje ich wyłączenie.

### Przykład 4. Ustawianie typu Zawartości dla wszystkich wersji tajnych
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

Pierwsze trzy polecenia definiują zmienne ciągu, które mają być używane dla parametrów *Nazwa* magazynu, *Nazwa* i *ContentType.* Czwarte polecenie używa polecenia cmdlet Get-AzKeyVaultKey do uzyskania określonych kluczy i potokuje klawisze do polecenia cmdlet programu Update-AzKeyVaultSecret, aby ustawić typ zawartości na XML.

## PARAMETERS

### - ContentType
Typ zawartości tajny.
Jeśli nie zostanie określona, istniejąca wartość typu zawartości tajnych pozostanie niezmieniona.
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

### — Włącz
Jeśli istnieje, włącz klucz tajny, jeśli wartość jest prawdziwa.
Wyłącz klucz tajny, jeśli wartość jest fałszywa.
Jeśli nie zostanie określona, istniejąca wartość stanu włączone/wyłączonego tajnych pozostanie niezmieniona.

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

### — Wygasa
Czas wygaśnięcia tajnego pliku w czasie UTC.
Jeśli nie zostanie określona, istniejąca wartość czasu wygaśnięcia tajemnicy pozostanie niezmieniona.

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

### -InputObject
Tajny obiekt

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

### — Nazwa
Tajna nazwa.
Polecenie cmdlet konstruuje nazwę FQDN tajnych nazw magazynów, obecnie wybranego środowiska i nazwy tajnej.

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
Czas UTC, przed którym nie można użyć tajnych danych.
Jeśli nie zostanie określona, istniejąca wartość atrybutu NotBefore sekretu pozostanie niezmieniona.

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
Jeśli ten przełącznik jest określony, zwróć tajny obiekt.

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

### — Tag
Hashtable representing secret tags.
Jeśli nie zostanie określona, istniejące tagi tajnych pozostaną niezmienione.
Usuń tag, określając pustą tabelę skrótów.

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
Nazwa magazynu.
Polecenie cmdlet konstruuje nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.

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

### — Wersja
Wersja tajna.
Polecenie cmdlet konstruuje nazwę FQDN tajnych nazw magazynów, obecnie wybrane środowisko, nazwę tajną i wersję tajną.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret

## NOTATKI

## LINKI POKREWNE
