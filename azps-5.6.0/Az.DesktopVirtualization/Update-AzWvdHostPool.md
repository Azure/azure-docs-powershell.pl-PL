---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: 5b69ff6bb04f1e8b1ae5e13fbab2c6a5f7c67927
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983585"
---
# <span data-ttu-id="91449-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="91449-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="91449-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91449-102">SYNOPSIS</span></span>
<span data-ttu-id="91449-103">Zaktualizuj pulę hosta.</span><span class="sxs-lookup"><span data-stu-id="91449-103">Update a host pool.</span></span>

## <span data-ttu-id="91449-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="91449-104">SYNTAX</span></span>

### <span data-ttu-id="91449-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="91449-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="91449-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="91449-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="91449-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="91449-107">DESCRIPTION</span></span>
<span data-ttu-id="91449-108">Zaktualizuj pulę hosta.</span><span class="sxs-lookup"><span data-stu-id="91449-108">Update a host pool.</span></span>

## <span data-ttu-id="91449-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="91449-109">EXAMPLES</span></span>

### <span data-ttu-id="91449-110">Przykład 1. Aktualizowanie buforu hosta pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="91449-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="91449-111">To polecenie aktualizuje bufor hosta pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="91449-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="91449-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91449-112">PARAMETERS</span></span>

### <span data-ttu-id="91449-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="91449-113">-CustomRdpProperty</span></span>
<span data-ttu-id="91449-114">Niestandardowa właściwość rdp buforu hosta.</span><span class="sxs-lookup"><span data-stu-id="91449-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="91449-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91449-115">-DefaultProfile</span></span>
<span data-ttu-id="91449-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="91449-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91449-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="91449-117">-Description</span></span>
<span data-ttu-id="91449-118">Opis buforu hosta.</span><span class="sxs-lookup"><span data-stu-id="91449-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="91449-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="91449-119">-FriendlyName</span></span>
<span data-ttu-id="91449-120">Przyjazna nazwa HostPool.</span><span class="sxs-lookup"><span data-stu-id="91449-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="91449-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91449-121">-InputObject</span></span>
<span data-ttu-id="91449-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="91449-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="91449-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="91449-123">-LoadBalancerType</span></span>
<span data-ttu-id="91449-124">Typ równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="91449-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="91449-125">- MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="91449-125">-MaxSessionLimit</span></span>
<span data-ttu-id="91449-126">Limit maksymalnej liczby sesji dla buforu hosta.</span><span class="sxs-lookup"><span data-stu-id="91449-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="91449-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="91449-127">-Name</span></span>
<span data-ttu-id="91449-128">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="91449-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="91449-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="91449-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="91449-130">PersonalDesktopAssignment type for HostPool.</span><span class="sxs-lookup"><span data-stu-id="91449-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="91449-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="91449-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="91449-132">Typ preferowanego typu grupy aplikacji domyślnej dla grupy aplikacji klasycznych</span><span class="sxs-lookup"><span data-stu-id="91449-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="91449-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="91449-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="91449-134">Czas wygaśnięcia tokenu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="91449-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="91449-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="91449-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="91449-136">Typ resetowania tokenu.</span><span class="sxs-lookup"><span data-stu-id="91449-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="91449-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91449-137">-ResourceGroupName</span></span>
<span data-ttu-id="91449-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91449-138">The name of the resource group.</span></span>
<span data-ttu-id="91449-139">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="91449-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="91449-140">— Dzwonek</span><span class="sxs-lookup"><span data-stu-id="91449-140">-Ring</span></span>
<span data-ttu-id="91449-141">Liczba pierścieniowa buforu hosta.</span><span class="sxs-lookup"><span data-stu-id="91449-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="91449-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="91449-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="91449-143">Adres URL serwera usług ADFS klienta do podpisywania certyfikatów logowania jednokrotnego WVD.</span><span class="sxs-lookup"><span data-stu-id="91449-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="91449-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="91449-144">-SsoClientId</span></span>
<span data-ttu-id="91449-145">ClientId zarejestrowanej jednostki zależnej używanej do wydawania certyfikatów logowania jednokrotnego WVD.</span><span class="sxs-lookup"><span data-stu-id="91449-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="91449-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="91449-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="91449-147">Ścieżka do usługi Azure KeyVault przechowująca klucz tajny używany do komunikacji z usługami ADFS.</span><span class="sxs-lookup"><span data-stu-id="91449-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="91449-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="91449-148">-SsoContext</span></span>
<span data-ttu-id="91449-149">Path to keyvault containing ssoContext secret.</span><span class="sxs-lookup"><span data-stu-id="91449-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="91449-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="91449-150">-SsoSecretType</span></span>
<span data-ttu-id="91449-151">Typ pojedynczego znaku w tajnym typie.</span><span class="sxs-lookup"><span data-stu-id="91449-151">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91449-152">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="91449-152">-StartVMOnConnect</span></span>
<span data-ttu-id="91449-153">Flaga do włączanie/wyłączanie funkcji StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="91449-153">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="91449-154">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91449-154">-SubscriptionId</span></span>
<span data-ttu-id="91449-155">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="91449-155">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="91449-156">— Tag</span><span class="sxs-lookup"><span data-stu-id="91449-156">-Tag</span></span>
<span data-ttu-id="91449-157">tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="91449-157">tags to be updated</span></span>

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

### <span data-ttu-id="91449-158">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="91449-158">-ValidationEnvironment</span></span>
<span data-ttu-id="91449-159">Jest środowiskiem sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="91449-159">Is validation environment.</span></span>

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

### <span data-ttu-id="91449-160">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="91449-160">-VMTemplate</span></span>
<span data-ttu-id="91449-161">Szablon MASZYNY WIRTUALNEj dla konfiguracji hostów sesji w ramach buforu hosta.</span><span class="sxs-lookup"><span data-stu-id="91449-161">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="91449-162">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91449-162">-Confirm</span></span>
<span data-ttu-id="91449-163">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="91449-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91449-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91449-164">-WhatIf</span></span>
<span data-ttu-id="91449-165">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91449-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91449-166">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="91449-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91449-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91449-167">CommonParameters</span></span>
<span data-ttu-id="91449-168">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91449-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91449-169">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91449-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91449-170">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91449-170">INPUTS</span></span>

### <span data-ttu-id="91449-171">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="91449-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="91449-172">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91449-172">OUTPUTS</span></span>

### <span data-ttu-id="91449-173">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="91449-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="91449-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="91449-174">NOTES</span></span>

<span data-ttu-id="91449-175">ALIASY</span><span class="sxs-lookup"><span data-stu-id="91449-175">ALIASES</span></span>

<span data-ttu-id="91449-176">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91449-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91449-177">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="91449-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91449-178">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="91449-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91449-179">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="91449-179">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="91449-180">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="91449-180">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="91449-181">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="91449-181">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="91449-182">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="91449-182">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="91449-183">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91449-183">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="91449-184">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="91449-184">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="91449-185">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="91449-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="91449-186">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91449-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="91449-187">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="91449-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="91449-188">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="91449-188">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="91449-189">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="91449-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="91449-190">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="91449-190">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="91449-191">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="91449-191">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="91449-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91449-192">RELATED LINKS</span></span>

