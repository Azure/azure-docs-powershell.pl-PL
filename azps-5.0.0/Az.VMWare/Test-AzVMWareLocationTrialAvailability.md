---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
ms.openlocfilehash: 942ac0b4a8bca964e88c7dfd327fe460f249a915
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318757"
---
# <span data-ttu-id="17344-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="17344-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="17344-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17344-102">SYNOPSIS</span></span>
<span data-ttu-id="17344-103">Zwrotny status próbny subskrypcji według regionów</span><span class="sxs-lookup"><span data-stu-id="17344-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="17344-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17344-104">SYNTAX</span></span>

### <span data-ttu-id="17344-105">Zaznacz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="17344-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="17344-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="17344-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17344-107">Opis</span><span class="sxs-lookup"><span data-stu-id="17344-107">DESCRIPTION</span></span>
<span data-ttu-id="17344-108">Zwrotny status próbny subskrypcji według regionów</span><span class="sxs-lookup"><span data-stu-id="17344-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="17344-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17344-109">EXAMPLES</span></span>

### <span data-ttu-id="17344-110">Przykład 1. Sprawdź dostępność wersji próbnej</span><span class="sxs-lookup"><span data-stu-id="17344-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="17344-111">Sprawdzanie dostępności wersji próbnej</span><span class="sxs-lookup"><span data-stu-id="17344-111">Check trial availability</span></span>

## <span data-ttu-id="17344-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17344-112">PARAMETERS</span></span>

### <span data-ttu-id="17344-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17344-113">-DefaultProfile</span></span>
<span data-ttu-id="17344-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17344-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17344-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="17344-115">-InputObject</span></span>
<span data-ttu-id="17344-116">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="17344-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="17344-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="17344-117">-Location</span></span>
<span data-ttu-id="17344-118">Obszar Azure</span><span class="sxs-lookup"><span data-stu-id="17344-118">Azure region</span></span>

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

### <span data-ttu-id="17344-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="17344-119">-SubscriptionId</span></span>
<span data-ttu-id="17344-120">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="17344-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="17344-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="17344-121">-Confirm</span></span>
<span data-ttu-id="17344-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17344-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17344-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17344-123">-WhatIf</span></span>
<span data-ttu-id="17344-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17344-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17344-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="17344-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17344-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17344-126">CommonParameters</span></span>
<span data-ttu-id="17344-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17344-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17344-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17344-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17344-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17344-129">INPUTS</span></span>

### <span data-ttu-id="17344-130">Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="17344-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="17344-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17344-131">OUTPUTS</span></span>

### <span data-ttu-id="17344-132">Microsoft. Azure. PowerShell. cmdlet. VMWare. modele. Api20200320. ITrial</span><span class="sxs-lookup"><span data-stu-id="17344-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="17344-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17344-133">NOTES</span></span>

<span data-ttu-id="17344-134">PISUJE</span><span class="sxs-lookup"><span data-stu-id="17344-134">ALIASES</span></span>

<span data-ttu-id="17344-135">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17344-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="17344-136">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="17344-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17344-137">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="17344-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="17344-138">INPUTobject <IVMWareIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="17344-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="17344-139">`[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="17344-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="17344-140">`[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="17344-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="17344-141">`[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="17344-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="17344-142">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="17344-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="17344-143">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="17344-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="17344-144">`[PrivateCloudName <String>]`: Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="17344-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="17344-145">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="17344-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="17344-146">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="17344-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="17344-147">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="17344-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="17344-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17344-148">RELATED LINKS</span></span>

