---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: fbd71d03c6f82bcb785105d9d75e155e9f7ef498
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304776"
---
# <span data-ttu-id="7dac1-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="7dac1-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="7dac1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7dac1-102">SYNOPSIS</span></span>
<span data-ttu-id="7dac1-103">Tworzenie lub aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7dac1-103">Create or update a workspace.</span></span>

## <span data-ttu-id="7dac1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7dac1-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7dac1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7dac1-105">DESCRIPTION</span></span>
<span data-ttu-id="7dac1-106">Tworzenie lub aktualizowanie obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7dac1-106">Create or update a workspace.</span></span>

## <span data-ttu-id="7dac1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7dac1-107">EXAMPLES</span></span>

### <span data-ttu-id="7dac1-108">Przykład 1. tworzenie pulpitu wirtualnego systemu Worksapce według nazwy</span><span class="sxs-lookup"><span data-stu-id="7dac1-108">Example 1: Create a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="7dac1-109">To polecenie tworzy obszar roboczy pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7dac1-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="7dac1-110">Przykład 2: tworzenie pulpitu wirtualnego systemu Worksapce według nazwy</span><span class="sxs-lookup"><span data-stu-id="7dac1-110">Example 2: Create a Windows Virtual Desktop Worksapce by name</span></span>
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

<span data-ttu-id="7dac1-111">To polecenie tworzy obszar roboczy pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7dac1-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="7dac1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7dac1-112">PARAMETERS</span></span>

### <span data-ttu-id="7dac1-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="7dac1-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="7dac1-114">Lista identyfikatorów zasobów aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7dac1-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="7dac1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dac1-115">-DefaultProfile</span></span>
<span data-ttu-id="7dac1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7dac1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dac1-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="7dac1-117">-Description</span></span>
<span data-ttu-id="7dac1-118">Opis obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7dac1-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="7dac1-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7dac1-119">-FriendlyName</span></span>
<span data-ttu-id="7dac1-120">Przyjazna nazwa obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="7dac1-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="7dac1-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7dac1-121">-Location</span></span>
<span data-ttu-id="7dac1-122">Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="7dac1-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="7dac1-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7dac1-123">-Name</span></span>
<span data-ttu-id="7dac1-124">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="7dac1-124">The name of the workspace</span></span>

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

### <span data-ttu-id="7dac1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dac1-125">-ResourceGroupName</span></span>
<span data-ttu-id="7dac1-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7dac1-126">The name of the resource group.</span></span>
<span data-ttu-id="7dac1-127">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="7dac1-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7dac1-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7dac1-128">-SubscriptionId</span></span>
<span data-ttu-id="7dac1-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="7dac1-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7dac1-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="7dac1-130">-Tag</span></span>
<span data-ttu-id="7dac1-131">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="7dac1-131">Resource tags.</span></span>

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

### <span data-ttu-id="7dac1-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7dac1-132">-Confirm</span></span>
<span data-ttu-id="7dac1-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dac1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dac1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dac1-134">-WhatIf</span></span>
<span data-ttu-id="7dac1-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dac1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dac1-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7dac1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dac1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dac1-137">CommonParameters</span></span>
<span data-ttu-id="7dac1-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dac1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dac1-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7dac1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dac1-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dac1-140">INPUTS</span></span>

## <span data-ttu-id="7dac1-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7dac1-141">OUTPUTS</span></span>

### <span data-ttu-id="7dac1-142">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="7dac1-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="7dac1-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7dac1-143">NOTES</span></span>

<span data-ttu-id="7dac1-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7dac1-144">ALIASES</span></span>

## <span data-ttu-id="7dac1-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dac1-145">RELATED LINKS</span></span>

