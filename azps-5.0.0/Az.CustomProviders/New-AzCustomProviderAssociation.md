---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306685"
---
# <span data-ttu-id="57f39-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="57f39-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="57f39-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57f39-102">SYNOPSIS</span></span>
<span data-ttu-id="57f39-103">Tworzenie lub aktualizowanie skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="57f39-103">Create or update an association.</span></span>

## <span data-ttu-id="57f39-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57f39-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57f39-105">Opis</span><span class="sxs-lookup"><span data-stu-id="57f39-105">DESCRIPTION</span></span>
<span data-ttu-id="57f39-106">Tworzenie lub aktualizowanie skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="57f39-106">Create or update an association.</span></span>

## <span data-ttu-id="57f39-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57f39-107">EXAMPLES</span></span>

### <span data-ttu-id="57f39-108">Przykład 1. Tworzenie niestandardowego skojarzenia dostawcy</span><span class="sxs-lookup"><span data-stu-id="57f39-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="57f39-109">Tworzenie niestandardowego skojarzenia dostawcy, powiązane provioder docelowe muszą być poprawnie skonfigurowane za pomocą trasy dla "stowarzyszenia"</span><span class="sxs-lookup"><span data-stu-id="57f39-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="57f39-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57f39-110">PARAMETERS</span></span>

### <span data-ttu-id="57f39-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57f39-111">-AsJob</span></span>
<span data-ttu-id="57f39-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="57f39-112">Run the command as a job</span></span>

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

### <span data-ttu-id="57f39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f39-113">-DefaultProfile</span></span>
<span data-ttu-id="57f39-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57f39-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57f39-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57f39-115">-Name</span></span>
<span data-ttu-id="57f39-116">Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="57f39-116">The name of the association.</span></span>

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

### <span data-ttu-id="57f39-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="57f39-117">-NoWait</span></span>
<span data-ttu-id="57f39-118">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="57f39-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="57f39-119">-Zakres</span><span class="sxs-lookup"><span data-stu-id="57f39-119">-Scope</span></span>
<span data-ttu-id="57f39-120">Zakres skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="57f39-120">The scope of the association.</span></span>
<span data-ttu-id="57f39-121">Zakres może być dowolną prawidłową instancją zasobu w usłudze w spoczynku.</span><span class="sxs-lookup"><span data-stu-id="57f39-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="57f39-122">Na przykład użyj "/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}" dla zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57f39-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="57f39-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="57f39-123">-TargetResourceId</span></span>
<span data-ttu-id="57f39-124">Wystąpienie zasobu usługi współpracy nad zasobem docelowym dla tego skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="57f39-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="57f39-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57f39-125">-Confirm</span></span>
<span data-ttu-id="57f39-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57f39-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57f39-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f39-127">-WhatIf</span></span>
<span data-ttu-id="57f39-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57f39-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57f39-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57f39-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57f39-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f39-130">CommonParameters</span></span>
<span data-ttu-id="57f39-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f39-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f39-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57f39-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f39-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57f39-133">INPUTS</span></span>

## <span data-ttu-id="57f39-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57f39-134">OUTPUTS</span></span>

### <span data-ttu-id="57f39-135">Microsoft. Azure. PowerShell. polecenia. CustomProviders. models. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="57f39-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="57f39-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57f39-136">NOTES</span></span>

<span data-ttu-id="57f39-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="57f39-137">ALIASES</span></span>

## <span data-ttu-id="57f39-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57f39-138">RELATED LINKS</span></span>

