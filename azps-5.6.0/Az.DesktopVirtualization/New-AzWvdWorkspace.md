---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: 9335bb4c3177fa405d65038255f43dbba5fb88fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966081"
---
# <span data-ttu-id="78a50-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="78a50-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="78a50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78a50-102">SYNOPSIS</span></span>
<span data-ttu-id="78a50-103">Tworzenie lub aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="78a50-103">Create or update a workspace.</span></span>

## <span data-ttu-id="78a50-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="78a50-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="78a50-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="78a50-105">DESCRIPTION</span></span>
<span data-ttu-id="78a50-106">Tworzenie lub aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="78a50-106">Create or update a workspace.</span></span>

## <span data-ttu-id="78a50-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="78a50-107">EXAMPLES</span></span>

### <span data-ttu-id="78a50-108">Przykład 1. Tworzenie obszaru roboczego pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="78a50-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference $null `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="78a50-109">To polecenie umożliwia utworzenie wirtualnego obszaru roboczego pulpitu systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="78a50-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="78a50-110">Przykład 2. Tworzenie obszaru roboczego pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="78a50-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="78a50-111">To polecenie umożliwia utworzenie wirtualnego obszaru roboczego pulpitu systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="78a50-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="78a50-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78a50-112">PARAMETERS</span></span>

### <span data-ttu-id="78a50-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="78a50-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="78a50-114">Lista identyfikatorów zasobów grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="78a50-114">List of applicationGroup resource Ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a50-115">-DefaultProfile</span></span>
<span data-ttu-id="78a50-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="78a50-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78a50-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="78a50-117">-Description</span></span>
<span data-ttu-id="78a50-118">Opis obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="78a50-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="78a50-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="78a50-119">-FriendlyName</span></span>
<span data-ttu-id="78a50-120">Przyjazna nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="78a50-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="78a50-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="78a50-121">-Location</span></span>
<span data-ttu-id="78a50-122">Lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="78a50-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="78a50-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="78a50-123">-Name</span></span>
<span data-ttu-id="78a50-124">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="78a50-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a50-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a50-125">-ResourceGroupName</span></span>
<span data-ttu-id="78a50-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78a50-126">The name of the resource group.</span></span>
<span data-ttu-id="78a50-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="78a50-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="78a50-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78a50-128">-SubscriptionId</span></span>
<span data-ttu-id="78a50-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="78a50-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="78a50-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="78a50-130">-Tag</span></span>
<span data-ttu-id="78a50-131">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="78a50-131">Resource tags.</span></span>

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

### <span data-ttu-id="78a50-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78a50-132">-Confirm</span></span>
<span data-ttu-id="78a50-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="78a50-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78a50-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78a50-134">-WhatIf</span></span>
<span data-ttu-id="78a50-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78a50-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78a50-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="78a50-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78a50-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a50-137">CommonParameters</span></span>
<span data-ttu-id="78a50-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a50-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a50-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78a50-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a50-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78a50-140">INPUTS</span></span>

## <span data-ttu-id="78a50-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78a50-141">OUTPUTS</span></span>

### <span data-ttu-id="78a50-142">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="78a50-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="78a50-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="78a50-143">NOTES</span></span>

<span data-ttu-id="78a50-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="78a50-144">ALIASES</span></span>

## <span data-ttu-id="78a50-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78a50-145">RELATED LINKS</span></span>

