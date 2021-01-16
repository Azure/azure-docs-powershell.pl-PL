---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 8aea57e0c2bea5dbaa2e3233e886c97bfebe4bd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322476"
---
# Update-AzAppConfigurationStore

## STRESZCZENIe
Umożliwia zaktualizowanie magazynu konfiguracji przy użyciu określonych parametrów.

## POLECENIA

### UpdateExpanded (domyślny)
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## Opis
Umożliwia zaktualizowanie magazynu konfiguracji przy użyciu określonych parametrów.

## Przykłady

### Przykład 1: Włączanie szyfrowania danych magazynu konfiguracji aplikacji przez tożsamość zarządzaną przez system
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

To polecenie umożliwia szyfrowanie danych za pomocą klucza przechowywanego w magazynie kluczy platformy Azure przy użyciu tożsamości zarządzanej przez system.
W magazynie musi być włączona funkcja usuwania wstępnego i przeczyszczania, a zarządzana tożsamość musi mieć następujące kluczowe uprawnienia: Get, wrapKey, unwrapKey.

### Przykład 2: Włączanie szyfrowania danych w magazynie konfiguracji aplikacji według tożsamości zarządzanej przez użytkownika
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $assignedIdentity.PrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test11 -EncryptionKeyIdentifier $key.Id -KeyVaultIdentityClientId $assignedIdentity.ClientId

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

To polecenie umożliwia szyfrowanie danych za pomocą klucza przechowywanego w magazynie kluczy platformy Azure przy użyciu tożsamości zarządzanej przez użytkownika.
Tożsamość przypisana przez użytkownika musi być ustawiona na wartość `-UserAssignedIdentity` .
W magazynie musi być włączona funkcja usuwania wstępnego i przeczyszczania, a zarządzana tożsamość musi mieć następujące kluczowe uprawnienia: Get, wrapKey, unwrapKey.

### Przykład 3: wyłączanie szyfrowania magazynu konfiguracji aplikacji.
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

To polecenie wyłącza szyfrowanie magazynu konfiguracji aplikacji.

### Przykład 3: Aktualizowanie wersji SKU i znacznika magazynu konfiguracji aplikacji według rurociągu.
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

To polecenie powoduje zaktualizowanie wersji SKU i znacznika magazynu konfiguracji aplikacji według rurociągu.

## PARAMETRÓW

### -AsJob
Uruchamianie polecenia jako zadania

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyIdentifier
Identyfikator URI klucza magazynu kluczy używanego do szyfrowania danych.

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

### -IdentityType
Typ używanej tożsamości zarządzanej.
Typ "SystemAssignedAndUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.
Typ "Brak" spowoduje usunięcie wszystkich tożsamości.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyVaultIdentityClientId
Identyfikator klienta tożsamości, która będzie używana w celu uzyskania dostępu do magazynu kluczy.

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

### -Name (nazwa)
Nazwa magazynu konfiguracji.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nowait
Wykonywanie polecenia asynchronicznie

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

### -ResourceGroupName
Nazwa grupy zasobów, do której należy rejestr kontenera.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Nazwa SKU magazynu konfiguracji.

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

### -Subskrypcji
Identyfikator subskrypcji platformy Microsoft Azure.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Znaczniki zasobów ARM.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserAssignedIdentity
Lista tożsamości przypisanych do danego zasobu.
Klucze słowników tożsamości przypisane do użytkownika są identyfikatorami zasobów ARM w postaci: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. IAppConfigurationIdentity

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. Api20200601. IConfigurationStore

## INFORMACYJN

PISUJE

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.


INPUTobject <IAppConfigurationIdentity> : parametr Identity
  - `[ConfigStoreName <String>]`: Nazwa magazynu konfiguracji.
  - `[GroupName <String>]`: Nazwa grupy zasobów linku prywatnego.
  - `[Id <String>]`: Ścieżka tożsamości zasobu
  - `[PrivateEndpointConnectionName <String>]`: Nazwa połączenia prywatnego punktu końcowego
  - `[ResourceGroupName <String>]`: Nazwa grupy zasobów, do której należy rejestr kontenera.
  - `[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure.

## LINKI POKREWNE



[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [Nowe — AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

