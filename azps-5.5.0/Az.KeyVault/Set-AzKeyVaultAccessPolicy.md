---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: eeaea44ec387dc7739a97b5026054186ff817ab3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185514"
---
# Set-AzKeyVaultAccessPolicy

## SYNOPSIS
Udziela lub modyfikuje istniejące uprawnienia użytkownika, aplikacji lub grupy zabezpieczeń do wykonywania operacji z magazynem kluczy.

## SKŁADNIA

### ByUserPrincipalName (Domyślna)
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByObjectId
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByEmailAddress
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ForVault
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectByObjectId
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectByUserPrincipalName
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectByEmailAddress
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectForVault
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByObjectId
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdByUserPrincipalName
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByEmailAddress
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdForVault
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzKeyVaultAccessPolicy** udziela lub modyfikuje istniejące uprawnienia użytkownika, aplikacji lub grupy zabezpieczeń do wykonywania określonych operacji za pomocą magazynu kluczy. Nie modyfikuje uprawnień innych użytkowników, aplikacji ani grup zabezpieczeń w magazynie kluczy.
Jeśli ustawiasz uprawnienia dla grupy zabezpieczeń, ta operacja dotyczy tylko użytkowników w tej grupie zabezpieczeń.
Wszystkie następujące katalogi muszą mieć ten sam katalog Azure:
- Domyślny katalog subskrypcji platformy Azure, w którym znajduje się magazyn kluczy.
- Katalog Azure zawierający użytkownika lub grupę aplikacji, do których chcesz przyznać uprawnienia.
Oto przykłady scenariuszy, w których te warunki nie są spełnione i to polecenie cmdlet nie będzie działać:
- Autoryzowanie użytkownika z innej organizacji w celu zarządzania Twoim magazynem kluczy.
Każda organizacja ma własny katalog.
- Twoje konto platformy Azure ma wiele katalogów.
Jeśli zarejestrujesz aplikację w katalogu innym niż katalog domyślny, nie możesz autoryzować tej aplikacji do używania Twojego magazynu kluczy.
Aplikacja musi znajdować się w katalogu domyślnym.
Pamiętaj, że mimo że w przypadku tego polecenia cmdlet określenie grupy zasobów jest opcjonalne, należy to zrobić, aby uzyskać lepszą wydajność.

> [!NOTE]
> Podczas udzielania uprawnień zasad dostępu za pomocą podmiotu zabezpieczeń usługi należy użyć `-BypassObjectIdValidation` parametru.

## PRZYKŁADY

### Przykład 1. Udzielanie użytkownikowi uprawnień do magazynu kluczy i modyfikowanie uprawnień
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

Pierwsze polecenie udziela użytkownikowi w usłudze Azure Active Directory uprawnień do wykonywania operacji na kluczach i sekretach magazynu kluczy o nazwie PattiFuller@contoso.com Contoso03Vault. Parametr *PassThru* powoduje zwrócenie zaktualizowanego obiektu przez polecenie cmdlet.
Drugie polecenie modyfikuje uprawnienia, które zostały przyznane w pierwszym poleceniu, aby teraz zezwolić na uzyskiwanie sekretów oprócz ich ustawiania PattiFuller@contoso.com i usuwania. Po tym poleceniu uprawnienia do operacji na kluczach pozostaną niezmienione.
Ostatnie polecenie dodatkowo zmodyfikuje istniejące uprawnienia do PattiFuller@contoso.com usuwania wszystkich uprawnień do kluczowych operacji. Po tym poleceniu uprawnienia do operacji tajnych pozostają niezmienione.

### Przykład 2. Udzielanie uprawnień podmiotu zabezpieczeń usługi aplikacji do odczytu i zapisu sekretów
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

To polecenie udziela uprawnień aplikacji dla magazynu kluczy o nazwie Contoso03Vault.
Parametr *ServicePrincipalName* określa aplikację. Aplikacja musi być zarejestrowana w usłudze Azure Active Directory. Wartość parametru *ServicePrincipalName* musi być główną nazwą usługi aplikacji lub identyfikatorem GUID aplikacji.
W tym przykładzie określono nazwę podmiotu zabezpieczeń usługi, a polecenie udziela uprawnień aplikacji do `http://payroll.contoso.com` odczytu i zapisu sekretów.

### Przykład 3. Udzielanie uprawnień aplikacji przy użyciu identyfikatora obiektu
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

To polecenie udziela uprawnień aplikacji do odczytu i zapisu sekretów.
W tym przykładzie określono aplikację, używając identyfikatora obiektu podmiotu zabezpieczeń usługi aplikacji.

### Przykład 4. Udzielanie uprawnień do głównej nazwy użytkownika
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

To polecenie pozwala uzyskać, wyświetlić listę i ustawić uprawnienia dla określonej głównej nazwy użytkownika w celu uzyskania dostępu do tajemnic.

### Przykład 5. Włączanie pobierania sekretów z magazynu kluczy przez dostawcę zasobów Microsoft.Compute
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

To polecenie udziela uprawnień dla tajemnic pobierania z magazynu kluczy Contoso03Vault przez dostawcę zasobów Microsoft.Compute.

### Przykład 6. Udzielanie uprawnień grupie zabezpieczeń
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

Pierwsze polecenie używa polecenia cmdlet Get-AzADGroup do uzyskania wszystkich grup usługi Active Directory. W wyniku widać 3 zwrócone grupy o nazwie **group1,** **group2** i **group3.** Wiele grup może mieć tę samą nazwę, ale zawsze ma unikatowy identyfikator ObjectId. Jeśli jest zwracana więcej niż jedna grupa o takiej samej nazwie, należy użyć w wynikach obiektu ObjectId, aby zidentyfikować tę, której chcesz użyć.
Następnie użyj danych wyjściowych tego polecenia z Set-AzKeyVaultAccessPolicy, aby udzielić uprawnień do grupy Group2 dla Twojego magazynu kluczy o **nazwie myownvault.** W tym przykładzie wyliczane są grupy o nazwie "grupa2" w tym samym wierszu polecenia.
Na liście zwróconej może być wiele grup o nazwie "grupa2".
W tym przykładzie wybierany jest pierwszy indeks \[ 0 \] na liście zwróconej.

### Przykład 7. Udzielanie usłudze Azure Information Protection dostępu do klucza dzierżawy zarządzanej przez klienta (BYOK)
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

To polecenie autoryzuje usługę Azure Information Protection do używania klucza zarządzanego przez klienta (czyli klucza własnego, czyli scenariusza "BYOK") jako klucza dzierżawy usługi Azure Information Protection.
Po uruchomieniu tego polecenia określ własną nazwę magazynu klucza, ale musisz określić parametr *ServicePrincipalName* z identyfikatorem GUID **00000012-0000-0000-c000-000000000000** i określić uprawnienia w przykładzie.

## PARAMETERS

### -ApplicationId
Do użytku w przyszłości.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BypassObjectIdValidation
Umożliwia określenie identyfikatora obiektu bez sprawdzania, czy obiekt istnieje w usłudze Azure Active Directory.
Użyj tego parametru tylko wtedy, gdy chcesz udzielić dostępu do magazynu kluczy identyfikatorowi obiektu, który odwołuje się do grupy zabezpieczeń delegowanych z innej dzierżawy platformy Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### -EmailAddress
Określa adres e-mail użytkownika, któremu mają być udzielane uprawnienia.
Ten adres e-mail musi znajdować się w katalogu skojarzonym z bieżącą subskrypcją i być unikatowy.

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForDeployment
Umożliwia dostawcy zasobów Microsoft.Compute pobieranie sekretów z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się podczas tworzenia zasobów, na przykład podczas tworzenia maszyny wirtualnej.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForScriptEncryption
Umożliwia usłudze szyfrowania dysków Platformy Azure uzyskiwanie sekretów i odłącza klucze z tego magazynu kluczy.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
Umożliwia usłudze Azure Resource Manager uzyskiwanie sekretów z tego magazynu kluczy, gdy do tego magazynu kluczy odwołuje się we wdrożeniu szablonu.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Obiekt magazynu kluczy

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
Określa identyfikator obiektu użytkownika lub podmiotu zabezpieczeń usługi w usłudze Azure Active Directory, dla którego mają być udzielane uprawnienia.

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -PermissionsToCertificates
Określa tablicę uprawnień certyfikatu, które mają być udzielane użytkownikowi lub podmiotowi zabezpieczeń usługi.
Dopuszczalne wartości dla tego parametru:
- Wszystkie
- Pobierz
- Lista
- Usuń
- Tworzenie
- Importowanie
- Aktualizacja
- Managecontacts
- Getissuers
- Listissuers
- Setissuers
- Deleteissuers
- Zarządzanie usługami
- Odzyskaj
- Kopia zapasowa
- Przywróć
- Przeczyszczanie

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToKeys
Określa tablicę uprawnień do obsługi kluczy, które mają być udzielane użytkownikowi lub podmiotowi zabezpieczeń usługi.
Dopuszczalne wartości dla tego parametru:
- Wszystkie
- Odszyfrowywanie
- Szyfrowanie
- UnwrapKey
- WrapKey
- Weryfikuj
- Podpisz
- Pobierz
- Lista
- Aktualizacja
- Tworzenie
- Importowanie
- Usuń
- Kopia zapasowa
- Przywróć
- Odzyskaj
- Przeczyszczanie

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToSecrets
Określa tablicę uprawnień operacji tajnych do udzielania użytkownikowi lub podmiotowi zabezpieczeń usługi.
Dopuszczalne wartości dla tego parametru:
- Wszystkie
- Pobierz
- Lista
- Ustaw
- Usuń
- Kopia zapasowa
- Przywróć
- Odzyskaj
- Przeczyszczanie

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToStorage
Określa uprawnienia do działania na koncie magazynu zarządzanego i operację SaS w celu udzielenia podmiotowi użytkownika lub podmiotu zabezpieczeń usługi.
Dopuszczalne wartości dla tego parametru:
- wszystko
- Pobierz
- lista
- usuń
- ustaw
- aktualizacja
- generuj klucz ponownie
- getsas
- listsas
- deletesas
- setsas
- odzyskiwanie
- kopia zapasowa
- przywracanie
- przeczyszczanie

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu magazynu kluczy

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Określa nazwę podmiotu zabezpieczeń usługi aplikacji, której uprawnienia mają być udzielane.
Określ identyfikator aplikacji, nazywany również identyfikatorem klienta, zarejestrowany dla aplikacji w usłudze AzureActive Directory. Aplikacja o nazwie podmiotu zabezpieczeń usługi, która określa ten parametr, musi być zarejestrowana w usłudze Azure Directory zawierającej Bieżącą subskrypcję.

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipalName
Określa główną nazwę użytkownika, któremu mają być udzielane uprawnienia.
Główna nazwa użytkownika musi istnieć w katalogu skojarzonym z bieżącą subskrypcją.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Określa nazwę magazynu kluczy.
To polecenie cmdlet modyfikuje zasady dostępu dla magazynu kluczy, który określa ten parametr.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

## NOTATKI

## LINKI POKREWNE

[Get-AzKeyVault](./Get-AzKeyVault.md)

[Remove-AzKeyVaultAccessPolicy](./Remove-AzKeyVaultAccessPolicy.md)

