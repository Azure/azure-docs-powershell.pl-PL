---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182299"
---
# <span data-ttu-id="e1589-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="e1589-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="e1589-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1589-102">SYNOPSIS</span></span>
<span data-ttu-id="e1589-103">Ponownie generuje klucz dostępu dla określonego magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e1589-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="e1589-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e1589-104">SYNTAX</span></span>

### <span data-ttu-id="e1589-105">Generuj ponownieRozwiń (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e1589-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e1589-106">Generuj generujViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e1589-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e1589-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e1589-107">DESCRIPTION</span></span>
<span data-ttu-id="e1589-108">Ponownie generuje klucz dostępu dla określonego magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e1589-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="e1589-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e1589-109">EXAMPLES</span></span>

### <span data-ttu-id="e1589-110">Przykład 1. Klucz ponownego generowania magazynu konfiguracji aplikacji</span><span class="sxs-lookup"><span data-stu-id="e1589-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="e1589-111">To polecenie umożliwia ponowne wygenerowanie klucza magazynu konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e1589-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="e1589-112">Przykład 2. Ponowne generowanie klucza magazynu konfiguracji aplikacji według obiektu</span><span class="sxs-lookup"><span data-stu-id="e1589-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="e1589-113">To polecenie umożliwia ponowne wygenerowanie klucza magazynu konfiguracji aplikacji według obiektów.</span><span class="sxs-lookup"><span data-stu-id="e1589-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="e1589-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1589-114">PARAMETERS</span></span>

### <span data-ttu-id="e1589-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1589-115">-DefaultProfile</span></span>
<span data-ttu-id="e1589-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1589-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1589-117">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="e1589-117">-Id</span></span>
<span data-ttu-id="e1589-118">Identyfikator klucza do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="e1589-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="e1589-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1589-119">-InputObject</span></span>
<span data-ttu-id="e1589-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e1589-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1589-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e1589-121">-Name</span></span>
<span data-ttu-id="e1589-122">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e1589-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1589-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1589-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1589-124">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="e1589-124">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1589-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1589-125">-SubscriptionId</span></span>
<span data-ttu-id="e1589-126">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e1589-126">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1589-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1589-127">-Confirm</span></span>
<span data-ttu-id="e1589-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e1589-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1589-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1589-129">-WhatIf</span></span>
<span data-ttu-id="e1589-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1589-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1589-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e1589-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1589-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1589-132">CommonParameters</span></span>
<span data-ttu-id="e1589-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1589-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1589-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1589-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1589-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1589-135">INPUTS</span></span>

### <span data-ttu-id="e1589-136">Microsoft.Azure.PowerShell.Cmdlet.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="e1589-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="e1589-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1589-137">OUTPUTS</span></span>

### <span data-ttu-id="e1589-138">Microsoft.Azure.PowerShell.Cmdlet.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="e1589-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="e1589-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e1589-139">NOTES</span></span>

<span data-ttu-id="e1589-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e1589-140">ALIASES</span></span>

<span data-ttu-id="e1589-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e1589-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e1589-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="e1589-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e1589-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e1589-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e1589-144">INPUTOBJECT: <IAppConfigurationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="e1589-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e1589-145">`[ConfigStoreName <String>]`: nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="e1589-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="e1589-146">`[GroupName <String>]`: nazwa grupy zasobów linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="e1589-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="e1589-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="e1589-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e1589-148">`[PrivateEndpointConnectionName <String>]`: nazwa prywatnego połączenia punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="e1589-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="e1589-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów, do której należy rejestr kontenerów.</span><span class="sxs-lookup"><span data-stu-id="e1589-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="e1589-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e1589-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="e1589-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1589-151">RELATED LINKS</span></span>

