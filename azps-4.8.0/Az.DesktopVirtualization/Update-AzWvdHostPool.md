---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: ffb38dd20c5bc43c3d243e5a6f320fdc5d48d008
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062783"
---
# <span data-ttu-id="b27df-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="b27df-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="b27df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b27df-102">SYNOPSIS</span></span>
<span data-ttu-id="b27df-103">Aktualizowanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="b27df-103">Update a host pool.</span></span>

## <span data-ttu-id="b27df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b27df-104">SYNTAX</span></span>

### <span data-ttu-id="b27df-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b27df-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b27df-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b27df-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b27df-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b27df-107">DESCRIPTION</span></span>
<span data-ttu-id="b27df-108">Aktualizowanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="b27df-108">Update a host pool.</span></span>

## <span data-ttu-id="b27df-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b27df-109">EXAMPLES</span></span>

### <span data-ttu-id="b27df-110">Przykład 1: aktualizowanie HostPool pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="b27df-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Update-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -LoadBalancerType 'BreadthFirst' `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 6 `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="b27df-111">To polecenie aktualizuje HostPool pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b27df-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="b27df-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b27df-112">PARAMETERS</span></span>

### <span data-ttu-id="b27df-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="b27df-113">-CustomRdpProperty</span></span>
<span data-ttu-id="b27df-114">Niestandardowa Właściwość RDP usługi HostPool.</span><span class="sxs-lookup"><span data-stu-id="b27df-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="b27df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27df-115">-DefaultProfile</span></span>
<span data-ttu-id="b27df-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b27df-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b27df-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="b27df-117">-Description</span></span>
<span data-ttu-id="b27df-118">Opis HostPool.</span><span class="sxs-lookup"><span data-stu-id="b27df-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="b27df-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b27df-119">-FriendlyName</span></span>
<span data-ttu-id="b27df-120">Przyjazna nazwa HostPool.</span><span class="sxs-lookup"><span data-stu-id="b27df-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="b27df-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b27df-121">-InputObject</span></span>
<span data-ttu-id="b27df-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b27df-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b27df-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="b27df-123">-LoadBalancerType</span></span>
<span data-ttu-id="b27df-124">Typ modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b27df-124">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27df-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="b27df-125">-MaxSessionLimit</span></span>
<span data-ttu-id="b27df-126">Limit maksymalnej liczby sesji HostPool.</span><span class="sxs-lookup"><span data-stu-id="b27df-126">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27df-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b27df-127">-Name</span></span>
<span data-ttu-id="b27df-128">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="b27df-128">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27df-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="b27df-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="b27df-130">Typ PersonalDesktopAssignment dla HostPool.</span><span class="sxs-lookup"><span data-stu-id="b27df-130">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27df-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="b27df-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="b27df-132">Typ preferowanego typu grupy aplikacji — domyślnie Grupa aplikacja klasyczna</span><span class="sxs-lookup"><span data-stu-id="b27df-132">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27df-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="b27df-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="b27df-134">Godzina wygaśnięcia tokenu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="b27df-134">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27df-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="b27df-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="b27df-136">Typ resetowania tokenu.</span><span class="sxs-lookup"><span data-stu-id="b27df-136">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27df-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b27df-137">-ResourceGroupName</span></span>
<span data-ttu-id="b27df-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b27df-138">The name of the resource group.</span></span>
<span data-ttu-id="b27df-139">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="b27df-139">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27df-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="b27df-140">-Ring</span></span>
<span data-ttu-id="b27df-141">Numer dzwonka HostPool.</span><span class="sxs-lookup"><span data-stu-id="b27df-141">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27df-142">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="b27df-142">-SsoContext</span></span>
<span data-ttu-id="b27df-143">Ścieżka do magazynu kluczy zawierającego klucz tajny ssoContext.</span><span class="sxs-lookup"><span data-stu-id="b27df-143">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="b27df-144">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b27df-144">-SubscriptionId</span></span>
<span data-ttu-id="b27df-145">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b27df-145">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27df-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="b27df-146">-Tag</span></span>
<span data-ttu-id="b27df-147">Tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="b27df-147">tags to be updated</span></span>

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

### <span data-ttu-id="b27df-148">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="b27df-148">-ValidationEnvironment</span></span>
<span data-ttu-id="b27df-149">To środowisko sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="b27df-149">Is validation environment.</span></span>

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

### <span data-ttu-id="b27df-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b27df-150">-Confirm</span></span>
<span data-ttu-id="b27df-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b27df-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b27df-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b27df-152">-WhatIf</span></span>
<span data-ttu-id="b27df-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b27df-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b27df-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b27df-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b27df-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27df-155">CommonParameters</span></span>
<span data-ttu-id="b27df-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b27df-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27df-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b27df-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27df-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b27df-158">INPUTS</span></span>

### <span data-ttu-id="b27df-159">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b27df-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b27df-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b27df-160">OUTPUTS</span></span>

### <span data-ttu-id="b27df-161">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="b27df-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="b27df-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b27df-162">NOTES</span></span>

<span data-ttu-id="b27df-163">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b27df-163">ALIASES</span></span>

<span data-ttu-id="b27df-164">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b27df-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b27df-165">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b27df-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b27df-166">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b27df-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b27df-167">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b27df-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b27df-168">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b27df-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b27df-169">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="b27df-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b27df-170">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="b27df-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b27df-171">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="b27df-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b27df-172">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b27df-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b27df-173">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b27df-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b27df-174">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="b27df-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="b27df-175">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="b27df-175">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b27df-176">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="b27df-176">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b27df-177">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="b27df-177">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b27df-178">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="b27df-178">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b27df-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b27df-179">RELATED LINKS</span></span>

