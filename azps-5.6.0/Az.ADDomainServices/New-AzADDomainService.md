---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/new-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
ms.openlocfilehash: 61918dd4bce5279a2528e94c4e46fbe1c8813aff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986322"
---
# <span data-ttu-id="83006-101">New-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="83006-101">New-AzADDomainService</span></span>

## <span data-ttu-id="83006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83006-102">SYNOPSIS</span></span>
<span data-ttu-id="83006-103">Operacja Utwórz usługę domeny tworzy nową usługę domeny o określonych parametrach.</span><span class="sxs-lookup"><span data-stu-id="83006-103">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="83006-104">Jeśli konkretną usługę już istnieje, wszelkie właściwości, które można poprawiać, zostaną zaktualizowane, a wszelkie właściwości, których nie można zmylić, pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="83006-104">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="83006-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="83006-105">SYNTAX</span></span>

```
New-AzADDomainService -Name <String> -ResourceGroupName <String> -DomainName <String>
 -ReplicaSet <IReplicaSet[]> [-SubscriptionId <String>] [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83006-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="83006-106">DESCRIPTION</span></span>
<span data-ttu-id="83006-107">Operacja Utwórz usługę domeny tworzy nową usługę domeny o określonych parametrach.</span><span class="sxs-lookup"><span data-stu-id="83006-107">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="83006-108">Jeśli konkretną usługę już istnieje, wszelkie właściwości, które można poprawiać, zostaną zaktualizowane, a wszelkie właściwości, których nie można zmylić, pozostaną niezmienione.</span><span class="sxs-lookup"><span data-stu-id="83006-108">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="83006-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="83006-109">EXAMPLES</span></span>

### <span data-ttu-id="83006-110">Przykład 1. Tworzenie nowej usługi ADDomainService</span><span class="sxs-lookup"><span data-stu-id="83006-110">Example 1: Create new ADDomainService</span></span>
```powershell
PS C:\> $replicaSet = New-AzADDomainServiceReplicaSetObject -Location westus -SubnetId /subscriptions/********-****-****-****-**********/resourceGroups/yishitest/providers/Microsoft.Network/virtualNetworks/aadds-vnet/subnets/default
New-AzADDomainService -name youriADdomain -ResourceGroupName youriAddomain -DomainName youriAddomain.com -ReplicaSet $replicaSet -debug

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="83006-111">Tworzenie nowej usługi ADDomainService</span><span class="sxs-lookup"><span data-stu-id="83006-111">Create new ADDomainService</span></span>

## <span data-ttu-id="83006-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83006-112">PARAMETERS</span></span>

### <span data-ttu-id="83006-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="83006-113">-AsJob</span></span>
<span data-ttu-id="83006-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="83006-114">Run the command as a job</span></span>

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

### <span data-ttu-id="83006-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83006-115">-DefaultProfile</span></span>
<span data-ttu-id="83006-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="83006-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83006-117">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="83006-117">-DomainConfigurationType</span></span>
<span data-ttu-id="83006-118">Typ konfiguracji domeny</span><span class="sxs-lookup"><span data-stu-id="83006-118">Domain Configuration Type</span></span>

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

### <span data-ttu-id="83006-119">-DomainName</span><span class="sxs-lookup"><span data-stu-id="83006-119">-DomainName</span></span>
<span data-ttu-id="83006-120">Nazwa domeny platformy Azure, w ramach których użytkownik chce wdrożyć usługi domenowe.</span><span class="sxs-lookup"><span data-stu-id="83006-120">The name of the Azure domain that the user would like to deploy Domain Services to.</span></span>

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

### <span data-ttu-id="83006-121">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="83006-121">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="83006-122">Flaga, która określa, czy funkcja NtlmV1 jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="83006-122">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="83006-123">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="83006-123">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="83006-124">Flaga, która określa, czy funkcja SyncKerberosPasswords jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="83006-124">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="83006-125">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="83006-125">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="83006-126">Flaga, która określa, czy funkcja SyncNtlmPasswords jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="83006-126">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="83006-127">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="83006-127">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="83006-128">Flaga, która określa, czy funkcja SyncOnPremPasswords jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="83006-128">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="83006-129">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="83006-129">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="83006-130">Flaga, która określa, czy funkcja TlsV1 jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="83006-130">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="83006-131">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="83006-131">-FilteredSync</span></span>
<span data-ttu-id="83006-132">Flaga Włączone lub Wyłączone, aby włączyć synchronizację filtrowaną według grupy</span><span class="sxs-lookup"><span data-stu-id="83006-132">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="83006-133">- ForestTrust</span><span class="sxs-lookup"><span data-stu-id="83006-133">-ForestTrust</span></span>
<span data-ttu-id="83006-134">Lista ustawień dla lasu zasobów do konstruowania, zobacz sekcję NOTATKI dla właściwości FORESTTRUST i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="83006-134">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IForestTrust[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83006-135">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="83006-135">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="83006-136">Flaga, która określa, czy jest włączony, czy wyłączony bezpieczny dostęp LDAP przez Internet.</span><span class="sxs-lookup"><span data-stu-id="83006-136">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="83006-137">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="83006-137">-LdapSettingLdaps</span></span>
<span data-ttu-id="83006-138">Flaga, która określa, czy funkcja Bezpieczny LDAP jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="83006-138">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="83006-139">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="83006-139">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="83006-140">Certyfikat wymagany do skonfigurowania bezpiecznego protokołu LDAP.</span><span class="sxs-lookup"><span data-stu-id="83006-140">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="83006-141">Parametr przekazany tutaj powinien być odzwierciedleniem base64encoded pliku pfx certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="83006-141">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="83006-142">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="83006-142">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="83006-143">Hasło do odszyfrowania podanego pliku pfx bezpiecznego certyfikatu LDAP.</span><span class="sxs-lookup"><span data-stu-id="83006-143">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83006-144">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="83006-144">-Name</span></span>
<span data-ttu-id="83006-145">Nazwa usługi domeny.</span><span class="sxs-lookup"><span data-stu-id="83006-145">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83006-146">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="83006-146">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="83006-147">Lista dodatkowych adresatów</span><span class="sxs-lookup"><span data-stu-id="83006-147">The list of additional recipients</span></span>

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

### <span data-ttu-id="83006-148">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="83006-148">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="83006-149">Czy administratorzy kontrolera domeny powinni zostać powiadomieni</span><span class="sxs-lookup"><span data-stu-id="83006-149">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="83006-150">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="83006-150">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="83006-151">Jeśli administratorzy globalni powinni zostać powiadomieni</span><span class="sxs-lookup"><span data-stu-id="83006-151">Should global admins be notified</span></span>

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

### <span data-ttu-id="83006-152">-NoWait</span><span class="sxs-lookup"><span data-stu-id="83006-152">-NoWait</span></span>
<span data-ttu-id="83006-153">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="83006-153">Run the command asynchronously</span></span>

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

### <span data-ttu-id="83006-154">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="83006-154">-ReplicaSet</span></span>
<span data-ttu-id="83006-155">Lista replik do skonstruowania, zobacz sekcję NOTATEK, aby uzyskać informacje o właściwościach zestawu REPLIKI I utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="83006-155">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83006-156">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="83006-156">-ResourceForest</span></span>
<span data-ttu-id="83006-157">Las zasobów</span><span class="sxs-lookup"><span data-stu-id="83006-157">Resource Forest</span></span>

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

### <span data-ttu-id="83006-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83006-158">-ResourceGroupName</span></span>
<span data-ttu-id="83006-159">Nazwa grupy zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="83006-159">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="83006-160">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="83006-160">The name is case insensitive.</span></span>

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

### <span data-ttu-id="83006-161">- SKU</span><span class="sxs-lookup"><span data-stu-id="83006-161">-Sku</span></span>
<span data-ttu-id="83006-162">Typ sku</span><span class="sxs-lookup"><span data-stu-id="83006-162">Sku Type</span></span>

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

### <span data-ttu-id="83006-163">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83006-163">-SubscriptionId</span></span>
<span data-ttu-id="83006-164">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83006-164">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="83006-165">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="83006-165">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="83006-166">— Tag</span><span class="sxs-lookup"><span data-stu-id="83006-166">-Tag</span></span>
<span data-ttu-id="83006-167">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="83006-167">Resource tags</span></span>

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

### <span data-ttu-id="83006-168">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83006-168">-Confirm</span></span>
<span data-ttu-id="83006-169">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="83006-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83006-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83006-170">-WhatIf</span></span>
<span data-ttu-id="83006-171">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83006-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83006-172">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="83006-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83006-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83006-173">CommonParameters</span></span>
<span data-ttu-id="83006-174">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83006-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83006-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83006-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83006-176">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83006-176">INPUTS</span></span>

## <span data-ttu-id="83006-177">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83006-177">OUTPUTS</span></span>

### <span data-ttu-id="83006-178">Microsoft.Azure.PowerShell.Cmdlet.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="83006-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="83006-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="83006-179">NOTES</span></span>

<span data-ttu-id="83006-180">ALIASY</span><span class="sxs-lookup"><span data-stu-id="83006-180">ALIASES</span></span>

<span data-ttu-id="83006-181">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83006-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83006-182">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="83006-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83006-183">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83006-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83006-184">FORESTTRUST <IForestTrust[]>: Lista ustawień dla lasu zasobów</span><span class="sxs-lookup"><span data-stu-id="83006-184">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="83006-185">`[FriendlyName <String>]`: Przyjazna nazwa</span><span class="sxs-lookup"><span data-stu-id="83006-185">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="83006-186">`[RemoteDnsIP <String>]`: zdalne adresy IP DNS</span><span class="sxs-lookup"><span data-stu-id="83006-186">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="83006-187">`[TrustDirection <String>]`: Kierunek zaufania</span><span class="sxs-lookup"><span data-stu-id="83006-187">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="83006-188">`[TrustPassword <String>]`: Hasło do zaufania</span><span class="sxs-lookup"><span data-stu-id="83006-188">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="83006-189">`[TrustedDomainFqdn <String>]`: nazwa FQDN zaufanej domeny</span><span class="sxs-lookup"><span data-stu-id="83006-189">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="83006-190">REPLICASET <IReplicaSet[]>: Lista replik</span><span class="sxs-lookup"><span data-stu-id="83006-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="83006-191">`[Location <String>]`: wirtualna lokalizacja sieciowa</span><span class="sxs-lookup"><span data-stu-id="83006-191">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="83006-192">`[SubnetId <String>]`: nazwa sieci wirtualnej, w przypadku których będą wdrażane usługi domenowe.</span><span class="sxs-lookup"><span data-stu-id="83006-192">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="83006-193">Identyfikator podsieci, w których będą wdrażane usługi domenowe.</span><span class="sxs-lookup"><span data-stu-id="83006-193">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="83006-194">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="83006-194">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="83006-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83006-195">RELATED LINKS</span></span>

