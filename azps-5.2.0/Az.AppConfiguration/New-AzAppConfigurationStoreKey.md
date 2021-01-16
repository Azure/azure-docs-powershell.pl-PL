---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322537"
---
# <span data-ttu-id="d401c-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="d401c-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="d401c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d401c-102">SYNOPSIS</span></span>
<span data-ttu-id="d401c-103">Generuje klucz dostępu dla określonego magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d401c-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="d401c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d401c-104">SYNTAX</span></span>

### <span data-ttu-id="d401c-105">RegenerateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d401c-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d401c-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d401c-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d401c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d401c-107">DESCRIPTION</span></span>
<span data-ttu-id="d401c-108">Generuje klucz dostępu dla określonego magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d401c-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="d401c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d401c-109">EXAMPLES</span></span>

### <span data-ttu-id="d401c-110">Przykład 1: ponowne generowanie klucza magazynu konfiguracji aplikacji</span><span class="sxs-lookup"><span data-stu-id="d401c-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="d401c-111">To polecenie generuje ponownie klucz magazynu konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d401c-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="d401c-112">Przykład 2: ponowne generowanie klucza magazynu konfiguracji aplikacji według obiektów</span><span class="sxs-lookup"><span data-stu-id="d401c-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="d401c-113">To polecenie generuje ponownie klucz magazynu konfiguracji aplikacji według obiektu.</span><span class="sxs-lookup"><span data-stu-id="d401c-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="d401c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d401c-114">PARAMETERS</span></span>

### <span data-ttu-id="d401c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d401c-115">-DefaultProfile</span></span>
<span data-ttu-id="d401c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d401c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d401c-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d401c-117">-Id</span></span>
<span data-ttu-id="d401c-118">Identyfikator klucza do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="d401c-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="d401c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d401c-119">-InputObject</span></span>
<span data-ttu-id="d401c-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d401c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d401c-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d401c-121">-Name</span></span>
<span data-ttu-id="d401c-122">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d401c-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="d401c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d401c-123">-ResourceGroupName</span></span>
<span data-ttu-id="d401c-124">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="d401c-124">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="d401c-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d401c-125">-SubscriptionId</span></span>
<span data-ttu-id="d401c-126">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d401c-126">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="d401c-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d401c-127">-Confirm</span></span>
<span data-ttu-id="d401c-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d401c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d401c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d401c-129">-WhatIf</span></span>
<span data-ttu-id="d401c-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d401c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d401c-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d401c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d401c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d401c-132">CommonParameters</span></span>
<span data-ttu-id="d401c-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d401c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d401c-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d401c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d401c-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d401c-135">INPUTS</span></span>

### <span data-ttu-id="d401c-136">Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="d401c-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="d401c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d401c-137">OUTPUTS</span></span>

### <span data-ttu-id="d401c-138">Microsoft. Azure. PowerShell. polecenia. AppConfiguration. models. Api20200601. IApiKey</span><span class="sxs-lookup"><span data-stu-id="d401c-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="d401c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d401c-139">NOTES</span></span>

<span data-ttu-id="d401c-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d401c-140">ALIASES</span></span>

<span data-ttu-id="d401c-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d401c-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d401c-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d401c-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d401c-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d401c-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d401c-144">INPUTobject <IAppConfigurationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="d401c-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d401c-145">`[ConfigStoreName <String>]`: Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d401c-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="d401c-146">`[GroupName <String>]`: Nazwa grupy zasobów linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="d401c-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="d401c-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d401c-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d401c-148">`[PrivateEndpointConnectionName <String>]`: Nazwa połączenia prywatnego punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="d401c-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="d401c-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="d401c-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="d401c-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d401c-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="d401c-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d401c-151">RELATED LINKS</span></span>

