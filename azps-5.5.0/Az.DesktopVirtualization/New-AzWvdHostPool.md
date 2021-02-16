---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: 6f579dfcba74f68eafaa149be15649e496c46f82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238070"
---
# <span data-ttu-id="d66ca-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="d66ca-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="d66ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d66ca-102">SYNOPSIS</span></span>
<span data-ttu-id="d66ca-103">Utwórz lub zaktualizuj pulę hosta.</span><span class="sxs-lookup"><span data-stu-id="d66ca-103">Create or update a host pool.</span></span>

## <span data-ttu-id="d66ca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d66ca-104">SYNTAX</span></span>

### <span data-ttu-id="d66ca-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="d66ca-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoadfsAuthority <String>]
 [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>] [-SsoContext <String>]
 [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d66ca-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="d66ca-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d66ca-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d66ca-107">DESCRIPTION</span></span>
<span data-ttu-id="d66ca-108">Utwórz lub zaktualizuj pulę hosta.</span><span class="sxs-lookup"><span data-stu-id="d66ca-108">Create or update a host pool.</span></span>

## <span data-ttu-id="d66ca-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d66ca-109">EXAMPLES</span></span>

### <span data-ttu-id="d66ca-110">Przykład 1. Tworzenie buforu hosta pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="d66ca-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="d66ca-111">To polecenie tworzy bufor pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d66ca-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="d66ca-112">Przykład 1. Tworzenie buforu hosta pulpitu wirtualnego systemu Windows według nazwy</span><span class="sxs-lookup"><span data-stu-id="d66ca-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="d66ca-113">To polecenie tworzy bufor pulpitu wirtualnego systemu Windows w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d66ca-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="d66ca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d66ca-114">PARAMETERS</span></span>

### <span data-ttu-id="d66ca-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="d66ca-115">-CustomRdpProperty</span></span>
<span data-ttu-id="d66ca-116">Niestandardowa właściwość rdp buforu hosta.</span><span class="sxs-lookup"><span data-stu-id="d66ca-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="d66ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d66ca-117">-DefaultProfile</span></span>
<span data-ttu-id="d66ca-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d66ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d66ca-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="d66ca-119">-Description</span></span>
<span data-ttu-id="d66ca-120">Opis buforu hosta.</span><span class="sxs-lookup"><span data-stu-id="d66ca-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="d66ca-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="d66ca-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="d66ca-122">Nazwa grupy aplikacji klasycznej</span><span class="sxs-lookup"><span data-stu-id="d66ca-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="d66ca-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="d66ca-123">-ExpirationTime</span></span>
<span data-ttu-id="d66ca-124">Czas wygaśnięcia tokenu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d66ca-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="d66ca-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d66ca-125">-FriendlyName</span></span>
<span data-ttu-id="d66ca-126">Przyjazna nazwa HostPool.</span><span class="sxs-lookup"><span data-stu-id="d66ca-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="d66ca-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="d66ca-127">-HostPoolType</span></span>
<span data-ttu-id="d66ca-128">Typ HostPool dla komputerów stacjonarnych.</span><span class="sxs-lookup"><span data-stu-id="d66ca-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="d66ca-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="d66ca-129">-LoadBalancerType</span></span>
<span data-ttu-id="d66ca-130">Typ równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="d66ca-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="d66ca-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d66ca-131">-Location</span></span>
<span data-ttu-id="d66ca-132">Lokalizacja geograficzna, w której znajduje się zasób</span><span class="sxs-lookup"><span data-stu-id="d66ca-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="d66ca-133">- MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="d66ca-133">-MaxSessionLimit</span></span>
<span data-ttu-id="d66ca-134">Limit maksymalnej liczby sesji dla buforu hosta.</span><span class="sxs-lookup"><span data-stu-id="d66ca-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="d66ca-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d66ca-135">-Name</span></span>
<span data-ttu-id="d66ca-136">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="d66ca-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="d66ca-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="d66ca-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="d66ca-138">PersonalDesktopAssignment type for HostPool.</span><span class="sxs-lookup"><span data-stu-id="d66ca-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="d66ca-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="d66ca-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="d66ca-140">Typ preferowanego typu grupy aplikacji domyślnej dla grupy aplikacji klasycznych</span><span class="sxs-lookup"><span data-stu-id="d66ca-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="d66ca-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="d66ca-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="d66ca-142">Zakodowany ciąg tokenu rejestracji (base64).</span><span class="sxs-lookup"><span data-stu-id="d66ca-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="d66ca-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="d66ca-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="d66ca-144">Typ resetowania tokenu.</span><span class="sxs-lookup"><span data-stu-id="d66ca-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="d66ca-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d66ca-145">-ResourceGroupName</span></span>
<span data-ttu-id="d66ca-146">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d66ca-146">The name of the resource group.</span></span>
<span data-ttu-id="d66ca-147">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="d66ca-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d66ca-148">— Dzwonek</span><span class="sxs-lookup"><span data-stu-id="d66ca-148">-Ring</span></span>
<span data-ttu-id="d66ca-149">Liczba pierścieniowa buforu hosta.</span><span class="sxs-lookup"><span data-stu-id="d66ca-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="d66ca-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="d66ca-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="d66ca-151">Adres URL serwera usług ADFS klienta do podpisywania certyfikatów logowania jednokrotnego WVD.</span><span class="sxs-lookup"><span data-stu-id="d66ca-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="d66ca-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="d66ca-152">-SsoClientId</span></span>
<span data-ttu-id="d66ca-153">ClientId zarejestrowanej jednostki zależnej używanej do wydawania certyfikatów logowania jednokrotnego WVD.</span><span class="sxs-lookup"><span data-stu-id="d66ca-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="d66ca-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="d66ca-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="d66ca-155">Ścieżka do usługi Azure KeyVault przechowująca klucz tajny używany do komunikacji z usługami ADFS.</span><span class="sxs-lookup"><span data-stu-id="d66ca-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="d66ca-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="d66ca-156">-SsoContext</span></span>
<span data-ttu-id="d66ca-157">Path to keyvault containing ssoContext secret.</span><span class="sxs-lookup"><span data-stu-id="d66ca-157">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="d66ca-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="d66ca-158">-SsoSecretType</span></span>
<span data-ttu-id="d66ca-159">Typ pojedynczego znaku w tajnym typie.</span><span class="sxs-lookup"><span data-stu-id="d66ca-159">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66ca-160">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="d66ca-160">-StartVMOnConnect</span></span>
<span data-ttu-id="d66ca-161">Flaga do włączanie/wyłączanie funkcji StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="d66ca-161">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="d66ca-162">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d66ca-162">-SubscriptionId</span></span>
<span data-ttu-id="d66ca-163">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="d66ca-163">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d66ca-164">— Tag</span><span class="sxs-lookup"><span data-stu-id="d66ca-164">-Tag</span></span>
<span data-ttu-id="d66ca-165">Tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="d66ca-165">Resource tags.</span></span>

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

### <span data-ttu-id="d66ca-166">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="d66ca-166">-ValidationEnvironment</span></span>
<span data-ttu-id="d66ca-167">Jest środowiskiem sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="d66ca-167">Is validation environment.</span></span>

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

### <span data-ttu-id="d66ca-168">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="d66ca-168">-VMTemplate</span></span>
<span data-ttu-id="d66ca-169">Szablon MASZYNY WIRTUALNEj dla konfiguracji hostów sesji w ramach buforu hosta.</span><span class="sxs-lookup"><span data-stu-id="d66ca-169">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="d66ca-170">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d66ca-170">-WorkspaceName</span></span>
<span data-ttu-id="d66ca-171">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="d66ca-171">Workspace Name</span></span>

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

### <span data-ttu-id="d66ca-172">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d66ca-172">-Confirm</span></span>
<span data-ttu-id="d66ca-173">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d66ca-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d66ca-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d66ca-174">-WhatIf</span></span>
<span data-ttu-id="d66ca-175">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d66ca-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d66ca-176">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d66ca-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d66ca-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66ca-177">CommonParameters</span></span>
<span data-ttu-id="d66ca-178">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d66ca-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66ca-179">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d66ca-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66ca-180">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d66ca-180">INPUTS</span></span>

## <span data-ttu-id="d66ca-181">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d66ca-181">OUTPUTS</span></span>

### <span data-ttu-id="d66ca-182">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="d66ca-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="d66ca-183">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d66ca-183">NOTES</span></span>

<span data-ttu-id="d66ca-184">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d66ca-184">ALIASES</span></span>

## <span data-ttu-id="d66ca-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d66ca-185">RELATED LINKS</span></span>

