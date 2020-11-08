---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 8897b2e1175c82f3dcc25642dec920a4b6d7343c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224905"
---
# <span data-ttu-id="cc63f-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc63f-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="cc63f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc63f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc63f-103">Aktualizuje istniejące VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cc63f-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="cc63f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc63f-104">SYNTAX</span></span>

### <span data-ttu-id="cc63f-105">ByVpnServerConfigurationNameByCertificateAuthentication (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cc63f-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc63f-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="cc63f-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc63f-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="cc63f-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc63f-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="cc63f-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc63f-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="cc63f-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc63f-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="cc63f-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc63f-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="cc63f-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc63f-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="cc63f-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc63f-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="cc63f-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc63f-114">Opis</span><span class="sxs-lookup"><span data-stu-id="cc63f-114">DESCRIPTION</span></span>
<span data-ttu-id="cc63f-115">Polecenie cmdlet **Update-AzVpnServerConfiguration** umożliwia zaktualizowanie istniejącego VpnServerConfiguration za pomocą różnych VpnProtocols, VpnAuthenticationTypes, IpsecPolicies i ustawienie wybranych parametrów związanych z typem uwierzytelniania sieci VPN zgodnie z wymaganiami klienta dotyczącymi łączności witryny.</span><span class="sxs-lookup"><span data-stu-id="cc63f-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="cc63f-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc63f-116">EXAMPLES</span></span>

### <span data-ttu-id="cc63f-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc63f-117">Example 1</span></span>
```powershell
PS C:\> Update-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2

PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="cc63f-118">Powyższe polecenie zaktualizuje istniejące VpnServerConfiguration za pomocą VpnProtocol jako IkeV2.</span><span class="sxs-lookup"><span data-stu-id="cc63f-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="cc63f-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc63f-119">PARAMETERS</span></span>

### <span data-ttu-id="cc63f-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="cc63f-120">-AadAudience</span></span>
<span data-ttu-id="cc63f-121">Grupa odbiorców AAD dla uwierzytelniania w usłudze AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="cc63f-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="cc63f-122">-AadIssuer</span></span>
<span data-ttu-id="cc63f-123">Wystawca AAD dla uwierzytelniania w usłudze P2S w usłudze AAD.</span><span class="sxs-lookup"><span data-stu-id="cc63f-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="cc63f-124">-AadTenant</span></span>
<span data-ttu-id="cc63f-125">Dzierżawa AAD na potrzeby uwierzytelniania w usłudze P2S w usłudze AAD.</span><span class="sxs-lookup"><span data-stu-id="cc63f-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc63f-126">-AsJob</span></span>
<span data-ttu-id="cc63f-127">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cc63f-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc63f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc63f-128">-DefaultProfile</span></span>
<span data-ttu-id="cc63f-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc63f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc63f-130">-InputObject</span></span>
<span data-ttu-id="cc63f-131">Obiekt konfiguracji serwera sieci VPN do zmodyfikowania</span><span class="sxs-lookup"><span data-stu-id="cc63f-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc63f-132">-Name</span></span>
<span data-ttu-id="cc63f-133">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cc63f-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="cc63f-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="cc63f-135">Lista ścieżek plików RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cc63f-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="cc63f-136">-RadiusServerAddress</span></span>
<span data-ttu-id="cc63f-137">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="cc63f-137">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-138">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="cc63f-138">-RadiusServerList</span></span>
<span data-ttu-id="cc63f-139">P2S zewnętrzne serwery RADIUS.</span><span class="sxs-lookup"><span data-stu-id="cc63f-139">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-140">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="cc63f-140">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="cc63f-141">Lista ścieżek plików RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cc63f-141">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="cc63f-142">-RadiusServerSecret</span></span>
<span data-ttu-id="cc63f-143">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="cc63f-143">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc63f-144">-ResourceGroupName</span></span>
<span data-ttu-id="cc63f-145">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc63f-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc63f-146">-ResourceId</span></span>
<span data-ttu-id="cc63f-147">Identyfikator zasobu platformy Azure dla konfiguracji serwera sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="cc63f-147">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="cc63f-148">-Tag</span></span>
<span data-ttu-id="cc63f-149">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc63f-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cc63f-150">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="cc63f-150">-VpnAuthenticationType</span></span>
<span data-ttu-id="cc63f-151">Lista protokołów tunelowania klienta sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="cc63f-151">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="cc63f-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="cc63f-153">Lista zasad IPSec dla VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cc63f-153">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-154">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="cc63f-154">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="cc63f-155">Lista ścieżek VpnClientCertificates do odwołania plików</span><span class="sxs-lookup"><span data-stu-id="cc63f-155">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-156">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="cc63f-156">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="cc63f-157">Lista ścieżek plików VpnClientRootCertificates do dodania</span><span class="sxs-lookup"><span data-stu-id="cc63f-157">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-158">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="cc63f-158">-VpnProtocol</span></span>
<span data-ttu-id="cc63f-159">Lista protokołów tunelowania klienta sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="cc63f-159">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc63f-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc63f-160">-Confirm</span></span>
<span data-ttu-id="cc63f-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc63f-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc63f-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc63f-162">-WhatIf</span></span>
<span data-ttu-id="cc63f-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc63f-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc63f-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc63f-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc63f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc63f-165">CommonParameters</span></span>
<span data-ttu-id="cc63f-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc63f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc63f-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc63f-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc63f-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc63f-168">INPUTS</span></span>

### <span data-ttu-id="cc63f-169">Microsoft. Azure. Commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc63f-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="cc63f-170">System. String Microsoft. Azure. Commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="cc63f-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="cc63f-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc63f-171">OUTPUTS</span></span>

### <span data-ttu-id="cc63f-172">Microsoft. Azure. Commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc63f-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="cc63f-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc63f-173">NOTES</span></span>

## <span data-ttu-id="cc63f-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc63f-174">RELATED LINKS</span></span>
