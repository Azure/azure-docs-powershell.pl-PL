---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 552a6a317524de6d0f1db86a9a69a2733826d3f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186794"
---
# <span data-ttu-id="8f568-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f568-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="8f568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f568-102">SYNOPSIS</span></span>
<span data-ttu-id="8f568-103">Aktualizuje istniejącą konfigurację VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8f568-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="8f568-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8f568-104">SYNTAX</span></span>

### <span data-ttu-id="8f568-105">ByVpnServerConfigurationName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="8f568-105">ByVpnServerConfigurationName (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f568-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="8f568-106">ByVpnServerConfigurationObject</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f568-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="8f568-107">ByVpnServerConfigurationResourceId</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f568-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8f568-108">DESCRIPTION</span></span>
<span data-ttu-id="8f568-109">Polecenie cmdlet **Update-AzVpnServerConfiguration** umożliwia aktualizowanie istniejącej konfiguracji VpnServerConfiguration przy użyciu różnych parametrów VpnProtocols, VpnAuthenticationTypes, IpsecPolicies oraz ustawianie wybranych parametrów powiązanych z uwierzytelnianiem vpn zgodnie z wymaganiami klienta w zakresie łączności typu Point to site.</span><span class="sxs-lookup"><span data-stu-id="8f568-109">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="8f568-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8f568-110">EXAMPLES</span></span>

### <span data-ttu-id="8f568-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8f568-111">Example 1</span></span>
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

<span data-ttu-id="8f568-112">Powyższe polecenie zaktualizuje istniejącą konfigurację VpnServerConfiguration przy użyciu połączenia VpnProtocol jako IkeV2.</span><span class="sxs-lookup"><span data-stu-id="8f568-112">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="8f568-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f568-113">PARAMETERS</span></span>

### <span data-ttu-id="8f568-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="8f568-114">-AadAudience</span></span>
<span data-ttu-id="8f568-115">Odbiorcy AAD do uwierzytelniania P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="8f568-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="8f568-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="8f568-116">-AadIssuer</span></span>
<span data-ttu-id="8f568-117">Wystawca AAD dla uwierzytelniania P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="8f568-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="8f568-118">- AadTenant</span><span class="sxs-lookup"><span data-stu-id="8f568-118">-AadTenant</span></span>
<span data-ttu-id="8f568-119">Dzierżawa AAD do uwierzytelniania P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="8f568-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="8f568-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8f568-120">-AsJob</span></span>
<span data-ttu-id="8f568-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8f568-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f568-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f568-122">-DefaultProfile</span></span>
<span data-ttu-id="8f568-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f568-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f568-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f568-124">-InputObject</span></span>
<span data-ttu-id="8f568-125">Obiekt konfiguracji serwera vpn do modyfikacji</span><span class="sxs-lookup"><span data-stu-id="8f568-125">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f568-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8f568-126">-Name</span></span>
<span data-ttu-id="8f568-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8f568-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f568-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="8f568-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="8f568-129">Lista ścieżek plików RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8f568-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="8f568-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="8f568-130">-RadiusServerAddress</span></span>
<span data-ttu-id="8f568-131">Adres serwera o promieniu zewnętrznym P2S.</span><span class="sxs-lookup"><span data-stu-id="8f568-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="8f568-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="8f568-132">-RadiusServerList</span></span>
<span data-ttu-id="8f568-133">P2S Zewnętrzne serwery o wielu promieniach.</span><span class="sxs-lookup"><span data-stu-id="8f568-133">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f568-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="8f568-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="8f568-135">Lista ścieżek plików RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8f568-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="8f568-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="8f568-136">-RadiusServerSecret</span></span>
<span data-ttu-id="8f568-137">Tajny serwer o promieniu zewnętrznym P2S.</span><span class="sxs-lookup"><span data-stu-id="8f568-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="8f568-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f568-138">-ResourceGroupName</span></span>
<span data-ttu-id="8f568-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f568-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f568-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f568-140">-ResourceId</span></span>
<span data-ttu-id="8f568-141">Identyfikator zasobu Azure dla konfiguracji serwera vpn.</span><span class="sxs-lookup"><span data-stu-id="8f568-141">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f568-142">— Tag</span><span class="sxs-lookup"><span data-stu-id="8f568-142">-Tag</span></span>
<span data-ttu-id="8f568-143">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f568-143">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8f568-144">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="8f568-144">-VpnAuthenticationType</span></span>
<span data-ttu-id="8f568-145">Lista protokołów odsyłki klienta VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="8f568-145">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="8f568-146">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="8f568-146">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="8f568-147">Lista zasad IPSec dla konfiguracji vpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8f568-147">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="8f568-148">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="8f568-148">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="8f568-149">Lista vpnClientCertificates, które mają zostać odwołane ścieżki plików</span><span class="sxs-lookup"><span data-stu-id="8f568-149">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="8f568-150">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="8f568-150">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="8f568-151">Lista elementów VpnClientRootCertificates, które mają zostać dodane ścieżki plików</span><span class="sxs-lookup"><span data-stu-id="8f568-151">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="8f568-152">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="8f568-152">-VpnProtocol</span></span>
<span data-ttu-id="8f568-153">Lista protokołów odsyłki klienta VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="8f568-153">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="8f568-154">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f568-154">-Confirm</span></span>
<span data-ttu-id="8f568-155">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8f568-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f568-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f568-156">-WhatIf</span></span>
<span data-ttu-id="8f568-157">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f568-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f568-158">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8f568-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f568-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f568-159">CommonParameters</span></span>
<span data-ttu-id="8f568-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f568-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f568-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f568-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f568-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f568-162">INPUTS</span></span>

### <span data-ttu-id="8f568-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f568-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="8f568-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="8f568-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="8f568-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f568-165">OUTPUTS</span></span>

### <span data-ttu-id="8f568-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f568-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="8f568-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8f568-167">NOTES</span></span>

## <span data-ttu-id="8f568-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f568-168">RELATED LINKS</span></span>
