---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
ms.openlocfilehash: f667e5f2c6f85e06e1d16a35b1279d88af5e2ed7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195498"
---
# <span data-ttu-id="8d627-101">Test-AzVMwareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="8d627-101">Test-AzVMwareLocationTrialAvailability</span></span>

## <span data-ttu-id="8d627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d627-102">SYNOPSIS</span></span>
<span data-ttu-id="8d627-103">Zwracanie stanu wersji próbnej dla subskrypcji według regionu</span><span class="sxs-lookup"><span data-stu-id="8d627-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="8d627-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8d627-104">SYNTAX</span></span>

### <span data-ttu-id="8d627-105">Sprawdzanie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8d627-105">Check (Default)</span></span>
```
Test-AzVMwareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d627-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d627-106">CheckViaIdentity</span></span>
```
Test-AzVMwareLocationTrialAvailability -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d627-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8d627-107">DESCRIPTION</span></span>
<span data-ttu-id="8d627-108">Zwracanie stanu wersji próbnej dla subskrypcji według regionu</span><span class="sxs-lookup"><span data-stu-id="8d627-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="8d627-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8d627-109">EXAMPLES</span></span>

### <span data-ttu-id="8d627-110">Przykład 1. Sprawdzanie dostępności wersji próbnej</span><span class="sxs-lookup"><span data-stu-id="8d627-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMwareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="8d627-111">Sprawdzanie dostępności wersji próbnej</span><span class="sxs-lookup"><span data-stu-id="8d627-111">Check trial availability</span></span>

## <span data-ttu-id="8d627-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d627-112">PARAMETERS</span></span>

### <span data-ttu-id="8d627-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d627-113">-DefaultProfile</span></span>
<span data-ttu-id="8d627-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d627-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d627-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d627-115">-InputObject</span></span>
<span data-ttu-id="8d627-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8d627-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d627-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8d627-117">-Location</span></span>
<span data-ttu-id="8d627-118">Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8d627-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d627-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d627-119">-SubscriptionId</span></span>
<span data-ttu-id="8d627-120">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8d627-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d627-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d627-121">-Confirm</span></span>
<span data-ttu-id="8d627-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8d627-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d627-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d627-123">-WhatIf</span></span>
<span data-ttu-id="8d627-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d627-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d627-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8d627-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d627-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d627-126">CommonParameters</span></span>
<span data-ttu-id="8d627-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d627-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d627-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d627-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d627-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d627-129">INPUTS</span></span>

### <span data-ttu-id="8d627-130">Microsoft.Azure.PowerShell.Cmdlet.VCmdlet.Models.IVDentIdentity</span><span class="sxs-lookup"><span data-stu-id="8d627-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="8d627-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d627-131">OUTPUTS</span></span>

### <span data-ttu-id="8d627-132">Microsoft.Azure.PowerShell.cmdlet.v Jak.model.api20200320.iTrial</span><span class="sxs-lookup"><span data-stu-id="8d627-132">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="8d627-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8d627-133">NOTES</span></span>

<span data-ttu-id="8d627-134">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8d627-134">ALIASES</span></span>

<span data-ttu-id="8d627-135">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="8d627-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d627-136">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8d627-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d627-137">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8d627-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d627-138">INPUTOBJECT: <IVMwareIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="8d627-138">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d627-139">`[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="8d627-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="8d627-140">`[ClusterName <String>]`: nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="8d627-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="8d627-141">`[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="8d627-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="8d627-142">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8d627-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d627-143">`[Location <String>]`: region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8d627-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="8d627-144">`[PrivateCloudName <String>]`: nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="8d627-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="8d627-145">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d627-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8d627-146">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="8d627-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="8d627-147">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="8d627-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="8d627-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d627-148">RELATED LINKS</span></span>

