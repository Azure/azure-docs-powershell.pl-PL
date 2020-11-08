---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: b91332fe8867283b5fff9cbbf1f5df96209fa2f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062261"
---
# <span data-ttu-id="45b61-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="45b61-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="45b61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45b61-102">SYNOPSIS</span></span>
<span data-ttu-id="45b61-103">Tworzenie lub aktualizowanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="45b61-103">Create or update a host pool.</span></span>

## <span data-ttu-id="45b61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45b61-104">SYNTAX</span></span>

### <span data-ttu-id="45b61-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="45b61-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoContext <String>]
 [-Tag <Hashtable>] [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="45b61-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="45b61-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="45b61-107">Opis</span><span class="sxs-lookup"><span data-stu-id="45b61-107">DESCRIPTION</span></span>
<span data-ttu-id="45b61-108">Tworzenie lub aktualizowanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="45b61-108">Create or update a host pool.</span></span>

## <span data-ttu-id="45b61-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45b61-109">EXAMPLES</span></span>

### <span data-ttu-id="45b61-110">Przykład 1. tworzenie pulpitu wirtualnego systemu HostPool według nazwy</span><span class="sxs-lookup"><span data-stu-id="45b61-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Pooled' `
                            -LoadBalancerType 'DepthFirst' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="45b61-111">To polecenie tworzy wirtualny pulpit systemu Windows HostPool w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="45b61-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="45b61-112">Przykład 1. tworzenie pulpitu wirtualnego systemu HostPool według nazwy</span><span class="sxs-lookup"><span data-stu-id="45b61-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Personal' `
                            -LoadBalancerType 'Persistent' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="45b61-113">To polecenie tworzy wirtualny pulpit systemu Windows HostPool w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="45b61-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="45b61-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45b61-114">PARAMETERS</span></span>

### <span data-ttu-id="45b61-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="45b61-115">-CustomRdpProperty</span></span>
<span data-ttu-id="45b61-116">Niestandardowa Właściwość RDP usługi HostPool.</span><span class="sxs-lookup"><span data-stu-id="45b61-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="45b61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b61-117">-DefaultProfile</span></span>
<span data-ttu-id="45b61-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45b61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45b61-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="45b61-119">-Description</span></span>
<span data-ttu-id="45b61-120">Opis HostPool.</span><span class="sxs-lookup"><span data-stu-id="45b61-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="45b61-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="45b61-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="45b61-122">Nazwa grupy aplikacji klasycznej</span><span class="sxs-lookup"><span data-stu-id="45b61-122">Desktop App Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b61-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="45b61-123">-ExpirationTime</span></span>
<span data-ttu-id="45b61-124">Godzina wygaśnięcia tokenu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="45b61-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="45b61-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="45b61-125">-FriendlyName</span></span>
<span data-ttu-id="45b61-126">Przyjazna nazwa HostPool.</span><span class="sxs-lookup"><span data-stu-id="45b61-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="45b61-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="45b61-127">-HostPoolType</span></span>
<span data-ttu-id="45b61-128">Typ HostPool dla komputerów stacjonarnych.</span><span class="sxs-lookup"><span data-stu-id="45b61-128">HostPool type for desktop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.HostPoolType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b61-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="45b61-129">-LoadBalancerType</span></span>
<span data-ttu-id="45b61-130">Typ modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="45b61-130">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b61-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="45b61-131">-Location</span></span>
<span data-ttu-id="45b61-132">Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="45b61-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="45b61-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="45b61-133">-MaxSessionLimit</span></span>
<span data-ttu-id="45b61-134">Limit maksymalnej liczby sesji HostPool.</span><span class="sxs-lookup"><span data-stu-id="45b61-134">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b61-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45b61-135">-Name</span></span>
<span data-ttu-id="45b61-136">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="45b61-136">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b61-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="45b61-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="45b61-138">Typ PersonalDesktopAssignment dla HostPool.</span><span class="sxs-lookup"><span data-stu-id="45b61-138">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b61-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="45b61-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="45b61-140">Typ preferowanego typu grupy aplikacji — domyślnie Grupa aplikacja klasyczna</span><span class="sxs-lookup"><span data-stu-id="45b61-140">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b61-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="45b61-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="45b61-142">Zakodowany ciąg Base64 tokenu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="45b61-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="45b61-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="45b61-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="45b61-144">Typ resetowania tokenu.</span><span class="sxs-lookup"><span data-stu-id="45b61-144">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b61-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45b61-145">-ResourceGroupName</span></span>
<span data-ttu-id="45b61-146">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="45b61-146">The name of the resource group.</span></span>
<span data-ttu-id="45b61-147">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="45b61-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="45b61-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="45b61-148">-Ring</span></span>
<span data-ttu-id="45b61-149">Numer dzwonka HostPool.</span><span class="sxs-lookup"><span data-stu-id="45b61-149">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b61-150">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="45b61-150">-SsoContext</span></span>
<span data-ttu-id="45b61-151">Ścieżka do magazynu kluczy zawierającego klucz tajny ssoContext.</span><span class="sxs-lookup"><span data-stu-id="45b61-151">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="45b61-152">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="45b61-152">-SubscriptionId</span></span>
<span data-ttu-id="45b61-153">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="45b61-153">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="45b61-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="45b61-154">-Tag</span></span>
<span data-ttu-id="45b61-155">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="45b61-155">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b61-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="45b61-156">-ValidationEnvironment</span></span>
<span data-ttu-id="45b61-157">To środowisko sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="45b61-157">Is validation environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b61-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="45b61-158">-VMTemplate</span></span>
<span data-ttu-id="45b61-159">Szablon maszyny wirtualnej na potrzeby konfiguracji sessionhosts w hostpool.</span><span class="sxs-lookup"><span data-stu-id="45b61-159">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="45b61-160">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="45b61-160">-WorkspaceName</span></span>
<span data-ttu-id="45b61-161">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="45b61-161">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b61-162">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45b61-162">-Confirm</span></span>
<span data-ttu-id="45b61-163">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b61-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45b61-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b61-164">-WhatIf</span></span>
<span data-ttu-id="45b61-165">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45b61-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45b61-166">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45b61-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45b61-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b61-167">CommonParameters</span></span>
<span data-ttu-id="45b61-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b61-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b61-169">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45b61-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b61-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45b61-170">INPUTS</span></span>

## <span data-ttu-id="45b61-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45b61-171">OUTPUTS</span></span>

### <span data-ttu-id="45b61-172">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="45b61-172">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="45b61-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45b61-173">NOTES</span></span>

<span data-ttu-id="45b61-174">PISUJE</span><span class="sxs-lookup"><span data-stu-id="45b61-174">ALIASES</span></span>

## <span data-ttu-id="45b61-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45b61-175">RELATED LINKS</span></span>

