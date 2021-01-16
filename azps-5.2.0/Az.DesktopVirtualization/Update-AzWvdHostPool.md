---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: a6c7572808184f3c83037932f45d36c7af3ff7a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341074"
---
# <span data-ttu-id="a0f12-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="a0f12-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="a0f12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0f12-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f12-103">Aktualizowanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="a0f12-103">Update a host pool.</span></span>

## <span data-ttu-id="a0f12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0f12-104">SYNTAX</span></span>

### <span data-ttu-id="a0f12-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a0f12-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a0f12-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a0f12-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0f12-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a0f12-107">DESCRIPTION</span></span>
<span data-ttu-id="a0f12-108">Aktualizowanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="a0f12-108">Update a host pool.</span></span>

## <span data-ttu-id="a0f12-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0f12-109">EXAMPLES</span></span>

### <span data-ttu-id="a0f12-110">Przykład 1: aktualizowanie HostPool pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="a0f12-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="a0f12-111">To polecenie aktualizuje HostPool pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0f12-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="a0f12-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0f12-112">PARAMETERS</span></span>

### <span data-ttu-id="a0f12-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="a0f12-113">-CustomRdpProperty</span></span>
<span data-ttu-id="a0f12-114">Niestandardowa Właściwość RDP usługi HostPool.</span><span class="sxs-lookup"><span data-stu-id="a0f12-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="a0f12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f12-115">-DefaultProfile</span></span>
<span data-ttu-id="a0f12-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f12-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0f12-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="a0f12-117">-Description</span></span>
<span data-ttu-id="a0f12-118">Opis HostPool.</span><span class="sxs-lookup"><span data-stu-id="a0f12-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="a0f12-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a0f12-119">-FriendlyName</span></span>
<span data-ttu-id="a0f12-120">Przyjazna nazwa HostPool.</span><span class="sxs-lookup"><span data-stu-id="a0f12-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="a0f12-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a0f12-121">-InputObject</span></span>
<span data-ttu-id="a0f12-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a0f12-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a0f12-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="a0f12-123">-LoadBalancerType</span></span>
<span data-ttu-id="a0f12-124">Typ modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a0f12-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="a0f12-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="a0f12-125">-MaxSessionLimit</span></span>
<span data-ttu-id="a0f12-126">Limit maksymalnej liczby sesji HostPool.</span><span class="sxs-lookup"><span data-stu-id="a0f12-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="a0f12-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0f12-127">-Name</span></span>
<span data-ttu-id="a0f12-128">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a0f12-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a0f12-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="a0f12-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="a0f12-130">Typ PersonalDesktopAssignment dla HostPool.</span><span class="sxs-lookup"><span data-stu-id="a0f12-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="a0f12-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="a0f12-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="a0f12-132">Typ preferowanego typu grupy aplikacji — domyślnie Grupa aplikacja klasyczna</span><span class="sxs-lookup"><span data-stu-id="a0f12-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="a0f12-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="a0f12-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="a0f12-134">Godzina wygaśnięcia tokenu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="a0f12-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="a0f12-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="a0f12-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="a0f12-136">Typ resetowania tokenu.</span><span class="sxs-lookup"><span data-stu-id="a0f12-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="a0f12-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f12-137">-ResourceGroupName</span></span>
<span data-ttu-id="a0f12-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0f12-138">The name of the resource group.</span></span>
<span data-ttu-id="a0f12-139">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a0f12-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a0f12-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="a0f12-140">-Ring</span></span>
<span data-ttu-id="a0f12-141">Numer dzwonka HostPool.</span><span class="sxs-lookup"><span data-stu-id="a0f12-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="a0f12-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="a0f12-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="a0f12-143">Adres URL do serwera usług ADFS dla klientów w celu podpisywania WVD certyfikatów SSO.</span><span class="sxs-lookup"><span data-stu-id="a0f12-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="a0f12-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="a0f12-144">-SsoClientId</span></span>
<span data-ttu-id="a0f12-145">ClientId dla zarejestrowanej jednostki uzależnionej używanej do wystawiania certyfikatów SSO usługi WVD.</span><span class="sxs-lookup"><span data-stu-id="a0f12-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="a0f12-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="a0f12-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="a0f12-147">Ścieżka do magazynu kluczy platformy Azure przechowującego klucz tajny służący do komunikacji z ADFS.</span><span class="sxs-lookup"><span data-stu-id="a0f12-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="a0f12-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="a0f12-148">-SsoContext</span></span>
<span data-ttu-id="a0f12-149">Ścieżka do magazynu kluczy zawierającego klucz tajny ssoContext.</span><span class="sxs-lookup"><span data-stu-id="a0f12-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="a0f12-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="a0f12-150">-SsoSecretType</span></span>
<span data-ttu-id="a0f12-151">Typ wpisu tajnego (Single Sign).</span><span class="sxs-lookup"><span data-stu-id="a0f12-151">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="a0f12-152">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a0f12-152">-SubscriptionId</span></span>
<span data-ttu-id="a0f12-153">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a0f12-153">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a0f12-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0f12-154">-Tag</span></span>
<span data-ttu-id="a0f12-155">Tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="a0f12-155">tags to be updated</span></span>

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

### <span data-ttu-id="a0f12-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="a0f12-156">-ValidationEnvironment</span></span>
<span data-ttu-id="a0f12-157">To środowisko sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="a0f12-157">Is validation environment.</span></span>

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

### <span data-ttu-id="a0f12-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="a0f12-158">-VMTemplate</span></span>
<span data-ttu-id="a0f12-159">Szablon maszyny wirtualnej na potrzeby konfiguracji sessionhosts w hostpool.</span><span class="sxs-lookup"><span data-stu-id="a0f12-159">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="a0f12-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0f12-160">-Confirm</span></span>
<span data-ttu-id="a0f12-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f12-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f12-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f12-162">-WhatIf</span></span>
<span data-ttu-id="a0f12-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f12-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0f12-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0f12-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f12-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f12-165">CommonParameters</span></span>
<span data-ttu-id="a0f12-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f12-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f12-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0f12-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f12-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0f12-168">INPUTS</span></span>

### <span data-ttu-id="a0f12-169">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a0f12-169">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a0f12-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0f12-170">OUTPUTS</span></span>

### <span data-ttu-id="a0f12-171">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="a0f12-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span></span>

## <span data-ttu-id="a0f12-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0f12-172">NOTES</span></span>

<span data-ttu-id="a0f12-173">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a0f12-173">ALIASES</span></span>

<span data-ttu-id="a0f12-174">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0f12-174">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a0f12-175">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a0f12-175">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0f12-176">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a0f12-176">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a0f12-177">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a0f12-177">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a0f12-178">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a0f12-178">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a0f12-179">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="a0f12-179">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a0f12-180">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="a0f12-180">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a0f12-181">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a0f12-181">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a0f12-182">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a0f12-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a0f12-183">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="a0f12-183">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a0f12-184">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0f12-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a0f12-185">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a0f12-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="a0f12-186">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="a0f12-186">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a0f12-187">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a0f12-187">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a0f12-188">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="a0f12-188">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a0f12-189">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="a0f12-189">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a0f12-190">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0f12-190">RELATED LINKS</span></span>

