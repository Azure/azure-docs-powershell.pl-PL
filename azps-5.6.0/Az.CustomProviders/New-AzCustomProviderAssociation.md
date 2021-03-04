---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: af502cd4115ba9ef7467c15aa09b78e5e33c2337
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998775"
---
# <span data-ttu-id="4fd5b-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="4fd5b-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="4fd5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fd5b-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd5b-103">Tworzenie lub aktualizowanie skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="4fd5b-103">Create or update an association.</span></span>

## <span data-ttu-id="4fd5b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4fd5b-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4fd5b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4fd5b-105">DESCRIPTION</span></span>
<span data-ttu-id="4fd5b-106">Tworzenie lub aktualizowanie skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="4fd5b-106">Create or update an association.</span></span>

## <span data-ttu-id="4fd5b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4fd5b-107">EXAMPLES</span></span>

### <span data-ttu-id="4fd5b-108">Przykład 1. Tworzenie niestandardowego skojarzenia dostawcy</span><span class="sxs-lookup"><span data-stu-id="4fd5b-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="4fd5b-109">Utwórz niestandardowe skojarzenie dostawcy, skojarzony element docelowy provioder musi być poprawnie skonfigurowany z trasą dla "skojarzeń"</span><span class="sxs-lookup"><span data-stu-id="4fd5b-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="4fd5b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fd5b-110">PARAMETERS</span></span>

### <span data-ttu-id="4fd5b-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4fd5b-111">-AsJob</span></span>
<span data-ttu-id="4fd5b-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="4fd5b-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fd5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd5b-113">-DefaultProfile</span></span>
<span data-ttu-id="4fd5b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4fd5b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fd5b-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4fd5b-115">-Name</span></span>
<span data-ttu-id="4fd5b-116">Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="4fd5b-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fd5b-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4fd5b-117">-NoWait</span></span>
<span data-ttu-id="4fd5b-118">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="4fd5b-118">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fd5b-119">— Zakres</span><span class="sxs-lookup"><span data-stu-id="4fd5b-119">-Scope</span></span>
<span data-ttu-id="4fd5b-120">Zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="4fd5b-120">The scope of the association.</span></span>
<span data-ttu-id="4fd5b-121">Zakres może być dowolnym prawidłowym wystąpieniem zasobu REST.</span><span class="sxs-lookup"><span data-stu-id="4fd5b-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="4fd5b-122">Na przykład użyj dla zasobu maszyny wirtualnej '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{machine-name}".</span><span class="sxs-lookup"><span data-stu-id="4fd5b-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="4fd5b-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4fd5b-123">-TargetResourceId</span></span>
<span data-ttu-id="4fd5b-124">Wystąpienie zasobu REST zasobu docelowego dla tego skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="4fd5b-124">The REST resource instance of the target resource for this association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fd5b-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4fd5b-125">-Confirm</span></span>
<span data-ttu-id="4fd5b-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4fd5b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fd5b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fd5b-127">-WhatIf</span></span>
<span data-ttu-id="4fd5b-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fd5b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fd5b-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4fd5b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fd5b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd5b-130">CommonParameters</span></span>
<span data-ttu-id="4fd5b-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd5b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd5b-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fd5b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd5b-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fd5b-133">INPUTS</span></span>

## <span data-ttu-id="4fd5b-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fd5b-134">OUTPUTS</span></span>

### <span data-ttu-id="4fd5b-135">Microsoft.Azure.PowerShell.Cmdlet.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="4fd5b-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="4fd5b-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4fd5b-136">NOTES</span></span>

<span data-ttu-id="4fd5b-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4fd5b-137">ALIASES</span></span>

## <span data-ttu-id="4fd5b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fd5b-138">RELATED LINKS</span></span>

