---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 0e3a9b99a23715b63eb42c83ba112776272969ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179699"
---
# <span data-ttu-id="d22f3-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d22f3-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="d22f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d22f3-102">SYNOPSIS</span></span>
<span data-ttu-id="d22f3-103">Tworzy nowe zasady zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d22f3-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="d22f3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d22f3-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-IntrusionDetection <PSAzureFirewallPolicyIntrusionDetection>] [-TransportSecurityName <String>]
 [-TransportSecurityKeyVaultSecretId <String>] [-SkuTier <String>] [-UserAssignedIdentityId <String>]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d22f3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d22f3-105">DESCRIPTION</span></span>
<span data-ttu-id="d22f3-106">Polecenie **cmdlet New-AzFirewallPolicy** tworzy zasady zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d22f3-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="d22f3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d22f3-107">EXAMPLES</span></span>

### <span data-ttu-id="d22f3-108">Przykład 1: 1.</span><span class="sxs-lookup"><span data-stu-id="d22f3-108">Example 1: 1.</span></span> <span data-ttu-id="d22f3-109">Tworzenie pustych zasad</span><span class="sxs-lookup"><span data-stu-id="d22f3-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="d22f3-110">W tym przykładzie są tworzyne zasady zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d22f3-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="d22f3-111">Przykład 2: 2.</span><span class="sxs-lookup"><span data-stu-id="d22f3-111">Example 2: 2.</span></span> <span data-ttu-id="d22f3-112">Tworzenie pustych zasad za pomocą trybu ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="d22f3-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="d22f3-113">W tym przykładzie są tworzyne zasady zapory platformy Azure z trybem intela z zagrożeniami</span><span class="sxs-lookup"><span data-stu-id="d22f3-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="d22f3-114">Przykład 3: 3.</span><span class="sxs-lookup"><span data-stu-id="d22f3-114">Example 3: 3.</span></span> <span data-ttu-id="d22f3-115">Tworzenie pustych zasad za pomocą aplikacji ThreatIntel Whitelist</span><span class="sxs-lookup"><span data-stu-id="d22f3-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="d22f3-116">W tym przykładzie są tworzyne zasady zapory platformy Azure z zagrożeniami, które mogą stanowić białą listę firmy Intel</span><span class="sxs-lookup"><span data-stu-id="d22f3-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

### <span data-ttu-id="d22f3-117">Przykład 4. 4.</span><span class="sxs-lookup"><span data-stu-id="d22f3-117">Example 4: 4.</span></span> <span data-ttu-id="d22f3-118">Tworzenie zasad z wykrywaniem intruzów, tożsamości i zabezpieczeń transportu</span><span class="sxs-lookup"><span data-stu-id="d22f3-118">Create policy with intrusion detection, identity and transport security</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride -BypassTraffic $bypass
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/TestRg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/user-assign-identity'
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection -TransportSecurityName tsName -TransportSecurityKeyVaultSecretId "https://<keyvaultname>.vault.azure.net/secrets/cacert"  -UserAssignedIdentityId $userAssignedIdentity
```

<span data-ttu-id="d22f3-119">W tym przykładzie są owane zasady zapory platformy Azure z wykrywaniem intruzów w trybie alertu, przypisaną tożsamością użytkownika i zabezpieczeniami transportu</span><span class="sxs-lookup"><span data-stu-id="d22f3-119">This example creates an azure firewall policy with a intrusion detection in mode alert, user assigned identity and transport security</span></span>

## <span data-ttu-id="d22f3-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d22f3-120">PARAMETERS</span></span>

### <span data-ttu-id="d22f3-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d22f3-121">-AsJob</span></span>
<span data-ttu-id="d22f3-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d22f3-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-123">— BasePolicy</span><span class="sxs-lookup"><span data-stu-id="d22f3-123">-BasePolicy</span></span>
<span data-ttu-id="d22f3-124">Zasady podstawowe, po których mają być dziedziczone</span><span class="sxs-lookup"><span data-stu-id="d22f3-124">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22f3-125">-DefaultProfile</span></span>
<span data-ttu-id="d22f3-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d22f3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-127">- DnsSetting</span><span class="sxs-lookup"><span data-stu-id="d22f3-127">-DnsSetting</span></span>
<span data-ttu-id="d22f3-128">Ustawienie DNS</span><span class="sxs-lookup"><span data-stu-id="d22f3-128">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-129">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d22f3-129">-Force</span></span>
<span data-ttu-id="d22f3-130">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="d22f3-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-131">— Tożsamość</span><span class="sxs-lookup"><span data-stu-id="d22f3-131">-Identity</span></span>
<span data-ttu-id="d22f3-132">Tożsamość zasad zapory, która ma zostać przypisana do zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="d22f3-132">Firewall Policy Identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-133">-IntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="d22f3-133">-IntrusionDetection</span></span>
<span data-ttu-id="d22f3-134">Ustawienie wykrywania intruzów</span><span class="sxs-lookup"><span data-stu-id="d22f3-134">The Intrusion Detection Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d22f3-135">-Location</span></span>
<span data-ttu-id="d22f3-136">.</span><span class="sxs-lookup"><span data-stu-id="d22f3-136">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d22f3-137">-Name</span></span>
<span data-ttu-id="d22f3-138">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d22f3-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d22f3-139">-ResourceGroupName</span></span>
<span data-ttu-id="d22f3-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d22f3-140">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-141">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d22f3-141">-SkuTier</span></span>
<span data-ttu-id="d22f3-142">Warstwa SKU zasad zapory</span><span class="sxs-lookup"><span data-stu-id="d22f3-142">Firewall policy sku tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-143">— Tag</span><span class="sxs-lookup"><span data-stu-id="d22f3-143">-Tag</span></span>
<span data-ttu-id="d22f3-144">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="d22f3-144">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-145">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="d22f3-145">-ThreatIntelMode</span></span>
<span data-ttu-id="d22f3-146">Tryb działania analizy zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="d22f3-146">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-147">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="d22f3-147">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="d22f3-148">Lista na liście na temat analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="d22f3-148">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-149">-TransportSecurityKeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="d22f3-149">-TransportSecurityKeyVaultSecretId</span></span>
<span data-ttu-id="d22f3-150">Secret Id of (base-64 encoded unencrypted pfx) 'Secret' or 'Certificate' object stored in KeyVault</span><span class="sxs-lookup"><span data-stu-id="d22f3-150">Secret Id of (base-64 encoded unencrypted pfx) 'Secret' or 'Certificate' object stored in KeyVault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-151">-TransportSecurityName</span><span class="sxs-lookup"><span data-stu-id="d22f3-151">-TransportSecurityName</span></span>
<span data-ttu-id="d22f3-152">Nazwa zabezpieczeń transportu</span><span class="sxs-lookup"><span data-stu-id="d22f3-152">Transport security name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-153">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="d22f3-153">-UserAssignedIdentityId</span></span>
<span data-ttu-id="d22f3-154">Identyfikator Zasobu użytkownika przypisanego do zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="d22f3-154">ResourceId of the user assigned identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-155">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d22f3-155">-Confirm</span></span>
<span data-ttu-id="d22f3-156">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d22f3-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d22f3-157">-WhatIf</span></span>
<span data-ttu-id="d22f3-158">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d22f3-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d22f3-159">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d22f3-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22f3-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22f3-160">CommonParameters</span></span>
<span data-ttu-id="d22f3-161">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22f3-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22f3-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d22f3-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22f3-163">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d22f3-163">INPUTS</span></span>

### <span data-ttu-id="d22f3-164">System.String</span><span class="sxs-lookup"><span data-stu-id="d22f3-164">System.String</span></span>

### <span data-ttu-id="d22f3-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d22f3-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d22f3-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d22f3-166">OUTPUTS</span></span>

### <span data-ttu-id="d22f3-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="d22f3-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="d22f3-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d22f3-168">NOTES</span></span>

## <span data-ttu-id="d22f3-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d22f3-169">RELATED LINKS</span></span>
