---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
ms.openlocfilehash: e0ce7e46e8105048d58ee8a4334eaf098b40399c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377881"
---
# <span data-ttu-id="ff295-101">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="ff295-101">Get-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="ff295-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff295-102">SYNOPSIS</span></span>
<span data-ttu-id="ff295-103">Pobiera przeniesienie zasobu.</span><span class="sxs-lookup"><span data-stu-id="ff295-103">Gets the Move Resource.</span></span>

## <span data-ttu-id="ff295-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff295-104">SYNTAX</span></span>

### <span data-ttu-id="ff295-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ff295-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff295-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ff295-106">Get</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ff295-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ff295-107">DESCRIPTION</span></span>
<span data-ttu-id="ff295-108">Pobiera przeniesienie zasobu.</span><span class="sxs-lookup"><span data-stu-id="ff295-108">Gets the Move Resource.</span></span>

## <span data-ttu-id="ff295-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff295-109">EXAMPLES</span></span>

### <span data-ttu-id="ff295-110">Przykład 1: uzyskiwanie szczegółów dotyczących wszystkich zasobów w kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="ff295-110">Example 1: Get details of all the resources in the Move collection.</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM          

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.networ
                                          k/publicipaddresses/psdemovm-ip, /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/psd
                                          emorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet, /subscriptions/e80eb9fa-c996-4435-aa32
                                          -5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/psdemovm62
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : MovePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : psdemovm62
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Network/networkInterfaces
ResourceSettingTargetResourceName       : psdemovm62
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network
                                          /networkInterfaces/psdemovm62
SourceResourceSettingResourceType       : Microsoft.Network/networkInterfaces
SourceResourceSettingTargetResourceName : psdemovm62
Target                                  :
TargetId                                :
Type                                    :

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/psdemorm
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : CommitPending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : psdemorm
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : resourceGroups
ResourceSettingTargetResourceName       : psdemorm2
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm
SourceResourceSettingResourceType       : resourceGroups
SourceResourceSettingTargetResourceName : psdemorm
Target                                  :
TargetId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/psdemorm2
Type                                    :

```

<span data-ttu-id="ff295-111">Uzyskiwanie szczegółowych informacji o wszystkich zasobach w kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="ff295-111">Get details of all the resources in the move collection.</span></span>

### <span data-ttu-id="ff295-112">Przykład 2: uzyskiwanie szczegółowych informacji o określonych zasobach w kolekcji przenoszenia przy użyciu funkcji Przenieś nazwę zasobu.</span><span class="sxs-lookup"><span data-stu-id="ff295-112">Example 2: Get details of a specific resources in a Move collection using move resource name .</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM -Name PSDemoVM   
                                                     
Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

```

<span data-ttu-id="ff295-113">Uzyskiwanie szczegółowych informacji o określonych zasobach w kolekcji przenoszenia za pomocą funkcji Przenieś nazwę zasobu.</span><span class="sxs-lookup"><span data-stu-id="ff295-113">Get details of a specific resources in a Move collection using move resource name .</span></span>

### <span data-ttu-id="ff295-114">Przykład 3: uzyskiwanie szczegółowych informacji o określonych zasobach w kolekcji przenoszenia przy użyciu filtrów, takich jak SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState.</span><span class="sxs-lookup"><span data-stu-id="ff295-114">Example 3:Get details of a specific resources in a Move collection using filters such as : SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM -Filter "Properties/SourceResourceName eq 'PSDemoVM'"

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

```

<span data-ttu-id="ff295-115">Aby uzyskać szczegółowe informacje o określonych zasobach w kolekcji przenoszenia, Użyj filtru, takiego jak armid, moveStatusMoveState (verify) itp.</span><span class="sxs-lookup"><span data-stu-id="ff295-115">Get details of a specific resources in a Move collection using filter such as armid ,moveStatusMoveState(verify) etc.</span></span>

## <span data-ttu-id="ff295-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff295-116">PARAMETERS</span></span>

### <span data-ttu-id="ff295-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff295-117">-DefaultProfile</span></span>
<span data-ttu-id="ff295-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff295-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff295-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="ff295-119">-Filter</span></span>
<span data-ttu-id="ff295-120">Filtr, który ma zostać zastosowany do operacji.</span><span class="sxs-lookup"><span data-stu-id="ff295-120">The filter to apply on the operation.</span></span>
<span data-ttu-id="ff295-121">Można na przykład użyć $filter = Properties/ProvisioningState EQ '.</span><span class="sxs-lookup"><span data-stu-id="ff295-121">For example, you can use $filter=Properties/ProvisioningState eq 'Succeeded'.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff295-122">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ff295-122">-MoveCollectionName</span></span>
<span data-ttu-id="ff295-123">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="ff295-123">The Move Collection Name.</span></span>

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

### <span data-ttu-id="ff295-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ff295-124">-Name</span></span>
<span data-ttu-id="ff295-125">Nazwa przeniesienia zasobu.</span><span class="sxs-lookup"><span data-stu-id="ff295-125">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff295-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff295-126">-ResourceGroupName</span></span>
<span data-ttu-id="ff295-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff295-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ff295-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ff295-128">-SubscriptionId</span></span>
<span data-ttu-id="ff295-129">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="ff295-129">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff295-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff295-130">CommonParameters</span></span>
<span data-ttu-id="ff295-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff295-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff295-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff295-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff295-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff295-133">INPUTS</span></span>

## <span data-ttu-id="ff295-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff295-134">OUTPUTS</span></span>

### <span data-ttu-id="ff295-135">Microsoft. Azure. PowerShell. polecenia. ResourceMover. models. Api20191001Preview. IMoveResource</span><span class="sxs-lookup"><span data-stu-id="ff295-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="ff295-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff295-136">NOTES</span></span>

<span data-ttu-id="ff295-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="ff295-137">ALIASES</span></span>

## <span data-ttu-id="ff295-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff295-138">RELATED LINKS</span></span>

