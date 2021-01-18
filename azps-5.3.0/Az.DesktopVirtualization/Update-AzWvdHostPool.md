---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: e6b77d9d779931d9b50de2b504b357ecd22a2b92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501095"
---
# <span data-ttu-id="34575-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="34575-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="34575-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34575-102">SYNOPSIS</span></span>
<span data-ttu-id="34575-103">Aktualizowanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="34575-103">Update a host pool.</span></span>

## <span data-ttu-id="34575-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34575-104">SYNTAX</span></span>

### <span data-ttu-id="34575-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="34575-105">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="34575-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="34575-106">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="34575-107">Opis</span><span class="sxs-lookup"><span data-stu-id="34575-107">DESCRIPTION</span></span>
<span data-ttu-id="34575-108">Aktualizowanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="34575-108">Update a host pool.</span></span>

## <span data-ttu-id="34575-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34575-109">EXAMPLES</span></span>

### <span data-ttu-id="34575-110">Przykład 1: aktualizowanie HostPool pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="34575-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="34575-111">To polecenie aktualizuje HostPool pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="34575-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="34575-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34575-112">PARAMETERS</span></span>

### <span data-ttu-id="34575-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="34575-113">-CustomRdpProperty</span></span>
<span data-ttu-id="34575-114">Niestandardowa Właściwość RDP usługi HostPool.</span><span class="sxs-lookup"><span data-stu-id="34575-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="34575-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34575-115">-DefaultProfile</span></span>
<span data-ttu-id="34575-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34575-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34575-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="34575-117">-Description</span></span>
<span data-ttu-id="34575-118">Opis HostPool.</span><span class="sxs-lookup"><span data-stu-id="34575-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="34575-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="34575-119">-FriendlyName</span></span>
<span data-ttu-id="34575-120">Przyjazna nazwa HostPool.</span><span class="sxs-lookup"><span data-stu-id="34575-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="34575-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="34575-121">-InputObject</span></span>
<span data-ttu-id="34575-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="34575-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="34575-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="34575-123">-LoadBalancerType</span></span>
<span data-ttu-id="34575-124">Typ modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="34575-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="34575-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="34575-125">-MaxSessionLimit</span></span>
<span data-ttu-id="34575-126">Limit maksymalnej liczby sesji HostPool.</span><span class="sxs-lookup"><span data-stu-id="34575-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="34575-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34575-127">-Name</span></span>
<span data-ttu-id="34575-128">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="34575-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="34575-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="34575-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="34575-130">Typ PersonalDesktopAssignment dla HostPool.</span><span class="sxs-lookup"><span data-stu-id="34575-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="34575-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="34575-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="34575-132">Typ preferowanego typu grupy aplikacji — domyślnie Grupa aplikacja klasyczna</span><span class="sxs-lookup"><span data-stu-id="34575-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="34575-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="34575-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="34575-134">Godzina wygaśnięcia tokenu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="34575-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="34575-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="34575-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="34575-136">Typ resetowania tokenu.</span><span class="sxs-lookup"><span data-stu-id="34575-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="34575-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34575-137">-ResourceGroupName</span></span>
<span data-ttu-id="34575-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34575-138">The name of the resource group.</span></span>
<span data-ttu-id="34575-139">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="34575-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="34575-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="34575-140">-Ring</span></span>
<span data-ttu-id="34575-141">Numer dzwonka HostPool.</span><span class="sxs-lookup"><span data-stu-id="34575-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="34575-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="34575-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="34575-143">Adres URL do serwera usług ADFS dla klientów w celu podpisywania WVD certyfikatów SSO.</span><span class="sxs-lookup"><span data-stu-id="34575-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="34575-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="34575-144">-SsoClientId</span></span>
<span data-ttu-id="34575-145">ClientId dla zarejestrowanej jednostki uzależnionej używanej do wystawiania certyfikatów SSO usługi WVD.</span><span class="sxs-lookup"><span data-stu-id="34575-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="34575-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="34575-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="34575-147">Ścieżka do magazynu kluczy platformy Azure przechowującego klucz tajny służący do komunikacji z ADFS.</span><span class="sxs-lookup"><span data-stu-id="34575-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="34575-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="34575-148">-SsoContext</span></span>
<span data-ttu-id="34575-149">Ścieżka do magazynu kluczy zawierającego klucz tajny ssoContext.</span><span class="sxs-lookup"><span data-stu-id="34575-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="34575-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="34575-150">-SsoSecretType</span></span>
<span data-ttu-id="34575-151">Typ wpisu tajnego (Single Sign).</span><span class="sxs-lookup"><span data-stu-id="34575-151">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="34575-152">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="34575-152">-StartVMOnConnect</span></span>
<span data-ttu-id="34575-153">Flaga włączenia/wyłączenia funkcji StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="34575-153">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="34575-154">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="34575-154">-SubscriptionId</span></span>
<span data-ttu-id="34575-155">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="34575-155">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="34575-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="34575-156">-Tag</span></span>
<span data-ttu-id="34575-157">Tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="34575-157">tags to be updated</span></span>

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

### <span data-ttu-id="34575-158">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="34575-158">-ValidationEnvironment</span></span>
<span data-ttu-id="34575-159">To środowisko sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="34575-159">Is validation environment.</span></span>

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

### <span data-ttu-id="34575-160">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="34575-160">-VMTemplate</span></span>
<span data-ttu-id="34575-161">Szablon maszyny wirtualnej na potrzeby konfiguracji sessionhosts w hostpool.</span><span class="sxs-lookup"><span data-stu-id="34575-161">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="34575-162">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34575-162">-Confirm</span></span>
<span data-ttu-id="34575-163">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34575-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34575-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34575-164">-WhatIf</span></span>
<span data-ttu-id="34575-165">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34575-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34575-166">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34575-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34575-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34575-167">CommonParameters</span></span>
<span data-ttu-id="34575-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34575-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34575-169">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34575-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34575-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34575-170">INPUTS</span></span>

### <span data-ttu-id="34575-171">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="34575-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="34575-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34575-172">OUTPUTS</span></span>

### <span data-ttu-id="34575-173">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201102Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="34575-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="34575-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34575-174">NOTES</span></span>

<span data-ttu-id="34575-175">PISUJE</span><span class="sxs-lookup"><span data-stu-id="34575-175">ALIASES</span></span>

<span data-ttu-id="34575-176">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34575-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34575-177">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="34575-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34575-178">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34575-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34575-179">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="34575-179">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34575-180">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="34575-180">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="34575-181">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="34575-181">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="34575-182">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="34575-182">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="34575-183">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="34575-183">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="34575-184">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="34575-184">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34575-185">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="34575-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="34575-186">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34575-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="34575-187">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="34575-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="34575-188">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="34575-188">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="34575-189">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="34575-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="34575-190">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="34575-190">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="34575-191">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="34575-191">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="34575-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34575-192">RELATED LINKS</span></span>

