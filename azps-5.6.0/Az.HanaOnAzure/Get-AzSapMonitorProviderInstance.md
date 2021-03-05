---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 66f5a875f05b9c5d2fcdcc8a63eba9d149a9ba7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013370"
---
# <span data-ttu-id="55240-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="55240-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="55240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55240-102">SYNOPSIS</span></span>
<span data-ttu-id="55240-103">Pobiera właściwości wystąpienia dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="55240-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="55240-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="55240-104">SYNTAX</span></span>

### <span data-ttu-id="55240-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="55240-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="55240-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="55240-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="55240-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="55240-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="55240-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="55240-108">DESCRIPTION</span></span>
<span data-ttu-id="55240-109">Pobiera właściwości wystąpienia dostawcy dla określonej subskrypcji, grupy zasobów, nazwy SapMonitor i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="55240-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="55240-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="55240-110">EXAMPLES</span></span>

### <span data-ttu-id="55240-111">Przykład 1. Uzyskiwanie wszystkich wystąpień w obszarze monitora SAP</span><span class="sxs-lookup"><span data-stu-id="55240-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="55240-112">To polecenie pobiera wszystkie wystąpienia pod monitorem SAP.</span><span class="sxs-lookup"><span data-stu-id="55240-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="55240-113">Przykład 2. Uzyskiwanie wystąpień monitora SAP według nazwy</span><span class="sxs-lookup"><span data-stu-id="55240-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="55240-114">To polecenie pobiera wystąpienia monitora SAP według nazwy.</span><span class="sxs-lookup"><span data-stu-id="55240-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="55240-115">Przykład 3. Uzyskiwanie wystąpień monitora SAP według obiektów</span><span class="sxs-lookup"><span data-stu-id="55240-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="55240-116">To polecenie pobiera wystąpienia monitorów SAP według obiektów.</span><span class="sxs-lookup"><span data-stu-id="55240-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="55240-117">Przykład 4. Uzyskiwanie wystąpień monitora SAP według potoku</span><span class="sxs-lookup"><span data-stu-id="55240-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="55240-118">To polecenie pobiera wystąpienia monitora SAP według potoku.</span><span class="sxs-lookup"><span data-stu-id="55240-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="55240-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55240-119">PARAMETERS</span></span>

### <span data-ttu-id="55240-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55240-120">-DefaultProfile</span></span>
<span data-ttu-id="55240-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="55240-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55240-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55240-122">-InputObject</span></span>
<span data-ttu-id="55240-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="55240-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55240-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="55240-124">-Name</span></span>
<span data-ttu-id="55240-125">Nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="55240-125">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55240-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55240-126">-ResourceGroupName</span></span>
<span data-ttu-id="55240-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="55240-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55240-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="55240-128">-SapMonitorName</span></span>
<span data-ttu-id="55240-129">Nazwa zasobu monitorowego SAP.</span><span class="sxs-lookup"><span data-stu-id="55240-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55240-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55240-130">-SubscriptionId</span></span>
<span data-ttu-id="55240-131">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="55240-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="55240-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="55240-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55240-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55240-133">CommonParameters</span></span>
<span data-ttu-id="55240-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55240-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55240-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55240-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55240-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55240-136">INPUTS</span></span>

### <span data-ttu-id="55240-137">Microsoft.Azure.PowerShell.Cmdlet.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="55240-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="55240-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55240-138">OUTPUTS</span></span>

### <span data-ttu-id="55240-139">Microsoft.Azure.PowerShell.Cmdlet.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="55240-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="55240-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="55240-140">NOTES</span></span>

<span data-ttu-id="55240-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="55240-141">ALIASES</span></span>

<span data-ttu-id="55240-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55240-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55240-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="55240-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55240-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="55240-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55240-145">INPUTOBJECT: <IHanaOnAzureIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="55240-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="55240-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="55240-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="55240-147">`[Location <String>]`: lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="55240-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="55240-148">`[OperationKind <AccessPolicyUpdateKind?>]`: nazwa operacji</span><span class="sxs-lookup"><span data-stu-id="55240-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="55240-149">`[ProviderInstanceName <String>]`: nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="55240-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="55240-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="55240-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="55240-151">`[ResourceName <String>]`: nazwa zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="55240-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="55240-152">`[SapMonitorName <String>]`: nazwa zasobu monitorów SAP.</span><span class="sxs-lookup"><span data-stu-id="55240-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="55240-153">`[Scope <String>]`: zakres dostawcy zasobów dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="55240-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="55240-154">Zasób nadrzędny jest rozszerzany przez tożsamości zarządzane.</span><span class="sxs-lookup"><span data-stu-id="55240-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="55240-155">`[SubscriptionId <String>]`: Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="55240-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="55240-156">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="55240-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="55240-157">`[VaultName <String>]`: nazwa magazynu</span><span class="sxs-lookup"><span data-stu-id="55240-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="55240-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55240-158">RELATED LINKS</span></span>

