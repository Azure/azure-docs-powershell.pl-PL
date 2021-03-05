---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 8382358e6bad15948ed8cdfeb904cf8c431bd131
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991635"
---
# <span data-ttu-id="e5f87-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="e5f87-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="e5f87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5f87-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f87-103">Utwórz nową usługę CommunicationService lub zaktualizuj istniejącą usługę CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="e5f87-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="e5f87-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e5f87-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e5f87-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e5f87-105">DESCRIPTION</span></span>
<span data-ttu-id="e5f87-106">Utwórz nową usługę CommunicationService lub zaktualizuj istniejącą usługę CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="e5f87-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="e5f87-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e5f87-107">EXAMPLES</span></span>

### <span data-ttu-id="e5f87-108">Przykład 1. Tworzenie zasobu ACS</span><span class="sxs-lookup"><span data-stu-id="e5f87-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="e5f87-109">Tworzy zasób ACS przy użyciu określonych parametrów.</span><span class="sxs-lookup"><span data-stu-id="e5f87-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="e5f87-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5f87-110">PARAMETERS</span></span>

### <span data-ttu-id="e5f87-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e5f87-111">-AsJob</span></span>
<span data-ttu-id="e5f87-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e5f87-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e5f87-113">-DataLocation</span><span class="sxs-lookup"><span data-stu-id="e5f87-113">-DataLocation</span></span>
<span data-ttu-id="e5f87-114">Lokalizacja, w której usługa komunikacji przechowuje swoje dane w spoczynku.</span><span class="sxs-lookup"><span data-stu-id="e5f87-114">The location where the communication service stores its data at rest.</span></span>

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

### <span data-ttu-id="e5f87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f87-115">-DefaultProfile</span></span>
<span data-ttu-id="e5f87-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5f87-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5f87-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e5f87-117">-Location</span></span>
<span data-ttu-id="e5f87-118">Lokalizacja platformy Azure, w której jest uruchomiona usługa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="e5f87-118">The Azure location where the CommunicationService is running.</span></span>

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

### <span data-ttu-id="e5f87-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e5f87-119">-Name</span></span>
<span data-ttu-id="e5f87-120">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="e5f87-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f87-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e5f87-121">-NoWait</span></span>
<span data-ttu-id="e5f87-122">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e5f87-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e5f87-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5f87-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5f87-124">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="e5f87-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e5f87-125">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="e5f87-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e5f87-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5f87-126">-SubscriptionId</span></span>
<span data-ttu-id="e5f87-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e5f87-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e5f87-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="e5f87-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e5f87-129">— Tag</span><span class="sxs-lookup"><span data-stu-id="e5f87-129">-Tag</span></span>
<span data-ttu-id="e5f87-130">Tagi usługi, która jest listą kluczy par wartości opisujących zasób.</span><span class="sxs-lookup"><span data-stu-id="e5f87-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f87-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5f87-131">-Confirm</span></span>
<span data-ttu-id="e5f87-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e5f87-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5f87-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f87-133">-WhatIf</span></span>
<span data-ttu-id="e5f87-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5f87-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5f87-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e5f87-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5f87-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f87-136">CommonParameters</span></span>
<span data-ttu-id="e5f87-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5f87-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f87-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5f87-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f87-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5f87-139">INPUTS</span></span>

## <span data-ttu-id="e5f87-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5f87-140">OUTPUTS</span></span>

### <span data-ttu-id="e5f87-141">Microsoft.Azure.PowerShell.cmdlet.Communication.Models.Api200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="e5f87-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="e5f87-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e5f87-142">NOTES</span></span>

<span data-ttu-id="e5f87-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="e5f87-143">ALIASES</span></span>

## <span data-ttu-id="e5f87-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5f87-144">RELATED LINKS</span></span>

