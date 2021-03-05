---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/update-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
ms.openlocfilehash: 4504eaf26331fa4e881d6a86f284a74b7f249565
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991789"
---
# <span data-ttu-id="3a6c4-101">Update-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="3a6c4-101">Update-AzADDomainService</span></span>

## <span data-ttu-id="3a6c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6c4-103">Za pomocą operacji Aktualizuj usługę domeny można zaktualizować istniejące wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-103">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="3a6c4-104">Połączenie aktualizujące obsługuje tylko właściwości wymienione w treści poprawki.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-104">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="3a6c4-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a6c4-105">SYNTAX</span></span>

### <span data-ttu-id="3a6c4-106">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3a6c4-106">UpdateExpanded (Default)</span></span>
```
Update-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DomainConfigurationType <String>] [-DomainSecuritySettingNtlmV1 <String>]
 [-DomainSecuritySettingSyncKerberosPassword <String>] [-DomainSecuritySettingSyncNtlmPassword <String>]
 [-DomainSecuritySettingSyncOnPremPassword <String>] [-DomainSecuritySettingTlsV1 <String>]
 [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>] [-LdapSettingExternalAccess <String>]
 [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3a6c4-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3a6c4-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3a6c4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a6c4-108">DESCRIPTION</span></span>
<span data-ttu-id="3a6c4-109">Za pomocą operacji Aktualizuj usługę domeny można zaktualizować istniejące wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-109">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="3a6c4-110">Połączenie aktualizujące obsługuje tylko właściwości wymienione w treści poprawki.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-110">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="3a6c4-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a6c4-111">EXAMPLES</span></span>

### <span data-ttu-id="3a6c4-112">Przykład 1. Aktualizowanie usługi AzADDomainService według nazwy i nazwy grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3a6c4-112">Example 1: Update AzADDomainService By ResourceGroupName and Name</span></span>
```powershell
PS C:\> $ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="3a6c4-113">Aktualizowanie usługi AzADDomainService według nazwy i nazwy grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3a6c4-113">Update AzADDomainService By ResourceGroupName and Name</span></span>

### <span data-ttu-id="3a6c4-114">Przykład 2. Aktualizowanie usługi AzADDomainService przez inputobject</span><span class="sxs-lookup"><span data-stu-id="3a6c4-114">Example 2: Update AzADDomainService By Inputobject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
$ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -InputObject $getAzAddomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="3a6c4-115">Aktualizowanie usługi AzADDomainService przez Inputobject</span><span class="sxs-lookup"><span data-stu-id="3a6c4-115">Update AzADDomainService By Inputobject</span></span>

## <span data-ttu-id="3a6c4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a6c4-116">PARAMETERS</span></span>

### <span data-ttu-id="3a6c4-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3a6c4-117">-AsJob</span></span>
<span data-ttu-id="3a6c4-118">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="3a6c4-118">Run the command as a job</span></span>

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

### <span data-ttu-id="3a6c4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6c4-119">-DefaultProfile</span></span>
<span data-ttu-id="3a6c4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a6c4-121">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="3a6c4-121">-DomainConfigurationType</span></span>
<span data-ttu-id="3a6c4-122">Typ konfiguracji domeny</span><span class="sxs-lookup"><span data-stu-id="3a6c4-122">Domain Configuration Type</span></span>

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

### <span data-ttu-id="3a6c4-123">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="3a6c4-123">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="3a6c4-124">Flaga, która określa, czy funkcja NtlmV1 jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-124">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="3a6c4-125">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="3a6c4-125">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="3a6c4-126">Flaga, która określa, czy funkcja SyncKerberosPasswords jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-126">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="3a6c4-127">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="3a6c4-127">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="3a6c4-128">Flaga, która określa, czy funkcja SyncNtlmPasswords jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-128">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="3a6c4-129">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="3a6c4-129">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="3a6c4-130">Flaga, która określa, czy funkcja SyncOnPremPasswords jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-130">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="3a6c4-131">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="3a6c4-131">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="3a6c4-132">Flaga, która określa, czy funkcja TlsV1 jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-132">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="3a6c4-133">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="3a6c4-133">-FilteredSync</span></span>
<span data-ttu-id="3a6c4-134">Flaga Włączone lub Wyłączone, aby włączyć synchronizację filtrowaną według grupy</span><span class="sxs-lookup"><span data-stu-id="3a6c4-134">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="3a6c4-135">- ForestTrust</span><span class="sxs-lookup"><span data-stu-id="3a6c4-135">-ForestTrust</span></span>
<span data-ttu-id="3a6c4-136">Lista ustawień dla lasu zasobów do konstruowania, zobacz sekcję NOTATKI dla właściwości FORESTTRUST i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-136">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a6c4-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a6c4-137">-InputObject</span></span>
<span data-ttu-id="3a6c4-138">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-138">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a6c4-139">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="3a6c4-139">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="3a6c4-140">Flaga, która określa, czy jest włączony, czy wyłączony bezpieczny dostęp LDAP przez Internet.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-140">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="3a6c4-141">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="3a6c4-141">-LdapSettingLdaps</span></span>
<span data-ttu-id="3a6c4-142">Flaga, która określa, czy funkcja Bezpieczny LDAP jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-142">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="3a6c4-143">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="3a6c4-143">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="3a6c4-144">Certyfikat wymagany do skonfigurowania bezpiecznego protokołu LDAP.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-144">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="3a6c4-145">Parametr przekazany tutaj powinien być odzwierciedleniem base64encoded pliku pfx certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-145">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="3a6c4-146">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3a6c4-146">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="3a6c4-147">Hasło do odszyfrowania podanego pliku pfx bezpiecznego certyfikatu LDAP.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-147">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

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

### <span data-ttu-id="3a6c4-148">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3a6c4-148">-Name</span></span>
<span data-ttu-id="3a6c4-149">Nazwa usługi domeny.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-149">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6c4-150">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="3a6c4-150">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="3a6c4-151">Lista dodatkowych adresatów</span><span class="sxs-lookup"><span data-stu-id="3a6c4-151">The list of additional recipients</span></span>

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

### <span data-ttu-id="3a6c4-152">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="3a6c4-152">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="3a6c4-153">Czy administratorzy kontrolera domeny powinni zostać powiadomieni</span><span class="sxs-lookup"><span data-stu-id="3a6c4-153">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="3a6c4-154">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="3a6c4-154">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="3a6c4-155">Jeśli administratorzy globalni powinni zostać powiadomieni</span><span class="sxs-lookup"><span data-stu-id="3a6c4-155">Should global admins be notified</span></span>

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

### <span data-ttu-id="3a6c4-156">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3a6c4-156">-NoWait</span></span>
<span data-ttu-id="3a6c4-157">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="3a6c4-157">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3a6c4-158">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="3a6c4-158">-ReplicaSet</span></span>
<span data-ttu-id="3a6c4-159">Lista replik do skonstruowania, zobacz sekcję NOTATEK, aby uzyskać informacje o właściwościach zestawu REPLIKI I utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-159">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6c4-160">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="3a6c4-160">-ResourceForest</span></span>
<span data-ttu-id="3a6c4-161">Las zasobów</span><span class="sxs-lookup"><span data-stu-id="3a6c4-161">Resource Forest</span></span>

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

### <span data-ttu-id="3a6c4-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a6c4-162">-ResourceGroupName</span></span>
<span data-ttu-id="3a6c4-163">Nazwa grupy zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-163">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="3a6c4-164">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-164">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3a6c4-165">- SKU</span><span class="sxs-lookup"><span data-stu-id="3a6c4-165">-Sku</span></span>
<span data-ttu-id="3a6c4-166">Typ sku</span><span class="sxs-lookup"><span data-stu-id="3a6c4-166">Sku Type</span></span>

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

### <span data-ttu-id="3a6c4-167">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a6c4-167">-SubscriptionId</span></span>
<span data-ttu-id="3a6c4-168">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-168">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3a6c4-169">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-169">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3a6c4-170">— Tag</span><span class="sxs-lookup"><span data-stu-id="3a6c4-170">-Tag</span></span>
<span data-ttu-id="3a6c4-171">Tagi zasobów</span><span class="sxs-lookup"><span data-stu-id="3a6c4-171">Resource tags</span></span>

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

### <span data-ttu-id="3a6c4-172">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a6c4-172">-Confirm</span></span>
<span data-ttu-id="3a6c4-173">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a6c4-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a6c4-174">-WhatIf</span></span>
<span data-ttu-id="3a6c4-175">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a6c4-176">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a6c4-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6c4-177">CommonParameters</span></span>
<span data-ttu-id="3a6c4-178">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6c4-179">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a6c4-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6c4-180">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a6c4-180">INPUTS</span></span>

### <span data-ttu-id="3a6c4-181">Microsoft.Azure.PowerShell.Cmdlet.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="3a6c4-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="3a6c4-182">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a6c4-182">OUTPUTS</span></span>

### <span data-ttu-id="3a6c4-183">Microsoft.Azure.PowerShell.Cmdlet.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="3a6c4-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="3a6c4-184">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a6c4-184">NOTES</span></span>

<span data-ttu-id="3a6c4-185">ALIASY</span><span class="sxs-lookup"><span data-stu-id="3a6c4-185">ALIASES</span></span>

<span data-ttu-id="3a6c4-186">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a6c4-186">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3a6c4-187">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-187">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a6c4-188">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-188">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3a6c4-189">FORESTTRUST <IForestTrust[]>: Lista ustawień dla lasu zasobów</span><span class="sxs-lookup"><span data-stu-id="3a6c4-189">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="3a6c4-190">`[FriendlyName <String>]`: Przyjazna nazwa</span><span class="sxs-lookup"><span data-stu-id="3a6c4-190">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="3a6c4-191">`[RemoteDnsIP <String>]`: zdalne adresy IP DNS</span><span class="sxs-lookup"><span data-stu-id="3a6c4-191">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="3a6c4-192">`[TrustDirection <String>]`: Kierunek zaufania</span><span class="sxs-lookup"><span data-stu-id="3a6c4-192">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="3a6c4-193">`[TrustPassword <String>]`: Hasło do zaufania</span><span class="sxs-lookup"><span data-stu-id="3a6c4-193">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="3a6c4-194">`[TrustedDomainFqdn <String>]`: nazwa FQDN zaufanej domeny</span><span class="sxs-lookup"><span data-stu-id="3a6c4-194">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="3a6c4-195">INPUTOBJECT: <IAdDomainServicesIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="3a6c4-195">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a6c4-196">`[DomainServiceName <String>]`: nazwa usługi domeny.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-196">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="3a6c4-197">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3a6c4-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a6c4-198">`[ResourceGroupName <String>]`: nazwa grupy zasobów w ramach subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-198">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="3a6c4-199">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-199">The name is case insensitive.</span></span>
  - <span data-ttu-id="3a6c4-200">`[SubscriptionId <String>]`: pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-200">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="3a6c4-201">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-201">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="3a6c4-202">REPLICASET <IReplicaSet[]>: Lista replik</span><span class="sxs-lookup"><span data-stu-id="3a6c4-202">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="3a6c4-203">`[Location <String>]`: wirtualna lokalizacja sieciowa</span><span class="sxs-lookup"><span data-stu-id="3a6c4-203">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="3a6c4-204">`[SubnetId <String>]`: nazwa sieci wirtualnej, w przypadku których będą wdrażane usługi domenowe.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-204">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="3a6c4-205">Identyfikator podsieci, w których będą wdrażane usługi domenowe.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-205">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="3a6c4-206">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-206">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="3a6c4-207">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a6c4-207">RELATED LINKS</span></span>

