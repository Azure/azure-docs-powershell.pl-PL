---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 51a889abe0d1842f66a0ed9b17f3b07acd85a54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242970"
---
# <span data-ttu-id="3d3e9-101">Get-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="3d3e9-101">Get-AzVMwareCluster</span></span>

## <span data-ttu-id="3d3e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d3e9-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3e9-103">Uzyskiwanie klastrów według nazwy w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="3d3e9-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="3d3e9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3d3e9-104">SYNTAX</span></span>

### <span data-ttu-id="3d3e9-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3d3e9-105">List (Default)</span></span>
```
Get-AzVMwareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d3e9-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3d3e9-106">Get</span></span>
```
Get-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d3e9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3d3e9-107">GetViaIdentity</span></span>
```
Get-AzVMwareCluster -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3d3e9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3d3e9-108">DESCRIPTION</span></span>
<span data-ttu-id="3d3e9-109">Uzyskiwanie klastrów według nazwy w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="3d3e9-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="3d3e9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3d3e9-110">EXAMPLES</span></span>

### <span data-ttu-id="3d3e9-111">Przykład 1. Uzyskiwanie klastrów</span><span class="sxs-lookup"><span data-stu-id="3d3e9-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="3d3e9-112">Uzyskiwanie klastrów</span><span class="sxs-lookup"><span data-stu-id="3d3e9-112">Get cluster</span></span>

### <span data-ttu-id="3d3e9-113">Przykład 2. Klastry listy</span><span class="sxs-lookup"><span data-stu-id="3d3e9-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="3d3e9-114">Klastry listy</span><span class="sxs-lookup"><span data-stu-id="3d3e9-114">List clusters</span></span>

## <span data-ttu-id="3d3e9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d3e9-115">PARAMETERS</span></span>

### <span data-ttu-id="3d3e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3e9-116">-DefaultProfile</span></span>
<span data-ttu-id="3d3e9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d3e9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d3e9-118">-InputObject</span></span>
<span data-ttu-id="3d3e9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d3e9-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3d3e9-120">-Name</span></span>
<span data-ttu-id="3d3e9-121">Nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="3d3e9-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="3d3e9-122">- PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="3d3e9-122">-PrivateCloudName</span></span>
<span data-ttu-id="3d3e9-123">Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="3d3e9-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="3d3e9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d3e9-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d3e9-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-125">The name of the resource group.</span></span>
<span data-ttu-id="3d3e9-126">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3d3e9-127">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d3e9-127">-SubscriptionId</span></span>
<span data-ttu-id="3d3e9-128">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3d3e9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3e9-129">CommonParameters</span></span>
<span data-ttu-id="3d3e9-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3e9-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d3e9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3e9-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d3e9-132">INPUTS</span></span>

### <span data-ttu-id="3d3e9-133">Microsoft.Azure.PowerShell.Cmdlet.VCmdlet.Models.IVDentIdentity</span><span class="sxs-lookup"><span data-stu-id="3d3e9-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="3d3e9-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d3e9-134">OUTPUTS</span></span>

### <span data-ttu-id="3d3e9-135">Microsoft.Azure.PowerShell.Cmdlet.VCmdlet.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="3d3e9-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="3d3e9-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3d3e9-136">NOTES</span></span>

<span data-ttu-id="3d3e9-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="3d3e9-137">ALIASES</span></span>

<span data-ttu-id="3d3e9-138">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d3e9-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d3e9-139">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d3e9-140">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d3e9-141">INPUTOBJECT: <IVMwareIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="3d3e9-141">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d3e9-142">`[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="3d3e9-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="3d3e9-143">`[ClusterName <String>]`: nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="3d3e9-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="3d3e9-144">`[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="3d3e9-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="3d3e9-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3d3e9-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d3e9-146">`[Location <String>]`: region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3d3e9-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="3d3e9-147">`[PrivateCloudName <String>]`: nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="3d3e9-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="3d3e9-148">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3d3e9-149">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="3d3e9-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="3d3e9-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d3e9-151">RELATED LINKS</span></span>

