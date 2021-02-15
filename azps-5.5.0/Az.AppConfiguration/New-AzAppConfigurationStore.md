---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182306"
---
# <span data-ttu-id="be939-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="be939-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="be939-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be939-102">SYNOPSIS</span></span>
<span data-ttu-id="be939-103">Tworzy magazyn konfiguracji z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="be939-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="be939-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="be939-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="be939-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="be939-105">DESCRIPTION</span></span>
<span data-ttu-id="be939-106">Tworzy magazyn konfiguracji z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="be939-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="be939-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="be939-107">EXAMPLES</span></span>

### <span data-ttu-id="be939-108">Przykład 1. Tworzenie magazynu konfiguracji aplikacji</span><span class="sxs-lookup"><span data-stu-id="be939-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="be939-109">To polecenie tworzy magazyn konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="be939-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="be939-110">Przykład 2. Tworzenie konfiguracji aplikacji przy użyciu typu IdentityType ustawionego na "UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="be939-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="be939-111">To polecenie tworzy konfigurację aplikacji i przypisuje do niego tożsamość zarządzaną przypisaną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="be939-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="be939-112">Zobacz przykład poniższych kroków włączania `Update-AzAppConfigurationStore` klucza zarządzanego CMK (cusomer).</span><span class="sxs-lookup"><span data-stu-id="be939-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="be939-113">Przykład 3. Tworzenie konfiguracji aplikacji przy użyciu typu IdentityType ustawionego na "SystemAssigned"</span><span class="sxs-lookup"><span data-stu-id="be939-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="be939-114">To polecenie tworzy konfigurację aplikacji i włącza przypisaną przez system tożsamość zarządzaną skojarzoną z zasobem.</span><span class="sxs-lookup"><span data-stu-id="be939-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="be939-115">Zobacz przykład poniższych kroków włączania `Update-AzAppConfigurationStore` klucza zarządzanego CMK (cusomer).</span><span class="sxs-lookup"><span data-stu-id="be939-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="be939-116">Przykład 4. Tworzenie konfiguracji aplikacji przy użyciu typu IdentityType ustawionego na "SystemAssigned, UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="be939-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="be939-117">Możesz włączyć tożsamość zarządzaną przypisaną przez system i jednocześnie nadać tożsamości przypisane przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="be939-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="be939-118">Zobacz przykład poniższych kroków włączania `Update-AzAppConfigurationStore` klucza zarządzanego CMK (cusomer).</span><span class="sxs-lookup"><span data-stu-id="be939-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="be939-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be939-119">PARAMETERS</span></span>

### <span data-ttu-id="be939-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="be939-120">-AsJob</span></span>
<span data-ttu-id="be939-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="be939-121">Run the command as a job</span></span>

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

### <span data-ttu-id="be939-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be939-122">-DefaultProfile</span></span>
<span data-ttu-id="be939-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="be939-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be939-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="be939-124">-IdentityType</span></span>
<span data-ttu-id="be939-125">Typ używanej tożsamości zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="be939-125">The type of managed identity used.</span></span>
<span data-ttu-id="be939-126">Typ "SystemAssignedAndUserAssigned" obejmuje zarówno tożsamość utworzoną niejawnie, jak i zestaw tożsamości przypisanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="be939-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="be939-127">Wpisanie typu "Brak" spowoduje usunięcie wszystkich tożsamości.</span><span class="sxs-lookup"><span data-stu-id="be939-127">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="be939-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="be939-128">-Location</span></span>
<span data-ttu-id="be939-129">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="be939-129">The location of the resource.</span></span>
<span data-ttu-id="be939-130">Po utworzeniu zasobu nie można go zmienić.</span><span class="sxs-lookup"><span data-stu-id="be939-130">This cannot be changed after the resource is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be939-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="be939-131">-Name</span></span>
<span data-ttu-id="be939-132">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="be939-132">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be939-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="be939-133">-NoWait</span></span>
<span data-ttu-id="be939-134">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="be939-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="be939-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be939-135">-ResourceGroupName</span></span>
<span data-ttu-id="be939-136">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="be939-136">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be939-137">- SKU</span><span class="sxs-lookup"><span data-stu-id="be939-137">-Sku</span></span>
<span data-ttu-id="be939-138">Nazwa sKU magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="be939-138">The SKU name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be939-139">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be939-139">-SubscriptionId</span></span>
<span data-ttu-id="be939-140">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="be939-140">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be939-141">— Tag</span><span class="sxs-lookup"><span data-stu-id="be939-141">-Tag</span></span>
<span data-ttu-id="be939-142">Tagi zasobu.</span><span class="sxs-lookup"><span data-stu-id="be939-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="be939-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="be939-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="be939-144">Lista tożsamości przypisanych przez użytkownika skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="be939-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="be939-145">Klucze słownika tożsamości przypisane przez użytkownika ARM identyfikatory zasobów w postaci: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="be939-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="be939-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="be939-146">-Confirm</span></span>
<span data-ttu-id="be939-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="be939-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be939-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be939-148">-WhatIf</span></span>
<span data-ttu-id="be939-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be939-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be939-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="be939-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be939-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be939-151">CommonParameters</span></span>
<span data-ttu-id="be939-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be939-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be939-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be939-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be939-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be939-154">INPUTS</span></span>

## <span data-ttu-id="be939-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be939-155">OUTPUTS</span></span>

### <span data-ttu-id="be939-156">Microsoft.Azure.PowerShell.Cmdlet.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="be939-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="be939-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="be939-157">NOTES</span></span>

<span data-ttu-id="be939-158">ALIASY</span><span class="sxs-lookup"><span data-stu-id="be939-158">ALIASES</span></span>

## <span data-ttu-id="be939-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be939-159">RELATED LINKS</span></span>



[<span data-ttu-id="be939-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="be939-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

