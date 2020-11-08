---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221424"
---
# <span data-ttu-id="2be59-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="2be59-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="2be59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2be59-102">SYNOPSIS</span></span>
<span data-ttu-id="2be59-103">Przydział zwrotny dla subskrypcji według regionów</span><span class="sxs-lookup"><span data-stu-id="2be59-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="2be59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2be59-104">SYNTAX</span></span>

### <span data-ttu-id="2be59-105">Zaznacz (domyślne)</span><span class="sxs-lookup"><span data-stu-id="2be59-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2be59-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2be59-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2be59-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2be59-107">DESCRIPTION</span></span>
<span data-ttu-id="2be59-108">Przydział zwrotny dla subskrypcji według regionów</span><span class="sxs-lookup"><span data-stu-id="2be59-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="2be59-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2be59-109">EXAMPLES</span></span>

### <span data-ttu-id="2be59-110">Przykład 1: Sprawdzanie dostępności przydziałów</span><span class="sxs-lookup"><span data-stu-id="2be59-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="2be59-111">Sprawdzanie dostępności przydziałów</span><span class="sxs-lookup"><span data-stu-id="2be59-111">Check quota availability</span></span>

## <span data-ttu-id="2be59-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2be59-112">PARAMETERS</span></span>

### <span data-ttu-id="2be59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be59-113">-DefaultProfile</span></span>
<span data-ttu-id="2be59-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2be59-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2be59-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2be59-115">-InputObject</span></span>
<span data-ttu-id="2be59-116">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2be59-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2be59-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2be59-117">-Location</span></span>
<span data-ttu-id="2be59-118">Obszar Azure</span><span class="sxs-lookup"><span data-stu-id="2be59-118">Azure region</span></span>

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

### <span data-ttu-id="2be59-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2be59-119">-SubscriptionId</span></span>
<span data-ttu-id="2be59-120">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="2be59-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2be59-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2be59-121">-Confirm</span></span>
<span data-ttu-id="2be59-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2be59-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2be59-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2be59-123">-WhatIf</span></span>
<span data-ttu-id="2be59-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2be59-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2be59-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2be59-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2be59-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be59-126">CommonParameters</span></span>
<span data-ttu-id="2be59-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2be59-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be59-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2be59-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be59-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2be59-129">INPUTS</span></span>

### <span data-ttu-id="2be59-130">Microsoft. Azure. PowerShell. cmdlets. VMWare. modele. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="2be59-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="2be59-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2be59-131">OUTPUTS</span></span>

### <span data-ttu-id="2be59-132">Microsoft. Azure. PowerShell. cmdlet. VMWare. modele. Api20200320. IQuota</span><span class="sxs-lookup"><span data-stu-id="2be59-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="2be59-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2be59-133">NOTES</span></span>

<span data-ttu-id="2be59-134">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2be59-134">ALIASES</span></span>

<span data-ttu-id="2be59-135">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2be59-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2be59-136">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2be59-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2be59-137">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2be59-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2be59-138">INPUTobject <IVMWareIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="2be59-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2be59-139">`[AuthorizationName <String>]`: Nazwa autoryzacji obwodu ExpressRoute w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="2be59-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="2be59-140">`[ClusterName <String>]`: Nazwa klastra w prywatnej chmurze</span><span class="sxs-lookup"><span data-stu-id="2be59-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="2be59-141">`[HcxEnterpriseSiteName <String>]`: Nazwa witryny usługi HCX Enterprise w chmurze prywatnej</span><span class="sxs-lookup"><span data-stu-id="2be59-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="2be59-142">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2be59-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2be59-143">`[Location <String>]`: Region platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2be59-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="2be59-144">`[PrivateCloudName <String>]`: Nazwa chmury prywatnej</span><span class="sxs-lookup"><span data-stu-id="2be59-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="2be59-145">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2be59-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2be59-146">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="2be59-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="2be59-147">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="2be59-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="2be59-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2be59-148">RELATED LINKS</span></span>

