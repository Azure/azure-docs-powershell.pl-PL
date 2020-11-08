---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: 10feda31a97582ef56300b570ce2768c3ea0e277
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223766"
---
# <span data-ttu-id="b88dd-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b88dd-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="b88dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b88dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b88dd-103">Utwórz nowy VpnServerConfiguration, aby wskazać łączność witryny.</span><span class="sxs-lookup"><span data-stu-id="b88dd-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="b88dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b88dd-104">SYNTAX</span></span>

### <span data-ttu-id="b88dd-105">ByVpnServerConfigurationNameByCertificateAuthentication (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b88dd-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b88dd-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="b88dd-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b88dd-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="b88dd-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b88dd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b88dd-108">DESCRIPTION</span></span>
<span data-ttu-id="b88dd-109">Polecenie cmdlet **New-AzVpnServerConfiguration** umożliwia tworzenie nowych VpnServerConfiguration przy użyciu różnych VpnProtocols, VpnAuthenticationTypes, IpsecPolicies i Ustawianie wybranych parametrów związanych z typem uwierzytelniania sieci VPN zgodnie z wymaganiami klienta dotyczącymi łączności witryny.</span><span class="sxs-lookup"><span data-stu-id="b88dd-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="b88dd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b88dd-110">EXAMPLES</span></span>

### <span data-ttu-id="b88dd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b88dd-111">Example 1</span></span>
```powershell
PS C:\> $VpnServerConfigCertFilePath = Join-Path -Path $basedir -ChildPath "\ScenarioTests\Data\ApplicationGatewayAuthCert.cer"
PS C:\> $listOfCerts = New-Object "System.Collections.Generic.List[String]"
PS C:\> $listOfCerts.Add($VpnServerConfigCertFilePath)
PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
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

<span data-ttu-id="b88dd-112">Powyższe polecenie utworzy nowy VpnServerConfiguration z VpnAuthenticationType jako certyfikat.</span><span class="sxs-lookup"><span data-stu-id="b88dd-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="b88dd-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b88dd-113">Example 2</span></span>

<span data-ttu-id="b88dd-114">Utwórz nowy VpnServerConfiguration, aby wskazać łączność witryny.</span><span class="sxs-lookup"><span data-stu-id="b88dd-114">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="b88dd-115">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="b88dd-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="b88dd-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b88dd-116">PARAMETERS</span></span>

### <span data-ttu-id="b88dd-117">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="b88dd-117">-AadAudience</span></span>
<span data-ttu-id="b88dd-118">Grupa odbiorców AAD dla uwierzytelniania w usłudze AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="b88dd-118">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88dd-119">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="b88dd-119">-AadIssuer</span></span>
<span data-ttu-id="b88dd-120">Wystawca AAD dla uwierzytelniania w usłudze P2S w usłudze AAD.</span><span class="sxs-lookup"><span data-stu-id="b88dd-120">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88dd-121">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="b88dd-121">-AadTenant</span></span>
<span data-ttu-id="b88dd-122">Dzierżawa AAD na potrzeby uwierzytelniania w usłudze P2S w usłudze AAD.</span><span class="sxs-lookup"><span data-stu-id="b88dd-122">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88dd-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b88dd-123">-AsJob</span></span>
<span data-ttu-id="b88dd-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b88dd-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b88dd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b88dd-125">-DefaultProfile</span></span>
<span data-ttu-id="b88dd-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b88dd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b88dd-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b88dd-127">-Location</span></span>
<span data-ttu-id="b88dd-128">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b88dd-128">The resource location.</span></span>

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

### <span data-ttu-id="b88dd-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b88dd-129">-Name</span></span>
<span data-ttu-id="b88dd-130">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b88dd-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88dd-131">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b88dd-131">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="b88dd-132">Lista ścieżek plików RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b88dd-132">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88dd-133">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="b88dd-133">-RadiusServerAddress</span></span>
<span data-ttu-id="b88dd-134">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b88dd-134">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88dd-135">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="b88dd-135">-RadiusServerList</span></span>
<span data-ttu-id="b88dd-136">P2S zewnętrzne serwery RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b88dd-136">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88dd-137">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b88dd-137">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="b88dd-138">Lista ścieżek plików RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b88dd-138">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88dd-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="b88dd-139">-RadiusServerSecret</span></span>
<span data-ttu-id="b88dd-140">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b88dd-140">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88dd-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b88dd-141">-ResourceGroupName</span></span>
<span data-ttu-id="b88dd-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b88dd-142">The resource group name.</span></span>

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

### <span data-ttu-id="b88dd-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="b88dd-143">-Tag</span></span>
<span data-ttu-id="b88dd-144">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="b88dd-144">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b88dd-145">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="b88dd-145">-VpnAuthenticationType</span></span>
<span data-ttu-id="b88dd-146">Lista protokołów tunelowania klienta sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="b88dd-146">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="b88dd-147">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="b88dd-147">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="b88dd-148">Lista zasad IPSec dla VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b88dd-148">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b88dd-149">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b88dd-149">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="b88dd-150">Lista ścieżek VpnClientCertificates do odwołania plików</span><span class="sxs-lookup"><span data-stu-id="b88dd-150">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88dd-151">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="b88dd-151">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="b88dd-152">Lista ścieżek plików VpnClientRootCertificates do dodania</span><span class="sxs-lookup"><span data-stu-id="b88dd-152">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88dd-153">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="b88dd-153">-VpnProtocol</span></span>
<span data-ttu-id="b88dd-154">Lista protokołów tunelowania klienta sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="b88dd-154">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="b88dd-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b88dd-155">-Confirm</span></span>
<span data-ttu-id="b88dd-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b88dd-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b88dd-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b88dd-157">-WhatIf</span></span>
<span data-ttu-id="b88dd-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b88dd-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b88dd-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b88dd-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b88dd-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b88dd-160">CommonParameters</span></span>
<span data-ttu-id="b88dd-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b88dd-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b88dd-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b88dd-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b88dd-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b88dd-163">INPUTS</span></span>

### <span data-ttu-id="b88dd-164">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="b88dd-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="b88dd-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b88dd-165">OUTPUTS</span></span>

### <span data-ttu-id="b88dd-166">Microsoft. Azure. Commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b88dd-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="b88dd-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b88dd-167">NOTES</span></span>

## <span data-ttu-id="b88dd-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b88dd-168">RELATED LINKS</span></span>
