---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 38292351f091528ef4e153f9374dff75ccbfe941
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966154"
---
# <span data-ttu-id="fe005-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="fe005-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="fe005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe005-102">SYNOPSIS</span></span>
<span data-ttu-id="fe005-103">Utwórz lub zaktualizuj grupę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fe005-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="fe005-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe005-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fe005-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe005-105">DESCRIPTION</span></span>
<span data-ttu-id="fe005-106">Utwórz lub zaktualizuj grupę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fe005-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="fe005-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe005-107">EXAMPLES</span></span>

### <span data-ttu-id="fe005-108">Przykład 1. Tworzenie grupy aplikacji pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="fe005-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'RemoteApp'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="fe005-109">To polecenie tworzy grupę aplikacji pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe005-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="fe005-110">Przykład 2. Tworzenie grupy aplikacji pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="fe005-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'Desktop'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="fe005-111">To polecenie tworzy grupę aplikacji pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe005-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="fe005-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe005-112">PARAMETERS</span></span>

### <span data-ttu-id="fe005-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="fe005-113">-ApplicationGroupType</span></span>
<span data-ttu-id="fe005-114">Typ zasobu ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="fe005-114">Resource Type of ApplicationGroup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.ApplicationGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe005-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe005-115">-DefaultProfile</span></span>
<span data-ttu-id="fe005-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe005-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe005-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="fe005-117">-Description</span></span>
<span data-ttu-id="fe005-118">Opis grupy ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="fe005-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="fe005-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fe005-119">-FriendlyName</span></span>
<span data-ttu-id="fe005-120">Przyjazna nazwa grupy ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="fe005-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="fe005-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="fe005-121">-HostPoolArmPath</span></span>
<span data-ttu-id="fe005-122">Ścieżka armPool hosta grupy ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="fe005-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="fe005-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fe005-123">-Location</span></span>
<span data-ttu-id="fe005-124">Lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="fe005-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="fe005-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fe005-125">-Name</span></span>
<span data-ttu-id="fe005-126">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="fe005-126">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe005-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe005-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe005-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe005-128">The name of the resource group.</span></span>
<span data-ttu-id="fe005-129">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="fe005-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fe005-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe005-130">-SubscriptionId</span></span>
<span data-ttu-id="fe005-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="fe005-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fe005-132">— Tag</span><span class="sxs-lookup"><span data-stu-id="fe005-132">-Tag</span></span>
<span data-ttu-id="fe005-133">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe005-133">Resource tags.</span></span>

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

### <span data-ttu-id="fe005-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe005-134">-Confirm</span></span>
<span data-ttu-id="fe005-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fe005-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe005-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe005-136">-WhatIf</span></span>
<span data-ttu-id="fe005-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe005-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe005-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fe005-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe005-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe005-139">CommonParameters</span></span>
<span data-ttu-id="fe005-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe005-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe005-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe005-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe005-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe005-142">INPUTS</span></span>

## <span data-ttu-id="fe005-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe005-143">OUTPUTS</span></span>

### <span data-ttu-id="fe005-144">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="fe005-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="fe005-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe005-145">NOTES</span></span>

<span data-ttu-id="fe005-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fe005-146">ALIASES</span></span>

## <span data-ttu-id="fe005-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe005-147">RELATED LINKS</span></span>

