---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
ms.openlocfilehash: 707e7e4e702912d4d838913cb7ca030fef914e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197258"
---
# <span data-ttu-id="0f349-101">Get-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="0f349-101">Get-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="0f349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f349-102">SYNOPSIS</span></span>
<span data-ttu-id="0f349-103">Uzyskiwanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f349-103">Get a private cloud</span></span>

## <span data-ttu-id="0f349-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0f349-104">SYNTAX</span></span>

### <span data-ttu-id="0f349-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="0f349-105">List1 (Default)</span></span>
```
Get-AzVMwarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0f349-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="0f349-106">Get</span></span>
```
Get-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0f349-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0f349-107">GetViaIdentity</span></span>
```
Get-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0f349-108">Lista</span><span class="sxs-lookup"><span data-stu-id="0f349-108">List</span></span>
```
Get-AzVMwarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f349-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="0f349-109">DESCRIPTION</span></span>
<span data-ttu-id="0f349-110">Uzyskiwanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f349-110">Get a private cloud</span></span>

## <span data-ttu-id="0f349-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0f349-111">EXAMPLES</span></span>

### <span data-ttu-id="0f349-112">Przykład 1. Lista chmury prywatnej w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0f349-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="0f349-113">Lista chmury prywatnej w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0f349-113">List private cloud under subscription</span></span>

### <span data-ttu-id="0f349-114">Przykład 2. Lista chmury prywatnej w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="0f349-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="0f349-115">Lista chmury prywatnej w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="0f349-115">List private cloud under resource group</span></span>

### <span data-ttu-id="0f349-116">Przykład 3. Uzyskiwanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f349-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="0f349-117">Uzyskiwanie chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f349-117">Get private cloud</span></span>

## <span data-ttu-id="0f349-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f349-118">PARAMETERS</span></span>

### <span data-ttu-id="0f349-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f349-119">-DefaultProfile</span></span>
<span data-ttu-id="0f349-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f349-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f349-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f349-121">-InputObject</span></span>
<span data-ttu-id="0f349-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0f349-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0f349-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0f349-123">-Name</span></span>
<span data-ttu-id="0f349-124">Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f349-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f349-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f349-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f349-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f349-126">The name of the resource group.</span></span>
<span data-ttu-id="0f349-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="0f349-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0f349-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f349-128">-SubscriptionId</span></span>
<span data-ttu-id="0f349-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0f349-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0f349-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f349-130">CommonParameters</span></span>
<span data-ttu-id="0f349-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f349-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f349-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f349-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f349-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f349-133">INPUTS</span></span>

### <span data-ttu-id="0f349-134">Microsoft.Azure.PowerShell.Cmdlet.VCmdlet.Models.IVDentIdentity</span><span class="sxs-lookup"><span data-stu-id="0f349-134">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="0f349-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f349-135">OUTPUTS</span></span>

### <span data-ttu-id="0f349-136">Microsoft.Azure.PowerShell.cmdlet.vLogne.models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="0f349-136">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="0f349-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0f349-137">NOTES</span></span>

<span data-ttu-id="0f349-138">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0f349-138">ALIASES</span></span>

<span data-ttu-id="0f349-139">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f349-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0f349-140">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0f349-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0f349-141">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0f349-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0f349-142">INPUTOBJECT: <IVMwareIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="0f349-142">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0f349-143">`[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f349-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="0f349-144">`[ClusterName <String>]`: nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f349-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="0f349-145">`[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f349-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="0f349-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0f349-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0f349-147">`[Location <String>]`: region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0f349-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="0f349-148">`[PrivateCloudName <String>]`: nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="0f349-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="0f349-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f349-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0f349-150">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="0f349-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="0f349-151">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="0f349-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="0f349-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f349-152">RELATED LINKS</span></span>

