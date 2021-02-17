---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8d602e5cbb3a24307ba77daf9a88a79a3c5bb705
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180443"
---
# Get-AzKeyVaultManagedHsm

## SYNOPSIS
Uzyskiwanie zarządzanych hsm.

## SKŁADNIA

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzKeyVaultManagedHsm** pobiera informacje o zarządzanych modułach HSM w subskrypcji. Można wyświetlić wszystkie zarządzane wystąpienia HSM w subskrypcji lub przefiltrować wyniki według grupy zasobów lub określonego zarządzanego modułu hsm.
Pamiętaj, że mimo że określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet w przypadku uzyskania pojedynczego zarządzanego modułu HSM, należy to zrobić w celu uzyskania lepszej wydajności.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich zarządzanych kodów HSM w ramach bieżącej subskrypcji
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

To polecenie pobiera wszystkie zarządzane moduły HSM w bieżącej subskrypcji.

### Przykład 2. Uzyskiwanie określonego zarządzanego hsm
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

To polecenie pobiera zarządzany moduł HSM o nazwie myhsm w bieżącej subskrypcji.

### Przykład 3. Uzyskiwanie zarządzanych hsm w grupie zasobów
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

To polecenie pobiera wszystkie zarządzane moduły HSM w grupie zasobów o nazwie myrg1.

### Przykład 4. Uzyskiwanie zarządzanych hsm przy użyciu filtrowania
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

To polecenie pobiera wszystkie zarządzane moduły HSM w subskrypcji, które zaczynają się od "myhsm".

## PARAMETERS

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

### — Nazwa
Nazwa HSM. Polecenie cmdlet tworzy nazwę FQDN modułu HSM na podstawie nazwy i obecnie wybranego środowiska.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
Określa nazwę grupy zasobów skojarzonej z zarządzanym modułem HSM, do których jest ponawiane zapytanie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### — Tag
Określa klucz i opcjonalną wartość określonego tagu, według których ma być filtrowana lista zarządzanych hsM.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.Collections.Hashtable

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem

## NOTATKI

## LINKI POKREWNE

[New-AzKeyVaultManagedHsm](./New-AzKeyVaultManagedHsm.md)

[Remove-AzKeyVaultManagedHsm](./Remove-AzKeyVaultManagedHsm.md)

[Update-AzKeyVaultManagedHsm](./Update-AzKeyVaultManagedHsm.md)