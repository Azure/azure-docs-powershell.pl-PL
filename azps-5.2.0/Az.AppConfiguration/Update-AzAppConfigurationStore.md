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
# <span data-ttu-id="4f9b9-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="4f9b9-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="4f9b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="4f9b9-103">Umożliwia zaktualizowanie magazynu konfiguracji przy użyciu określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="4f9b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f9b9-104">SYNTAX</span></span>

### <span data-ttu-id="4f9b9-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4f9b9-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4f9b9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4f9b9-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4f9b9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4f9b9-107">DESCRIPTION</span></span>
<span data-ttu-id="4f9b9-108">Umożliwia zaktualizowanie magazynu konfiguracji przy użyciu określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="4f9b9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f9b9-109">EXAMPLES</span></span>

### <span data-ttu-id="4f9b9-110">Przykład 1: Włączanie szyfrowania danych magazynu konfiguracji aplikacji przez tożsamość zarządzaną przez system</span><span class="sxs-lookup"><span data-stu-id="4f9b9-110">Example 1: Enable data encryption of the app configuration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4f9b9-111">To polecenie umożliwia szyfrowanie danych za pomocą klucza przechowywanego w magazynie kluczy platformy Azure przy użyciu tożsamości zarządzanej przez system.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="4f9b9-112">W magazynie musi być włączona funkcja usuwania wstępnego i przeczyszczania, a zarządzana tożsamość musi mieć następujące kluczowe uprawnienia: Get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="4f9b9-113">Przykład 2: Włączanie szyfrowania danych w magazynie konfiguracji aplikacji według tożsamości zarządzanej przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="4f9b9-113">Example 2: Enable data encryption of the app configuration store by user-assigned managed identity</span></span>
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

<span data-ttu-id="4f9b9-114">To polecenie umożliwia szyfrowanie danych za pomocą klucza przechowywanego w magazynie kluczy platformy Azure przy użyciu tożsamości zarządzanej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="4f9b9-115">Tożsamość przypisana przez użytkownika musi być ustawiona na wartość `-UserAssignedIdentity` .</span><span class="sxs-lookup"><span data-stu-id="4f9b9-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="4f9b9-116">W magazynie musi być włączona funkcja usuwania wstępnego i przeczyszczania, a zarządzana tożsamość musi mieć następujące kluczowe uprawnienia: Get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="4f9b9-117">Przykład 3: wyłączanie szyfrowania magazynu konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-117">Example 3: Disable encryption of an app configuration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4f9b9-118">To polecenie wyłącza szyfrowanie magazynu konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-118">This command disables encryption of an app configuration store.</span></span>

### <span data-ttu-id="4f9b9-119">Przykład 3: Aktualizowanie wersji SKU i znacznika magazynu konfiguracji aplikacji według rurociągu.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-119">Example 3: Update sku and tag of an app configuration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4f9b9-120">To polecenie powoduje zaktualizowanie wersji SKU i znacznika magazynu konfiguracji aplikacji według rurociągu.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-120">This command updates sku and tag of an app configuration store by pipeline.</span></span>

## <span data-ttu-id="4f9b9-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f9b9-121">PARAMETERS</span></span>

### <span data-ttu-id="4f9b9-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f9b9-122">-AsJob</span></span>
<span data-ttu-id="4f9b9-123">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="4f9b9-123">Run the command as a job</span></span>

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

### <span data-ttu-id="4f9b9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f9b9-124">-DefaultProfile</span></span>
<span data-ttu-id="4f9b9-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f9b9-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="4f9b9-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="4f9b9-127">Identyfikator URI klucza magazynu kluczy używanego do szyfrowania danych.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="4f9b9-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4f9b9-128">-IdentityType</span></span>
<span data-ttu-id="4f9b9-129">Typ używanej tożsamości zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-129">The type of managed identity used.</span></span>
<span data-ttu-id="4f9b9-130">Typ "SystemAssignedAndUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="4f9b9-131">Typ "Brak" spowoduje usunięcie wszystkich tożsamości.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-131">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="4f9b9-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4f9b9-132">-InputObject</span></span>
<span data-ttu-id="4f9b9-133">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4f9b9-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="4f9b9-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="4f9b9-135">Identyfikator klienta tożsamości, która będzie używana w celu uzyskania dostępu do magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="4f9b9-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4f9b9-136">-Name</span></span>
<span data-ttu-id="4f9b9-137">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="4f9b9-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4f9b9-138">-NoWait</span></span>
<span data-ttu-id="4f9b9-139">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="4f9b9-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4f9b9-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f9b9-140">-ResourceGroupName</span></span>
<span data-ttu-id="4f9b9-141">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="4f9b9-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="4f9b9-142">-Sku</span></span>
<span data-ttu-id="4f9b9-143">Nazwa SKU magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="4f9b9-144">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4f9b9-144">-SubscriptionId</span></span>
<span data-ttu-id="4f9b9-145">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="4f9b9-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="4f9b9-146">-Tag</span></span>
<span data-ttu-id="4f9b9-147">Znaczniki zasobów ARM.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="4f9b9-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4f9b9-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="4f9b9-149">Lista tożsamości przypisanych do danego zasobu.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="4f9b9-150">Klucze słowników tożsamości przypisane do użytkownika są identyfikatorami zasobów ARM w postaci: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="4f9b9-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="4f9b9-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4f9b9-151">-Confirm</span></span>
<span data-ttu-id="4f9b9-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f9b9-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f9b9-153">-WhatIf</span></span>
<span data-ttu-id="4f9b9-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f9b9-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f9b9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f9b9-156">CommonParameters</span></span>
<span data-ttu-id="4f9b9-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f9b9-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f9b9-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f9b9-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f9b9-159">INPUTS</span></span>

### <span data-ttu-id="4f9b9-160">Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="4f9b9-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="4f9b9-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f9b9-161">OUTPUTS</span></span>

### <span data-ttu-id="4f9b9-162">Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="4f9b9-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="4f9b9-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f9b9-163">NOTES</span></span>

<span data-ttu-id="4f9b9-164">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4f9b9-164">ALIASES</span></span>

<span data-ttu-id="4f9b9-165">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f9b9-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4f9b9-166">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f9b9-167">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4f9b9-168">INPUTobject <IAppConfigurationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="4f9b9-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f9b9-169">`[ConfigStoreName <String>]`: Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="4f9b9-170">`[GroupName <String>]`: Nazwa grupy zasobów linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="4f9b9-171">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4f9b9-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f9b9-172">`[PrivateEndpointConnectionName <String>]`: Nazwa połączenia prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="4f9b9-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="4f9b9-173">`[ResourceGroupName <String>]`: Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="4f9b9-174">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4f9b9-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="4f9b9-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f9b9-175">RELATED LINKS</span></span>



<span data-ttu-id="4f9b9-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [Nowe — AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="4f9b9-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

