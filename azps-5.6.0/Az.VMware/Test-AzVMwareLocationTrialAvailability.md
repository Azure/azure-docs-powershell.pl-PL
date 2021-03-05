---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
ms.openlocfilehash: 133dc4dd259025556ab5f8dd3b848ae70a5101c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988625"
---
# <span data-ttu-id="724d4-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="724d4-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="724d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="724d4-102">SYNOPSIS</span></span>
<span data-ttu-id="724d4-103">Zwracanie stanu wersji próbnej dla subskrypcji według regionu</span><span class="sxs-lookup"><span data-stu-id="724d4-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="724d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="724d4-104">SYNTAX</span></span>

### <span data-ttu-id="724d4-105">Sprawdzanie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="724d4-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="724d4-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="724d4-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="724d4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="724d4-107">DESCRIPTION</span></span>
<span data-ttu-id="724d4-108">Zwracanie stanu wersji próbnej dla subskrypcji według regionu</span><span class="sxs-lookup"><span data-stu-id="724d4-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="724d4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="724d4-109">EXAMPLES</span></span>

### <span data-ttu-id="724d4-110">Przykład 1. Sprawdzanie dostępności wersji próbnej</span><span class="sxs-lookup"><span data-stu-id="724d4-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="724d4-111">Sprawdzanie dostępności wersji próbnej</span><span class="sxs-lookup"><span data-stu-id="724d4-111">Check trial availability</span></span>

## <span data-ttu-id="724d4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="724d4-112">PARAMETERS</span></span>

### <span data-ttu-id="724d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724d4-113">-DefaultProfile</span></span>
<span data-ttu-id="724d4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="724d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="724d4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="724d4-115">-InputObject</span></span>
<span data-ttu-id="724d4-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="724d4-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="724d4-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="724d4-117">-Location</span></span>
<span data-ttu-id="724d4-118">Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="724d4-118">Azure region</span></span>

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

### <span data-ttu-id="724d4-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="724d4-119">-SubscriptionId</span></span>
<span data-ttu-id="724d4-120">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="724d4-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="724d4-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="724d4-121">-Confirm</span></span>
<span data-ttu-id="724d4-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="724d4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="724d4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="724d4-123">-WhatIf</span></span>
<span data-ttu-id="724d4-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="724d4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="724d4-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="724d4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="724d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724d4-126">CommonParameters</span></span>
<span data-ttu-id="724d4-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="724d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724d4-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="724d4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724d4-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="724d4-129">INPUTS</span></span>

### <span data-ttu-id="724d4-130">Microsoft.Azure.PowerShell.Cmdlet.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="724d4-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="724d4-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="724d4-131">OUTPUTS</span></span>

### <span data-ttu-id="724d4-132">Microsoft.Azure.PowerShell.cmdlet.VMWare.Models.Api20200320.ITrial</span><span class="sxs-lookup"><span data-stu-id="724d4-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="724d4-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="724d4-133">NOTES</span></span>

<span data-ttu-id="724d4-134">ALIASY</span><span class="sxs-lookup"><span data-stu-id="724d4-134">ALIASES</span></span>

<span data-ttu-id="724d4-135">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="724d4-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="724d4-136">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="724d4-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="724d4-137">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="724d4-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="724d4-138">INPUTOBJECT: <IVMWareIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="724d4-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="724d4-139">`[AuthorizationName <String>]`: nazwa autoryzacji obwodu usługi ExpressRoute w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="724d4-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="724d4-140">`[ClusterName <String>]`: nazwa klastra w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="724d4-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="724d4-141">`[HcxEnterpriseSiteName <String>]`: nazwa witryny HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="724d4-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="724d4-142">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="724d4-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="724d4-143">`[Location <String>]`: region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="724d4-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="724d4-144">`[PrivateCloudName <String>]`: nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="724d4-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="724d4-145">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="724d4-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="724d4-146">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="724d4-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="724d4-147">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="724d4-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="724d4-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="724d4-148">RELATED LINKS</span></span>

