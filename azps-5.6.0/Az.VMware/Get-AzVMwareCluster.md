---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 842d0c26d4034a8c07415dfe8524b32623c07e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987197"
---
# <span data-ttu-id="744e6-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="744e6-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="744e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="744e6-102">SYNOPSIS</span></span>
<span data-ttu-id="744e6-103">Uzyskiwanie klastrów według nazwy w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="744e6-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="744e6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="744e6-104">SYNTAX</span></span>

### <span data-ttu-id="744e6-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="744e6-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="744e6-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="744e6-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="744e6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="744e6-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="744e6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="744e6-108">DESCRIPTION</span></span>
<span data-ttu-id="744e6-109">Uzyskiwanie klastrów według nazwy w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="744e6-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="744e6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="744e6-110">EXAMPLES</span></span>

### <span data-ttu-id="744e6-111">Przykład 1. Uzyskiwanie klastrów</span><span class="sxs-lookup"><span data-stu-id="744e6-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="744e6-112">Uzyskiwanie klastrów</span><span class="sxs-lookup"><span data-stu-id="744e6-112">Get cluster</span></span>

### <span data-ttu-id="744e6-113">Przykład 2. Klastry listy</span><span class="sxs-lookup"><span data-stu-id="744e6-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="744e6-114">Klastry listy</span><span class="sxs-lookup"><span data-stu-id="744e6-114">List clusters</span></span>

## <span data-ttu-id="744e6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="744e6-115">PARAMETERS</span></span>

### <span data-ttu-id="744e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744e6-116">-DefaultProfile</span></span>
<span data-ttu-id="744e6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="744e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="744e6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="744e6-118">-InputObject</span></span>
<span data-ttu-id="744e6-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="744e6-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="744e6-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="744e6-120">-Name</span></span>
<span data-ttu-id="744e6-121">Nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="744e6-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744e6-122">- PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="744e6-122">-PrivateCloudName</span></span>
<span data-ttu-id="744e6-123">Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="744e6-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="744e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="744e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="744e6-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="744e6-125">The name of the resource group.</span></span>
<span data-ttu-id="744e6-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="744e6-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="744e6-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="744e6-127">-SubscriptionId</span></span>
<span data-ttu-id="744e6-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="744e6-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="744e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744e6-129">CommonParameters</span></span>
<span data-ttu-id="744e6-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="744e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744e6-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="744e6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744e6-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="744e6-132">INPUTS</span></span>

### <span data-ttu-id="744e6-133">Microsoft.Azure.PowerShell.Cmdlet.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="744e6-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="744e6-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="744e6-134">OUTPUTS</span></span>

### <span data-ttu-id="744e6-135">Microsoft.Azure.PowerShell.Cmdlet.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="744e6-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="744e6-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="744e6-136">NOTES</span></span>

<span data-ttu-id="744e6-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="744e6-137">ALIASES</span></span>

<span data-ttu-id="744e6-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="744e6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="744e6-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="744e6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="744e6-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="744e6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="744e6-141">INPUTOBJECT: <IVMWareIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="744e6-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="744e6-142">`[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="744e6-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="744e6-143">`[ClusterName <String>]`: nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="744e6-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="744e6-144">`[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="744e6-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="744e6-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="744e6-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="744e6-146">`[Location <String>]`: region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="744e6-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="744e6-147">`[PrivateCloudName <String>]`: nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="744e6-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="744e6-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="744e6-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="744e6-149">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="744e6-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="744e6-150">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="744e6-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="744e6-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="744e6-151">RELATED LINKS</span></span>

