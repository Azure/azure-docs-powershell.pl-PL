---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: b97db1a21afab939e94b776b3da8d43f3d1468b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238060"
---
# <span data-ttu-id="592a6-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="592a6-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="592a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="592a6-102">SYNOPSIS</span></span>
<span data-ttu-id="592a6-103">Tworzenie lub aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="592a6-103">Create or update a workspace.</span></span>

## <span data-ttu-id="592a6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="592a6-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="592a6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="592a6-105">DESCRIPTION</span></span>
<span data-ttu-id="592a6-106">Tworzenie lub aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="592a6-106">Create or update a workspace.</span></span>

## <span data-ttu-id="592a6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="592a6-107">EXAMPLES</span></span>

### <span data-ttu-id="592a6-108">Przykład 1. Tworzenie obszaru roboczego pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="592a6-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="592a6-109">To polecenie umożliwia utworzenie wirtualnego obszaru roboczego pulpitu systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="592a6-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="592a6-110">Przykład 2. Tworzenie obszaru roboczego pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="592a6-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="592a6-111">To polecenie umożliwia utworzenie wirtualnego obszaru roboczego pulpitu systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="592a6-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="592a6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="592a6-112">PARAMETERS</span></span>

### <span data-ttu-id="592a6-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="592a6-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="592a6-114">Lista identyfikatorów zasobów applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="592a6-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="592a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592a6-115">-DefaultProfile</span></span>
<span data-ttu-id="592a6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="592a6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="592a6-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="592a6-117">-Description</span></span>
<span data-ttu-id="592a6-118">Opis obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="592a6-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="592a6-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="592a6-119">-FriendlyName</span></span>
<span data-ttu-id="592a6-120">Przyjazna nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="592a6-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="592a6-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="592a6-121">-Location</span></span>
<span data-ttu-id="592a6-122">Lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="592a6-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="592a6-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="592a6-123">-Name</span></span>
<span data-ttu-id="592a6-124">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="592a6-124">The name of the workspace</span></span>

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

### <span data-ttu-id="592a6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592a6-125">-ResourceGroupName</span></span>
<span data-ttu-id="592a6-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="592a6-126">The name of the resource group.</span></span>
<span data-ttu-id="592a6-127">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="592a6-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="592a6-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="592a6-128">-SubscriptionId</span></span>
<span data-ttu-id="592a6-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="592a6-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="592a6-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="592a6-130">-Tag</span></span>
<span data-ttu-id="592a6-131">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="592a6-131">Resource tags.</span></span>

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

### <span data-ttu-id="592a6-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="592a6-132">-Confirm</span></span>
<span data-ttu-id="592a6-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="592a6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="592a6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="592a6-134">-WhatIf</span></span>
<span data-ttu-id="592a6-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="592a6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="592a6-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="592a6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="592a6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592a6-137">CommonParameters</span></span>
<span data-ttu-id="592a6-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="592a6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592a6-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="592a6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592a6-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="592a6-140">INPUTS</span></span>

## <span data-ttu-id="592a6-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="592a6-141">OUTPUTS</span></span>

### <span data-ttu-id="592a6-142">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="592a6-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="592a6-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="592a6-143">NOTES</span></span>

<span data-ttu-id="592a6-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="592a6-144">ALIASES</span></span>

## <span data-ttu-id="592a6-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="592a6-145">RELATED LINKS</span></span>

