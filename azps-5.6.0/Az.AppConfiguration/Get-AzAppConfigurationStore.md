---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: e7f7c1f7493123793a32163b4e8f37bec8706e10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998250"
---
# <span data-ttu-id="83d9c-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="83d9c-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="83d9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="83d9c-103">Pobierz lub przygotuj listy magazynów konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="83d9c-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="83d9c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="83d9c-104">SYNTAX</span></span>

### <span data-ttu-id="83d9c-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="83d9c-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="83d9c-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="83d9c-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="83d9c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="83d9c-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="83d9c-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="83d9c-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="83d9c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="83d9c-109">DESCRIPTION</span></span>
<span data-ttu-id="83d9c-110">Pobierz lub przygotuj listy magazynów konfiguracji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="83d9c-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="83d9c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="83d9c-111">EXAMPLES</span></span>

### <span data-ttu-id="83d9c-112">Przykład 1. Lista wszystkich magazynów konfiguracji aplikacji w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="83d9c-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="83d9c-113">To polecenie wyświetla listę wszystkich magazynów konfiguracji aplikacji w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="83d9c-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="83d9c-114">Przykład 2. Lista wszystkich magazynów konfiguracji aplikacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="83d9c-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="83d9c-115">To polecenie wyświetla listę wszystkich magazynów konfiguracji aplikacji w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="83d9c-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="83d9c-116">Przykład 3. Uzyskiwanie magazynu konfiguracji aplikacji według nazwy</span><span class="sxs-lookup"><span data-stu-id="83d9c-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="83d9c-117">To polecenie otrzymuje magazyn konfiguracji aplikacji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="83d9c-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="83d9c-118">Przykład 4. Uzyskiwanie magazynu konfiguracji aplikacji według potoku</span><span class="sxs-lookup"><span data-stu-id="83d9c-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="83d9c-119">To polecenie pobiera magazyn konfiguracji aplikacji według potoku.</span><span class="sxs-lookup"><span data-stu-id="83d9c-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="83d9c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83d9c-120">PARAMETERS</span></span>

### <span data-ttu-id="83d9c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d9c-121">-DefaultProfile</span></span>
<span data-ttu-id="83d9c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="83d9c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83d9c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83d9c-123">-InputObject</span></span>
<span data-ttu-id="83d9c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="83d9c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83d9c-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="83d9c-125">-Name</span></span>
<span data-ttu-id="83d9c-126">Nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="83d9c-126">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d9c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83d9c-127">-ResourceGroupName</span></span>
<span data-ttu-id="83d9c-128">Nazwa grupy zasobów, do której należy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="83d9c-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d9c-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83d9c-129">-SubscriptionId</span></span>
<span data-ttu-id="83d9c-130">Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83d9c-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d9c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d9c-131">CommonParameters</span></span>
<span data-ttu-id="83d9c-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d9c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d9c-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83d9c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d9c-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83d9c-134">INPUTS</span></span>

### <span data-ttu-id="83d9c-135">Microsoft.Azure.PowerShell.Cmdlet.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="83d9c-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="83d9c-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83d9c-136">OUTPUTS</span></span>

### <span data-ttu-id="83d9c-137">Microsoft.Azure.PowerShell.Cmdlet.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="83d9c-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="83d9c-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="83d9c-138">NOTES</span></span>

<span data-ttu-id="83d9c-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="83d9c-139">ALIASES</span></span>

<span data-ttu-id="83d9c-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83d9c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83d9c-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="83d9c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83d9c-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83d9c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83d9c-143">INPUTOBJECT: <IAppConfigurationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="83d9c-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83d9c-144">`[ConfigStoreName <String>]`: nazwa magazynu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="83d9c-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="83d9c-145">`[GroupName <String>]`: nazwa grupy zasobów linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="83d9c-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="83d9c-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="83d9c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83d9c-147">`[PrivateEndpointConnectionName <String>]`: nazwa prywatnego połączenia punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="83d9c-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="83d9c-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów, do której należy rejestr kontenerów.</span><span class="sxs-lookup"><span data-stu-id="83d9c-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="83d9c-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83d9c-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="83d9c-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83d9c-150">RELATED LINKS</span></span>

