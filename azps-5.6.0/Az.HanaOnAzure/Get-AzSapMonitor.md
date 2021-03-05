---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 0de9aa6dd623efa379a6123570e766d30c850ab8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013377"
---
# <span data-ttu-id="d7970-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="d7970-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="d7970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7970-102">SYNOPSIS</span></span>
<span data-ttu-id="d7970-103">Pobiera właściwości monitora SAP dla określonej subskrypcji, grupy zasobów i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="d7970-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="d7970-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7970-104">SYNTAX</span></span>

### <span data-ttu-id="d7970-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d7970-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7970-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="d7970-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7970-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d7970-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d7970-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7970-108">DESCRIPTION</span></span>
<span data-ttu-id="d7970-109">Pobiera właściwości monitora SAP dla określonej subskrypcji, grupy zasobów i nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="d7970-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="d7970-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7970-110">EXAMPLES</span></span>

### <span data-ttu-id="d7970-111">Przykład 1. Uzyskiwanie wszystkich monitorów SAP w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d7970-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="d7970-112">To polecenie pobiera monitory SAP w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d7970-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="d7970-113">Przykład 2. Uzyskiwanie monitora SAP według nazwy</span><span class="sxs-lookup"><span data-stu-id="d7970-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="d7970-114">To polecenie otrzymuje monitor SAP według nazwy.</span><span class="sxs-lookup"><span data-stu-id="d7970-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="d7970-115">Przykład 3. Uzyskiwanie monitora SAP według obiektu</span><span class="sxs-lookup"><span data-stu-id="d7970-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="d7970-116">To polecenie pobiera obiektowy monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="d7970-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="d7970-117">Przykład 4. Uzyskiwanie monitora SAP według potoku</span><span class="sxs-lookup"><span data-stu-id="d7970-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="d7970-118">To polecenie pobiera monitor SAP według potoku.</span><span class="sxs-lookup"><span data-stu-id="d7970-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="d7970-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7970-119">PARAMETERS</span></span>

### <span data-ttu-id="d7970-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7970-120">-DefaultProfile</span></span>
<span data-ttu-id="d7970-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7970-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7970-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7970-122">-InputObject</span></span>
<span data-ttu-id="d7970-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d7970-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d7970-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d7970-124">-Name</span></span>
<span data-ttu-id="d7970-125">Nazwa zasobu monitorowego SAP.</span><span class="sxs-lookup"><span data-stu-id="d7970-125">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7970-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7970-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7970-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7970-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="d7970-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7970-128">-SubscriptionId</span></span>
<span data-ttu-id="d7970-129">Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d7970-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d7970-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d7970-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d7970-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7970-131">CommonParameters</span></span>
<span data-ttu-id="d7970-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7970-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7970-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7970-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7970-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7970-134">INPUTS</span></span>

### <span data-ttu-id="d7970-135">Microsoft.Azure.PowerShell.Cmdlet.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="d7970-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="d7970-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7970-136">OUTPUTS</span></span>

### <span data-ttu-id="d7970-137">Microsoft.Azure.PowerShell.Cmdlet.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="d7970-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="d7970-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7970-138">NOTES</span></span>

<span data-ttu-id="d7970-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d7970-139">ALIASES</span></span>

<span data-ttu-id="d7970-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7970-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7970-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d7970-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7970-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d7970-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7970-143">INPUTOBJECT: <IHanaOnAzureIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d7970-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d7970-144">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d7970-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7970-145">`[Location <String>]`: lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="d7970-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="d7970-146">`[OperationKind <AccessPolicyUpdateKind?>]`: nazwa operacji</span><span class="sxs-lookup"><span data-stu-id="d7970-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="d7970-147">`[ProviderInstanceName <String>]`: nazwa wystąpienia dostawcy.</span><span class="sxs-lookup"><span data-stu-id="d7970-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="d7970-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7970-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d7970-149">`[ResourceName <String>]`: nazwa zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="d7970-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="d7970-150">`[SapMonitorName <String>]`: nazwa zasobu monitorów SAP.</span><span class="sxs-lookup"><span data-stu-id="d7970-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="d7970-151">`[Scope <String>]`: zakres dostawcy zasobów dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="d7970-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="d7970-152">Zasób nadrzędny jest rozszerzany przez tożsamości zarządzane.</span><span class="sxs-lookup"><span data-stu-id="d7970-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="d7970-153">`[SubscriptionId <String>]`: Identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d7970-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d7970-154">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d7970-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d7970-155">`[VaultName <String>]`: nazwa magazynu</span><span class="sxs-lookup"><span data-stu-id="d7970-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="d7970-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7970-156">RELATED LINKS</span></span>

