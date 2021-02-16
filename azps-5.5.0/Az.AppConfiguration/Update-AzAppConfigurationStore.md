---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 8aea57e0c2bea5dbaa2e3233e886c97bfebe4bd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195322"
---
# <span data-ttu-id="50cfa-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="50cfa-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="50cfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="50cfa-103">Aktualizuje magazyn konfiguracji o określone parametry.</span><span class="sxs-lookup"><span data-stu-id="50cfa-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="50cfa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50cfa-104">SYNTAX</span></span>

### <span data-ttu-id="50cfa-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="50cfa-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="50cfa-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="50cfa-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="50cfa-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="50cfa-107">DESCRIPTION</span></span>
<span data-ttu-id="50cfa-108">Aktualizuje magazyn konfiguracji o określone parametry.</span><span class="sxs-lookup"><span data-stu-id="50cfa-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="50cfa-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50cfa-109">EXAMPLES</span></span>

### <span data-ttu-id="50cfa-110">Przykład 1. Włączanie szyfrowania danych magazynu konfiguracji aplikacji za pomocą tożsamości zarządzanej przypisanej przez system</span><span class="sxs-lookup"><span data-stu-id="50cfa-110">Example 1: Enable data encryption of the app configuration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="50cfa-111">To polecenie umożliwia szyfrowanie danych przy użyciu klucza przechowywanego w magazynie kluczy platformy Azure przy użyciu tożsamości zarządzanej przypisanej do systemu.</span><span class="sxs-lookup"><span data-stu-id="50cfa-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="50cfa-112">Magazyn musi mieć włączone funkcję "miękkiego usuwania" i ochrony przed przeczyszczaniami, a tożsamość zarządzana musi mieć następujące uprawnienia klucza: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="50cfa-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="50cfa-113">Przykład 2. Włączanie szyfrowania danych magazynu konfiguracji aplikacji przez tożsamość zarządzaną przypisaną przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="50cfa-113">Example 2: Enable data encryption of the app configuration store by user-assigned managed identity</span></span>
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

<span data-ttu-id="50cfa-114">To polecenie umożliwia szyfrowanie danych przy użyciu klucza przechowywanego w magazynie kluczy platformy Azure przy użyciu tożsamości zarządzanej przypisanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="50cfa-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="50cfa-115">Tożsamość przypisana przez użytkownika musi być ustawiona za `-UserAssignedIdentity` pomocą.</span><span class="sxs-lookup"><span data-stu-id="50cfa-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="50cfa-116">Magazyn musi mieć włączone funkcję "miękkiego usuwania" i ochrony przed przeczyszczaniami, a tożsamość zarządzana musi mieć następujące uprawnienia klucza: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="50cfa-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="50cfa-117">Przykład 3. Wyłączenie szyfrowania magazynu konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="50cfa-117">Example 3: Disable encryption of an app configuration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="50cfa-118">To polecenie wyłącza szyfrowanie magazynu konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="50cfa-118">This command disables encryption of an app configuration store.</span></span>

### <span data-ttu-id="50cfa-119">Przykład 3. Aktualizowanie sKU i tagu magazynu konfiguracji aplikacji według potoku.</span><span class="sxs-lookup"><span data-stu-id="50cfa-119">Example 3: Update sku and tag of an app configuration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="50cfa-120">To polecenie aktualizuje element SKU i tag magazynu konfiguracji aplikacji według potoku.</span><span class="sxs-lookup"><span data-stu-id="50cfa-120">This command updates sku and tag of an app configuration store by pipeline.</span></span>

## <span data-ttu-id="50cfa-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50cfa-121">PARAMETERS</span></span>

### <span data-ttu-id="50cfa-122">— AsJob</span><span class="sxs-lookup"><span data-stu-id="50cfa-122">-AsJob</span></span>
<span data-ttu-id="50cfa-123">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="50cfa-123">Run the command as a job</span></span>

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

### <span data-ttu-id="50cfa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50cfa-124">-DefaultProfile</span></span>
<span data-ttu-id="50cfa-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="50cfa-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50cfa-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="50cfa-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="50cfa-127">URI klucza magazynu kluczy używanego do szyfrowania danych.</span><span class="sxs-lookup"><span data-stu-id="50cfa-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="50cfa-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="50cfa-128">-IdentityType</span></span>
<span data-ttu-id="50cfa-129">Typ używanej tożsamości zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="50cfa-129">The type of managed identity used.</span></span>
<span data-ttu-id="50cfa-130">Typ "SystemAssignedAndUserAssigned" obejmuje zarówno tożsamość utworzoną niejawnie, jak i zestaw tożsamości przypisanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="50cfa-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="50cfa-131">Wpisanie typu "Brak" spowoduje usunięcie wszystkich tożsamości.</span><span class="sxs-lookup"><span data-stu-id="50cfa-131">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="50cfa-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50cfa-132">-InputObject</span></span>
<span data-ttu-id="50cfa-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="50cfa-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="50cfa-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="50cfa-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="50cfa-135">Identyfikator klienta tożsamości, która będzie używana do uzyskiwania dostępu do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="50cfa-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="50cfa-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="50cfa-136">-Name</span></span>
<span data-ttu-id="50cfa-137">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="50cfa-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="50cfa-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="50cfa-138">-NoWait</span></span>
<span data-ttu-id="50cfa-139">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="50cfa-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="50cfa-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50cfa-140">-ResourceGroupName</span></span>
<span data-ttu-id="50cfa-141">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="50cfa-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="50cfa-142">- SKU</span><span class="sxs-lookup"><span data-stu-id="50cfa-142">-Sku</span></span>
<span data-ttu-id="50cfa-143">Nazwa sKU magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="50cfa-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="50cfa-144">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50cfa-144">-SubscriptionId</span></span>
<span data-ttu-id="50cfa-145">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="50cfa-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="50cfa-146">— Tag</span><span class="sxs-lookup"><span data-stu-id="50cfa-146">-Tag</span></span>
<span data-ttu-id="50cfa-147">Tagi ARM zasobów.</span><span class="sxs-lookup"><span data-stu-id="50cfa-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="50cfa-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="50cfa-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="50cfa-149">Lista tożsamości przypisanych przez użytkownika skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="50cfa-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="50cfa-150">Klucze słownika tożsamości przypisane przez użytkownika ARM identyfikatory zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="50cfa-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="50cfa-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50cfa-151">-Confirm</span></span>
<span data-ttu-id="50cfa-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="50cfa-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50cfa-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50cfa-153">-WhatIf</span></span>
<span data-ttu-id="50cfa-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50cfa-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50cfa-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="50cfa-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50cfa-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50cfa-156">CommonParameters</span></span>
<span data-ttu-id="50cfa-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50cfa-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50cfa-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50cfa-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50cfa-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50cfa-159">INPUTS</span></span>

### <span data-ttu-id="50cfa-160">Microsoft.Azure.PowerShell.Cmdlet.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="50cfa-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="50cfa-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50cfa-161">OUTPUTS</span></span>

### <span data-ttu-id="50cfa-162">Microsoft.Azure.PowerShell.Cmdlet.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="50cfa-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="50cfa-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50cfa-163">NOTES</span></span>

<span data-ttu-id="50cfa-164">ALIASY</span><span class="sxs-lookup"><span data-stu-id="50cfa-164">ALIASES</span></span>

<span data-ttu-id="50cfa-165">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50cfa-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="50cfa-166">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="50cfa-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="50cfa-167">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="50cfa-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="50cfa-168">INPUTOBJECT: <IAppConfigurationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="50cfa-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="50cfa-169">`[ConfigStoreName <String>]`: nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="50cfa-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="50cfa-170">`[GroupName <String>]`: nazwa grupy zasobów linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="50cfa-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="50cfa-171">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="50cfa-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="50cfa-172">`[PrivateEndpointConnectionName <String>]`: nazwa prywatnego połączenia punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="50cfa-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="50cfa-173">`[ResourceGroupName <String>]`: nazwa grupy zasobów, do której należy rejestr kontenerów.</span><span class="sxs-lookup"><span data-stu-id="50cfa-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="50cfa-174">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="50cfa-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="50cfa-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50cfa-175">RELATED LINKS</span></span>



<span data-ttu-id="50cfa-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="50cfa-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

