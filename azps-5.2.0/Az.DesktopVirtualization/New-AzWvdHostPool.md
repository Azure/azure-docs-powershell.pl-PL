---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: 0eacae818861b28bfd13e0354400673b26f8e23f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340357"
---
# <span data-ttu-id="d1b42-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="d1b42-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="d1b42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d1b42-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b42-103">Tworzenie lub aktualizowanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="d1b42-103">Create or update a host pool.</span></span>

## <span data-ttu-id="d1b42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d1b42-104">SYNTAX</span></span>

### <span data-ttu-id="d1b42-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d1b42-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoadfsAuthority <String>]
 [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>] [-SsoContext <String>]
 [-SsoSecretType <SsoSecretType>] [-Tag <Hashtable>] [-ValidationEnvironment] [-VMTemplate <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1b42-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="d1b42-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1b42-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d1b42-107">DESCRIPTION</span></span>
<span data-ttu-id="d1b42-108">Tworzenie lub aktualizowanie puli hostów.</span><span class="sxs-lookup"><span data-stu-id="d1b42-108">Create or update a host pool.</span></span>

## <span data-ttu-id="d1b42-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d1b42-109">EXAMPLES</span></span>

### <span data-ttu-id="d1b42-110">Przykład 1. tworzenie pulpitu wirtualnego systemu HostPool według nazwy</span><span class="sxs-lookup"><span data-stu-id="d1b42-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="d1b42-111">To polecenie tworzy wirtualny pulpit systemu Windows HostPool w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1b42-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="d1b42-112">Przykład 1. tworzenie pulpitu wirtualnego systemu HostPool według nazwy</span><span class="sxs-lookup"><span data-stu-id="d1b42-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="d1b42-113">To polecenie tworzy wirtualny pulpit systemu Windows HostPool w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1b42-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="d1b42-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1b42-114">PARAMETERS</span></span>

### <span data-ttu-id="d1b42-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="d1b42-115">-CustomRdpProperty</span></span>
<span data-ttu-id="d1b42-116">Niestandardowa Właściwość RDP usługi HostPool.</span><span class="sxs-lookup"><span data-stu-id="d1b42-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="d1b42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b42-117">-DefaultProfile</span></span>
<span data-ttu-id="d1b42-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b42-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1b42-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="d1b42-119">-Description</span></span>
<span data-ttu-id="d1b42-120">Opis HostPool.</span><span class="sxs-lookup"><span data-stu-id="d1b42-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="d1b42-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="d1b42-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="d1b42-122">Nazwa grupy aplikacji klasycznej</span><span class="sxs-lookup"><span data-stu-id="d1b42-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="d1b42-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="d1b42-123">-ExpirationTime</span></span>
<span data-ttu-id="d1b42-124">Godzina wygaśnięcia tokenu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d1b42-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="d1b42-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d1b42-125">-FriendlyName</span></span>
<span data-ttu-id="d1b42-126">Przyjazna nazwa HostPool.</span><span class="sxs-lookup"><span data-stu-id="d1b42-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="d1b42-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="d1b42-127">-HostPoolType</span></span>
<span data-ttu-id="d1b42-128">Typ HostPool dla komputerów stacjonarnych.</span><span class="sxs-lookup"><span data-stu-id="d1b42-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="d1b42-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="d1b42-129">-LoadBalancerType</span></span>
<span data-ttu-id="d1b42-130">Typ modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="d1b42-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="d1b42-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d1b42-131">-Location</span></span>
<span data-ttu-id="d1b42-132">Lokalizacja geograficzna, w której mieszka zasób</span><span class="sxs-lookup"><span data-stu-id="d1b42-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="d1b42-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="d1b42-133">-MaxSessionLimit</span></span>
<span data-ttu-id="d1b42-134">Limit maksymalnej liczby sesji HostPool.</span><span class="sxs-lookup"><span data-stu-id="d1b42-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="d1b42-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d1b42-135">-Name</span></span>
<span data-ttu-id="d1b42-136">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="d1b42-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="d1b42-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="d1b42-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="d1b42-138">Typ PersonalDesktopAssignment dla HostPool.</span><span class="sxs-lookup"><span data-stu-id="d1b42-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="d1b42-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="d1b42-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="d1b42-140">Typ preferowanego typu grupy aplikacji — domyślnie Grupa aplikacja klasyczna</span><span class="sxs-lookup"><span data-stu-id="d1b42-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="d1b42-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="d1b42-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="d1b42-142">Zakodowany ciąg Base64 tokenu rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d1b42-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="d1b42-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="d1b42-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="d1b42-144">Typ resetowania tokenu.</span><span class="sxs-lookup"><span data-stu-id="d1b42-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="d1b42-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1b42-145">-ResourceGroupName</span></span>
<span data-ttu-id="d1b42-146">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1b42-146">The name of the resource group.</span></span>
<span data-ttu-id="d1b42-147">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="d1b42-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d1b42-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="d1b42-148">-Ring</span></span>
<span data-ttu-id="d1b42-149">Numer dzwonka HostPool.</span><span class="sxs-lookup"><span data-stu-id="d1b42-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="d1b42-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="d1b42-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="d1b42-151">Adres URL do serwera usług ADFS dla klientów w celu podpisywania WVD certyfikatów SSO.</span><span class="sxs-lookup"><span data-stu-id="d1b42-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="d1b42-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="d1b42-152">-SsoClientId</span></span>
<span data-ttu-id="d1b42-153">ClientId dla zarejestrowanej jednostki uzależnionej używanej do wystawiania certyfikatów SSO usługi WVD.</span><span class="sxs-lookup"><span data-stu-id="d1b42-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="d1b42-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="d1b42-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="d1b42-155">Ścieżka do magazynu kluczy platformy Azure przechowującego klucz tajny służący do komunikacji z ADFS.</span><span class="sxs-lookup"><span data-stu-id="d1b42-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="d1b42-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="d1b42-156">-SsoContext</span></span>
<span data-ttu-id="d1b42-157">Ścieżka do magazynu kluczy zawierającego klucz tajny ssoContext.</span><span class="sxs-lookup"><span data-stu-id="d1b42-157">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="d1b42-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="d1b42-158">-SsoSecretType</span></span>
<span data-ttu-id="d1b42-159">Typ wpisu tajnego (Single Sign).</span><span class="sxs-lookup"><span data-stu-id="d1b42-159">The type of single sign on Secret Type.</span></span>

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

### <span data-ttu-id="d1b42-160">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d1b42-160">-SubscriptionId</span></span>
<span data-ttu-id="d1b42-161">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="d1b42-161">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d1b42-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1b42-162">-Tag</span></span>
<span data-ttu-id="d1b42-163">Znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1b42-163">Resource tags.</span></span>

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

### <span data-ttu-id="d1b42-164">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="d1b42-164">-ValidationEnvironment</span></span>
<span data-ttu-id="d1b42-165">To środowisko sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="d1b42-165">Is validation environment.</span></span>

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

### <span data-ttu-id="d1b42-166">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="d1b42-166">-VMTemplate</span></span>
<span data-ttu-id="d1b42-167">Szablon maszyny wirtualnej na potrzeby konfiguracji sessionhosts w hostpool.</span><span class="sxs-lookup"><span data-stu-id="d1b42-167">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="d1b42-168">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="d1b42-168">-WorkspaceName</span></span>
<span data-ttu-id="d1b42-169">Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="d1b42-169">Workspace Name</span></span>

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

### <span data-ttu-id="d1b42-170">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1b42-170">-Confirm</span></span>
<span data-ttu-id="d1b42-171">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1b42-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1b42-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1b42-172">-WhatIf</span></span>
<span data-ttu-id="d1b42-173">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1b42-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1b42-174">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d1b42-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1b42-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b42-175">CommonParameters</span></span>
<span data-ttu-id="d1b42-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1b42-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b42-177">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1b42-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b42-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1b42-178">INPUTS</span></span>

## <span data-ttu-id="d1b42-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d1b42-179">OUTPUTS</span></span>

### <span data-ttu-id="d1b42-180">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="d1b42-180">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span></span>

## <span data-ttu-id="d1b42-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d1b42-181">NOTES</span></span>

<span data-ttu-id="d1b42-182">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d1b42-182">ALIASES</span></span>

## <span data-ttu-id="d1b42-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1b42-183">RELATED LINKS</span></span>

