---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222701"
---
# <span data-ttu-id="03f64-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="03f64-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="03f64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03f64-102">SYNOPSIS</span></span>
<span data-ttu-id="03f64-103">Umożliwia utworzenie magazynu konfiguracji z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="03f64-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="03f64-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03f64-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="03f64-105">Opis</span><span class="sxs-lookup"><span data-stu-id="03f64-105">DESCRIPTION</span></span>
<span data-ttu-id="03f64-106">Umożliwia utworzenie magazynu konfiguracji z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="03f64-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="03f64-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03f64-107">EXAMPLES</span></span>

### <span data-ttu-id="03f64-108">Przykład 1. Tworzenie magazynu konfiguracji aplikacji</span><span class="sxs-lookup"><span data-stu-id="03f64-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="03f64-109">To polecenie tworzy magazyn konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="03f64-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="03f64-110">Przykład 2: Tworzenie konfiguracji aplikacji o identyfikatorze tożsamości o wartości "UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="03f64-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="03f64-111">To polecenie powoduje utworzenie konfiguracji aplikacji i przypisanie zarządzanej tożsamości przypisanej do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="03f64-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="03f64-112">Zapoznaj się z przykładem, `Update-AzAppConfigurationStore` Aby wykonać następujące czynności w celu włączenia CMK (cusomer Managed Key).</span><span class="sxs-lookup"><span data-stu-id="03f64-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="03f64-113">Przykład 3: Tworzenie konfiguracji aplikacji o identyfikatorze tożsamości o wartości "SystemAssigned"</span><span class="sxs-lookup"><span data-stu-id="03f64-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="03f64-114">To polecenie powoduje utworzenie konfiguracji aplikacji i włączenie zarządzanej przez system tożsamości zarządzanej skojarzonej z zasobem.</span><span class="sxs-lookup"><span data-stu-id="03f64-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="03f64-115">Zapoznaj się z przykładem, `Update-AzAppConfigurationStore` Aby wykonać następujące czynności w celu włączenia CMK (cusomer Managed Key).</span><span class="sxs-lookup"><span data-stu-id="03f64-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="03f64-116">Przykład 4: Tworzenie konfiguracji aplikacji o wartości IdentityType ustawionej na "SystemAssigned, UserAssigned"</span><span class="sxs-lookup"><span data-stu-id="03f64-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="03f64-117">Możesz włączyć zarządzaną przez system tożsamość i jednocześnie nadawać tożsamości przypisane do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="03f64-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="03f64-118">Zapoznaj się z przykładem, `Update-AzAppConfigurationStore` Aby wykonać następujące czynności w celu włączenia CMK (cusomer Managed Key).</span><span class="sxs-lookup"><span data-stu-id="03f64-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="03f64-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03f64-119">PARAMETERS</span></span>

### <span data-ttu-id="03f64-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03f64-120">-AsJob</span></span>
<span data-ttu-id="03f64-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="03f64-121">Run the command as a job</span></span>

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

### <span data-ttu-id="03f64-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03f64-122">-DefaultProfile</span></span>
<span data-ttu-id="03f64-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03f64-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03f64-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="03f64-124">-IdentityType</span></span>
<span data-ttu-id="03f64-125">Typ używanej tożsamości zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="03f64-125">The type of managed identity used.</span></span>
<span data-ttu-id="03f64-126">Typ "SystemAssignedAndUserAssigned" obejmuje zarówno niejawnie utworzoną tożsamość, jak i zestaw tożsamości przypisanych do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="03f64-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="03f64-127">Typ "Brak" spowoduje usunięcie wszystkich tożsamości.</span><span class="sxs-lookup"><span data-stu-id="03f64-127">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="03f64-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="03f64-128">-Location</span></span>
<span data-ttu-id="03f64-129">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="03f64-129">The location of the resource.</span></span>
<span data-ttu-id="03f64-130">Nie można jej zmienić po utworzeniu zasobu.</span><span class="sxs-lookup"><span data-stu-id="03f64-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="03f64-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03f64-131">-Name</span></span>
<span data-ttu-id="03f64-132">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="03f64-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="03f64-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="03f64-133">-NoWait</span></span>
<span data-ttu-id="03f64-134">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="03f64-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="03f64-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03f64-135">-ResourceGroupName</span></span>
<span data-ttu-id="03f64-136">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="03f64-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="03f64-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="03f64-137">-Sku</span></span>
<span data-ttu-id="03f64-138">Nazwa SKU magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="03f64-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="03f64-139">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="03f64-139">-SubscriptionId</span></span>
<span data-ttu-id="03f64-140">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="03f64-140">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="03f64-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="03f64-141">-Tag</span></span>
<span data-ttu-id="03f64-142">Znaczniki zasobu.</span><span class="sxs-lookup"><span data-stu-id="03f64-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="03f64-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="03f64-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="03f64-144">Lista tożsamości przypisanych do danego zasobu.</span><span class="sxs-lookup"><span data-stu-id="03f64-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="03f64-145">Klucze słowników tożsamości przypisane do użytkownika są identyfikatorami zasobów ARM w postaci: "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="03f64-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="03f64-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03f64-146">-Confirm</span></span>
<span data-ttu-id="03f64-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03f64-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03f64-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03f64-148">-WhatIf</span></span>
<span data-ttu-id="03f64-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03f64-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03f64-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03f64-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03f64-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03f64-151">CommonParameters</span></span>
<span data-ttu-id="03f64-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03f64-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03f64-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03f64-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03f64-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03f64-154">INPUTS</span></span>

## <span data-ttu-id="03f64-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03f64-155">OUTPUTS</span></span>

### <span data-ttu-id="03f64-156">Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="03f64-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="03f64-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03f64-157">NOTES</span></span>

<span data-ttu-id="03f64-158">PISUJE</span><span class="sxs-lookup"><span data-stu-id="03f64-158">ALIASES</span></span>

## <span data-ttu-id="03f64-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03f64-159">RELATED LINKS</span></span>



[<span data-ttu-id="03f64-160">Nowe — AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="03f64-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

