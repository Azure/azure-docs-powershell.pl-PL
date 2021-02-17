---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: c610339bf90069f30d6107d46fc92fd896d6816c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188170"
---
# Get-AzKeyVaultRoleAssignment

## SYNOPSIS
Uzyskiwanie lub lista przypisań ról zarządzanego hsm. Użyj odpowiednich parametrów, aby wyświetlić listę przydziałów dla określonego użytkownika lub definicji roli.

## SKŁADNIA

### Lista (domyślna)
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByName
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Użyj tego `Get-AzKeyVaultRoleAssignment` polecenia, aby wyświetlić listę wszystkich przydziałów ról, które mają zastosowanie w zakresie.
Bez żadnych parametrów to polecenie zwraca wszystkie przydziały ról wykonane w ramach zarządzanego systemu HSM.
Tę listę można filtrować przy użyciu parametrów filtrowania dla podmiotu głównego, roli i zakresu.
Należy określić temat zadania.
Aby określić użytkownika, użyj parametrów SignInName lub Azure AD ObjectId.
Aby określić grupę zabezpieczeń, użyj parametru Azure AD ObjectId.
Aby określić aplikację usługi Azure AD, użyj parametrów ApplicationId lub ObjectId.
Przypisaną rolę należy określić przy użyciu parametru RoleDefinitionName lub RoleDefinitionId.
Zakres, w którym udzielany jest dostęp, można określić. Domyślnie jest to "/".

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

W tym przykładzie wymieniono wszystkie przypisania ról "mójHsm" we wszystkich zakresach.

### Przykład 2
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

W tym przykładzie wymieniono wszystkie przypisania ról "myHsm" w zakresie "/keys" i odfiltrowuje wynik według nazwy logowania użytkownika.

## PARAMETERS

### -ApplicationId
The app SPN.

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

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

### - HsmName
Nazwa hsm.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Identyfikator obiektu użytkownika lub grupy.

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleAssignmentName
Nazwa przydziału roli.

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleDefinitionId
Identyfikator roli, do których jest przydzielony podmiot zabezpieczeń.

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleDefinitionName
Nazwa roli RBAC, do których ma zostać przypisany podmiot zabezpieczeń.

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Zakres
Zakres, do którego ma zastosowanie przypisanie roli lub definicja, np. '/' lub '/keys' lub '/keys/{keyName}'.
W przypadku pominięcia tej przeoczonej w tym przypadku jest używane "/".

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

### -SignInName
Nazwa_logowania użytkownika.

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment

## NOTATKI

## LINKI POKREWNE
