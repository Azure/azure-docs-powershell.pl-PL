---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242707"
---
# <span data-ttu-id="b0ea6-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="b0ea6-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="b0ea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="b0ea6-103">Pobiera komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="b0ea6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0ea6-104">SYNTAX</span></span>

### <span data-ttu-id="b0ea6-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b0ea6-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0ea6-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b0ea6-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b0ea6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b0ea6-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="b0ea6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0ea6-108">DESCRIPTION</span></span>
<span data-ttu-id="b0ea6-109">Pobiera komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="b0ea6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0ea6-110">EXAMPLES</span></span>

### <span data-ttu-id="b0ea6-111">Przykład 1. Lista wszystkich komunikacji równorzędnej w sieci VNET w obszarze sesji danych</span><span class="sxs-lookup"><span data-stu-id="b0ea6-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="b0ea6-112">To polecenie zawiera listę wszystkich komunikacji równorzędnej w sieci VNET w obszarze danych.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="b0ea6-113">Przykład 2. Uzyskiwanie komunikacji równorzędnej w sieci VNET</span><span class="sxs-lookup"><span data-stu-id="b0ea6-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="b0ea6-114">To polecenie pobiera komunikacji równorzędnej w sieci VNET.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="b0ea6-115">Przykład 3. Uzyskiwanie komunikacji równorzędnej w sieci VNET według obiektu</span><span class="sxs-lookup"><span data-stu-id="b0ea6-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="b0ea6-116">To polecenie pobiera obiekt w komunikacji równorzędnej sieci VNET.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="b0ea6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0ea6-117">PARAMETERS</span></span>

### <span data-ttu-id="b0ea6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0ea6-118">-DefaultProfile</span></span>
<span data-ttu-id="b0ea6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0ea6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0ea6-120">-InputObject</span></span>
<span data-ttu-id="b0ea6-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0ea6-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b0ea6-122">-Name</span></span>
<span data-ttu-id="b0ea6-123">Nazwa komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="b0ea6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0ea6-124">-PassThru</span></span>
<span data-ttu-id="b0ea6-125">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0ea6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0ea6-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0ea6-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-127">The name of the resource group.</span></span>
<span data-ttu-id="b0ea6-128">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b0ea6-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0ea6-129">-SubscriptionId</span></span>
<span data-ttu-id="b0ea6-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b0ea6-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b0ea6-131">-WorkspaceName</span></span>
<span data-ttu-id="b0ea6-132">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="b0ea6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0ea6-133">CommonParameters</span></span>
<span data-ttu-id="b0ea6-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0ea6-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0ea6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0ea6-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0ea6-136">INPUTS</span></span>

### <span data-ttu-id="b0ea6-137">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="b0ea6-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="b0ea6-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0ea6-138">OUTPUTS</span></span>

### <span data-ttu-id="b0ea6-139">Microsoft.Azure.PowerShell.Cmdlet.Databricks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b0ea6-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="b0ea6-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0ea6-140">NOTES</span></span>

<span data-ttu-id="b0ea6-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b0ea6-141">ALIASES</span></span>

<span data-ttu-id="b0ea6-142">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b0ea6-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b0ea6-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0ea6-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b0ea6-145">INPUTOBJECT: <IDatabricksIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="b0ea6-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0ea6-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b0ea6-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0ea6-147">`[PeeringName <String>]`: nazwa komunikacji równorzędnej vNet obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="b0ea6-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b0ea6-149">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="b0ea6-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b0ea6-151">`[WorkspaceName <String>]`: nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="b0ea6-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="b0ea6-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0ea6-152">RELATED LINKS</span></span>

