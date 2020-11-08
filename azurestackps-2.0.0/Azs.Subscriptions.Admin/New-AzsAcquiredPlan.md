---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 0db0f7ae4358e49ff62f94132701be1f4bd4d0b7
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/22/2020
ms.locfileid: "94054112"
---
# <span data-ttu-id="3f4da-101">New-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="3f4da-101">New-AzsAcquiredPlan</span></span>

## <span data-ttu-id="3f4da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f4da-102">SYNOPSIS</span></span>


## <span data-ttu-id="3f4da-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f4da-103">SYNTAX</span></span>

### <span data-ttu-id="3f4da-104">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3f4da-104">CreateExpanded (Default)</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> [-PlanAcquisitionId <String>] [-SubscriptionId <String>]
 [-AcquisitionTime <DateTime>] [-ExternalReferenceId <String>] [-Id <String>] [-PlanId <String>]
 [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3f4da-105">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="3f4da-105">Create</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> -AcquiredPlanDefinition <IPlanAcquisition>
 [-PlanAcquisitionId <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3f4da-106">Opis</span><span class="sxs-lookup"><span data-stu-id="3f4da-106">DESCRIPTION</span></span>


## <span data-ttu-id="3f4da-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f4da-107">EXAMPLES</span></span>

### <span data-ttu-id="3f4da-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3f4da-108">Example 1</span></span>
```powershell
PS C:\> New-AzsAcquiredPlan -PlanAcquisitionId $([Guid]::NewGuid()) -PlanId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="3f4da-109">Utwórz plan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="3f4da-109">Create a subscription plan.</span></span>

## <span data-ttu-id="3f4da-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f4da-110">PARAMETERS</span></span>

### <span data-ttu-id="3f4da-111">-AcquiredPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="3f4da-111">-AcquiredPlanDefinition</span></span>
<span data-ttu-id="3f4da-112">Aby skonstruować, zobacz sekcję notatki dla właściwości ACQUIREDPLANDEFINITION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="3f4da-112">To construct, see NOTES section for ACQUIREDPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3f4da-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="3f4da-113">-AcquisitionTime</span></span>


```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f4da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4da-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="3f4da-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="3f4da-115">-ExternalReferenceId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f4da-116">-ID</span><span class="sxs-lookup"><span data-stu-id="3f4da-116">-Id</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f4da-117">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="3f4da-117">-PlanAcquisitionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f4da-118">-PlanId</span><span class="sxs-lookup"><span data-stu-id="3f4da-118">-PlanId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f4da-119">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="3f4da-119">-ProvisioningState</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f4da-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3f4da-120">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f4da-121">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f4da-121">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="3f4da-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3f4da-122">-Confirm</span></span>
<span data-ttu-id="3f4da-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f4da-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f4da-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f4da-124">-WhatIf</span></span>
<span data-ttu-id="3f4da-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f4da-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f4da-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3f4da-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f4da-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4da-127">CommonParameters</span></span>
<span data-ttu-id="3f4da-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f4da-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4da-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f4da-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4da-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f4da-130">INPUTS</span></span>

### <span data-ttu-id="3f4da-131">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="3f4da-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

## <span data-ttu-id="3f4da-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f4da-132">OUTPUTS</span></span>

### <span data-ttu-id="3f4da-133">Microsoft. Azure. PowerShell. polecenia. SubscriptionsAdmin. models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="3f4da-133">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="3f4da-134">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3f4da-134">ALIASES</span></span>

<span data-ttu-id="3f4da-135">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="3f4da-135">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="3f4da-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f4da-136">NOTES</span></span>

<span data-ttu-id="3f4da-137">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3f4da-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f4da-138">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3f4da-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3f4da-139">ACQUIREDPLANDEFINITION <IPlanAcquisition> :</span><span class="sxs-lookup"><span data-stu-id="3f4da-139">ACQUIREDPLANDEFINITION <IPlanAcquisition>:</span></span> 
  - <span data-ttu-id="3f4da-140">`[AcquisitionId <String>]`: Identyfikator nabycia.</span><span class="sxs-lookup"><span data-stu-id="3f4da-140">`[AcquisitionId <String>]`: Acquisition identifier.</span></span>
  - <span data-ttu-id="3f4da-141">`[AcquisitionTime <DateTime?>]`: Czas nabycia.</span><span class="sxs-lookup"><span data-stu-id="3f4da-141">`[AcquisitionTime <DateTime?>]`: Acquisition time.</span></span>
  - <span data-ttu-id="3f4da-142">`[ExternalReferenceId <String>]`: Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="3f4da-142">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="3f4da-143">`[Id <String>]`: Identyfikator w kontekście subskrypcji dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="3f4da-143">`[Id <String>]`: Identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="3f4da-144">`[PlanId <String>]`: Identyfikator planu w kontekście subskrypcji dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="3f4da-144">`[PlanId <String>]`: Plan identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="3f4da-145">`[ProvisioningState <ProvisioningState?>]`: Stan aprowizacji.</span><span class="sxs-lookup"><span data-stu-id="3f4da-145">`[ProvisioningState <ProvisioningState?>]`: State of the provisioning.</span></span>

## <span data-ttu-id="3f4da-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f4da-146">RELATED LINKS</span></span>

