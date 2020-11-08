---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222599"
---
# <span data-ttu-id="5e33e-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="5e33e-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="5e33e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e33e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e33e-103">Pobiera elementy równorzędne wirtualnej przestrzeni roboczej.</span><span class="sxs-lookup"><span data-stu-id="5e33e-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="5e33e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e33e-104">SYNTAX</span></span>

### <span data-ttu-id="5e33e-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="5e33e-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e33e-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="5e33e-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="5e33e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e33e-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="5e33e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5e33e-108">DESCRIPTION</span></span>
<span data-ttu-id="5e33e-109">Pobiera elementy równorzędne wirtualnej przestrzeni roboczej.</span><span class="sxs-lookup"><span data-stu-id="5e33e-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="5e33e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e33e-110">EXAMPLES</span></span>

### <span data-ttu-id="5e33e-111">Przykład 1: wyświetlanie wszystkich elementów równorzędnych wirtualnej w ramach datakostki</span><span class="sxs-lookup"><span data-stu-id="5e33e-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="5e33e-112">To polecenie wyświetla listę wszystkich elementów równorzędnych wirtualnej w obszarze datakostki.</span><span class="sxs-lookup"><span data-stu-id="5e33e-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="5e33e-113">Przykład 2: uzyskiwanie komunikacji równorzędnej VNET</span><span class="sxs-lookup"><span data-stu-id="5e33e-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="5e33e-114">To polecenie umożliwia pobieranie komunikacji równorzędnej sieci VNET.</span><span class="sxs-lookup"><span data-stu-id="5e33e-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="5e33e-115">Przykład 3: uzyskiwanie komunikacji równorzędnej VNET według obiektów</span><span class="sxs-lookup"><span data-stu-id="5e33e-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="5e33e-116">To polecenie pobiera komunikację równorzędną VNET według obiektu.</span><span class="sxs-lookup"><span data-stu-id="5e33e-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="5e33e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e33e-117">PARAMETERS</span></span>

### <span data-ttu-id="5e33e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e33e-118">-DefaultProfile</span></span>
<span data-ttu-id="5e33e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e33e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e33e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e33e-120">-InputObject</span></span>
<span data-ttu-id="5e33e-121">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5e33e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5e33e-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e33e-122">-Name</span></span>
<span data-ttu-id="5e33e-123">Nazwa komunikacji równorzędnej w obszarze roboczym sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5e33e-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="5e33e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e33e-124">-PassThru</span></span>
<span data-ttu-id="5e33e-125">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="5e33e-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5e33e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e33e-126">-ResourceGroupName</span></span>
<span data-ttu-id="5e33e-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5e33e-127">The name of the resource group.</span></span>
<span data-ttu-id="5e33e-128">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="5e33e-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5e33e-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5e33e-129">-SubscriptionId</span></span>
<span data-ttu-id="5e33e-130">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="5e33e-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5e33e-131">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="5e33e-131">-WorkspaceName</span></span>
<span data-ttu-id="5e33e-132">Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="5e33e-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="5e33e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e33e-133">CommonParameters</span></span>
<span data-ttu-id="5e33e-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e33e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e33e-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e33e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e33e-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e33e-136">INPUTS</span></span>

### <span data-ttu-id="5e33e-137">Microsoft. Azure. PowerShell. polecenia. datakosteks. models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="5e33e-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="5e33e-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e33e-138">OUTPUTS</span></span>

### <span data-ttu-id="5e33e-139">Microsoft. Azure. PowerShell. polecenia. datakosteks. models. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5e33e-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="5e33e-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e33e-140">NOTES</span></span>

<span data-ttu-id="5e33e-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="5e33e-141">ALIASES</span></span>

<span data-ttu-id="5e33e-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e33e-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e33e-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="5e33e-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e33e-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e33e-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e33e-145">INPUTobject <IDatabricksIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="5e33e-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e33e-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="5e33e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e33e-147">`[PeeringName <String>]`: Nazwa komunikacji równorzędnej w obszarze roboczym w sieci vNet.</span><span class="sxs-lookup"><span data-stu-id="5e33e-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="5e33e-148">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5e33e-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5e33e-149">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="5e33e-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="5e33e-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="5e33e-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5e33e-151">`[WorkspaceName <String>]`: Nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="5e33e-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="5e33e-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e33e-152">RELATED LINKS</span></span>

