---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 6cfee237c1104a77f0e1790c4980e8eb793a771c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341410"
---
# <span data-ttu-id="36f25-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="36f25-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="36f25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36f25-102">SYNOPSIS</span></span>
<span data-ttu-id="36f25-103">Tworzenie lub aktualizowanie obiektu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36f25-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="36f25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36f25-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36f25-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36f25-105">DESCRIPTION</span></span>
<span data-ttu-id="36f25-106">Tworzenie lub aktualizowanie obiektu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36f25-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="36f25-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36f25-107">EXAMPLES</span></span>

### <span data-ttu-id="36f25-108">Przykład 1: Tworzenie okna aplikacji klasycznego pulpitu systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="36f25-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="36f25-109">To polecenie powoduje utworzenie grupy aplikacji pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="36f25-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="36f25-110">Przykład 2: Tworzenie okna aplikacji klasycznego pulpitu systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="36f25-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="36f25-111">To polecenie powoduje utworzenie grupy aplikacji pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="36f25-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="36f25-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36f25-112">PARAMETERS</span></span>

### <span data-ttu-id="36f25-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="36f25-113">-ApplicationGroupType</span></span>
<span data-ttu-id="36f25-114">Typ zasobu w polu ApplicationName.</span><span class="sxs-lookup"><span data-stu-id="36f25-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="36f25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f25-115">-DefaultProfile</span></span>
<span data-ttu-id="36f25-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36f25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36f25-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="36f25-117">-Description</span></span>
<span data-ttu-id="36f25-118">Opis aplikacji ApplicationName.</span><span class="sxs-lookup"><span data-stu-id="36f25-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="36f25-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="36f25-119">-FriendlyName</span></span>
<span data-ttu-id="36f25-120">Przyjazna nazwa aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36f25-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="36f25-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="36f25-121">-HostPoolArmPath</span></span>
<span data-ttu-id="36f25-122">HostPool ARM ścieżka do aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36f25-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="36f25-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="36f25-123">-Location</span></span>
<span data-ttu-id="36f25-124">Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="36f25-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="36f25-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36f25-125">-Name</span></span>
<span data-ttu-id="36f25-126">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="36f25-126">The name of the application group</span></span>

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

### <span data-ttu-id="36f25-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f25-127">-ResourceGroupName</span></span>
<span data-ttu-id="36f25-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36f25-128">The name of the resource group.</span></span>
<span data-ttu-id="36f25-129">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="36f25-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="36f25-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="36f25-130">-SubscriptionId</span></span>
<span data-ttu-id="36f25-131">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="36f25-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="36f25-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="36f25-132">-Tag</span></span>
<span data-ttu-id="36f25-133">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="36f25-133">Resource tags.</span></span>

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

### <span data-ttu-id="36f25-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36f25-134">-Confirm</span></span>
<span data-ttu-id="36f25-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36f25-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36f25-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36f25-136">-WhatIf</span></span>
<span data-ttu-id="36f25-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36f25-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36f25-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36f25-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36f25-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f25-139">CommonParameters</span></span>
<span data-ttu-id="36f25-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36f25-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f25-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36f25-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f25-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36f25-142">INPUTS</span></span>

## <span data-ttu-id="36f25-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36f25-143">OUTPUTS</span></span>

### <span data-ttu-id="36f25-144">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="36f25-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span></span>

## <span data-ttu-id="36f25-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36f25-145">NOTES</span></span>

<span data-ttu-id="36f25-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="36f25-146">ALIASES</span></span>

## <span data-ttu-id="36f25-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36f25-147">RELATED LINKS</span></span>

