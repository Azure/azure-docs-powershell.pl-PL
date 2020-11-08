---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225414"
---
# <span data-ttu-id="361fe-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="361fe-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="361fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="361fe-102">SYNOPSIS</span></span>
<span data-ttu-id="361fe-103">Generuje klucz dostępu dla określonego magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="361fe-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="361fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="361fe-104">SYNTAX</span></span>

### <span data-ttu-id="361fe-105">RegenerateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="361fe-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="361fe-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="361fe-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="361fe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="361fe-107">DESCRIPTION</span></span>
<span data-ttu-id="361fe-108">Generuje klucz dostępu dla określonego magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="361fe-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="361fe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="361fe-109">EXAMPLES</span></span>

### <span data-ttu-id="361fe-110">Przykład 1: ponowne generowanie klucza magazynu konfiguracji aplikacji</span><span class="sxs-lookup"><span data-stu-id="361fe-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="361fe-111">To polecenie generuje ponownie klucz magazynu konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="361fe-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="361fe-112">Przykład 2: ponowne generowanie klucza magazynu konfiguracji aplikacji według obiektów</span><span class="sxs-lookup"><span data-stu-id="361fe-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="361fe-113">To polecenie generuje ponownie klucz magazynu konfiguracji aplikacji według obiektu.</span><span class="sxs-lookup"><span data-stu-id="361fe-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="361fe-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="361fe-114">PARAMETERS</span></span>

### <span data-ttu-id="361fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="361fe-115">-DefaultProfile</span></span>
<span data-ttu-id="361fe-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="361fe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="361fe-117">-ID</span><span class="sxs-lookup"><span data-stu-id="361fe-117">-Id</span></span>
<span data-ttu-id="361fe-118">Identyfikator klucza do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="361fe-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="361fe-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="361fe-119">-InputObject</span></span>
<span data-ttu-id="361fe-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="361fe-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="361fe-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="361fe-121">-Name</span></span>
<span data-ttu-id="361fe-122">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="361fe-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="361fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="361fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="361fe-124">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="361fe-124">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="361fe-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="361fe-125">-SubscriptionId</span></span>
<span data-ttu-id="361fe-126">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="361fe-126">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="361fe-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="361fe-127">-Confirm</span></span>
<span data-ttu-id="361fe-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="361fe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="361fe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="361fe-129">-WhatIf</span></span>
<span data-ttu-id="361fe-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="361fe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="361fe-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="361fe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="361fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="361fe-132">CommonParameters</span></span>
<span data-ttu-id="361fe-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="361fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="361fe-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="361fe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="361fe-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="361fe-135">INPUTS</span></span>

### <span data-ttu-id="361fe-136">Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="361fe-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="361fe-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="361fe-137">OUTPUTS</span></span>

### <span data-ttu-id="361fe-138">Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. Api20200601. IApiKey</span><span class="sxs-lookup"><span data-stu-id="361fe-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="361fe-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="361fe-139">NOTES</span></span>

<span data-ttu-id="361fe-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="361fe-140">ALIASES</span></span>

<span data-ttu-id="361fe-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="361fe-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="361fe-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="361fe-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="361fe-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="361fe-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="361fe-144">INPUTobject <IAppConfigurationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="361fe-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="361fe-145">`[ConfigStoreName <String>]`: Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="361fe-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="361fe-146">`[GroupName <String>]`: Nazwa grupy zasobów linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="361fe-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="361fe-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="361fe-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="361fe-148">`[PrivateEndpointConnectionName <String>]`: Nazwa połączenia prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="361fe-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="361fe-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="361fe-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="361fe-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="361fe-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="361fe-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="361fe-151">RELATED LINKS</span></span>

