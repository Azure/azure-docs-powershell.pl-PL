---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: de0806585cee16eed19291766ab29696a9a1b960
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895853"
---
# <span data-ttu-id="03548-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="03548-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="03548-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03548-102">SYNOPSIS</span></span>
<span data-ttu-id="03548-103">Utwórz nowy VpnServerConfiguration, aby wskazać łączność witryny.</span><span class="sxs-lookup"><span data-stu-id="03548-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="03548-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03548-104">SYNTAX</span></span>

### <span data-ttu-id="03548-105">ByVpnServerConfigurationNameByCertificateAuthentication (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03548-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03548-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="03548-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03548-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="03548-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03548-108">Opis</span><span class="sxs-lookup"><span data-stu-id="03548-108">DESCRIPTION</span></span>
<span data-ttu-id="03548-109">Polecenie cmdlet **New-AzVpnServerConfiguration** umożliwia tworzenie nowych VpnServerConfiguration przy użyciu różnych VpnProtocols, VpnAuthenticationTypes, IpsecPolicies i Ustawianie wybranych parametrów związanych z typem uwierzytelniania sieci VPN zgodnie z wymaganiami klienta dotyczącymi łączności witryny.</span><span class="sxs-lookup"><span data-stu-id="03548-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="03548-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03548-110">EXAMPLES</span></span>

### <span data-ttu-id="03548-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03548-111">Example 1</span></span>
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

<span data-ttu-id="03548-112">Powyższe polecenie utworzy nowy VpnServerConfiguration z VpnAuthenticationType jako certyfikat.</span><span class="sxs-lookup"><span data-stu-id="03548-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

## <span data-ttu-id="03548-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03548-113">PARAMETERS</span></span>

### <span data-ttu-id="03548-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="03548-114">-AadAudience</span></span>
<span data-ttu-id="03548-115">Grupa odbiorców AAD dla uwierzytelniania w usłudze AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="03548-115">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="03548-116">-AadIssuer</span></span>
<span data-ttu-id="03548-117">Wystawca AAD dla uwierzytelniania w usłudze P2S w usłudze AAD.</span><span class="sxs-lookup"><span data-stu-id="03548-117">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="03548-118">-AadTenant</span></span>
<span data-ttu-id="03548-119">Dzierżawa AAD na potrzeby uwierzytelniania w usłudze P2S w usłudze AAD.</span><span class="sxs-lookup"><span data-stu-id="03548-119">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03548-120">-AsJob</span></span>
<span data-ttu-id="03548-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="03548-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03548-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03548-122">-DefaultProfile</span></span>
<span data-ttu-id="03548-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03548-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03548-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="03548-124">-Location</span></span>
<span data-ttu-id="03548-125">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="03548-125">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03548-126">-Name</span></span>
<span data-ttu-id="03548-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="03548-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="03548-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="03548-129">Lista ścieżek plików RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="03548-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="03548-130">-RadiusServerAddress</span></span>
<span data-ttu-id="03548-131">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="03548-131">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-132">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="03548-132">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="03548-133">Lista ścieżek plików RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="03548-133">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-134">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="03548-134">-RadiusServerSecret</span></span>
<span data-ttu-id="03548-135">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="03548-135">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03548-136">-ResourceGroupName</span></span>
<span data-ttu-id="03548-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03548-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="03548-138">-Tag</span></span>
<span data-ttu-id="03548-139">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="03548-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-140">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="03548-140">-VpnAuthenticationType</span></span>
<span data-ttu-id="03548-141">Lista protokołów tunelowania klienta sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="03548-141">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-142">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="03548-142">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="03548-143">Lista zasad IPSec dla VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="03548-143">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03548-144">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="03548-144">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="03548-145">Lista ścieżek VpnClientCertificates do odwołania plików</span><span class="sxs-lookup"><span data-stu-id="03548-145">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-146">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="03548-146">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="03548-147">Lista ścieżek plików VpnClientRootCertificates do dodania</span><span class="sxs-lookup"><span data-stu-id="03548-147">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-148">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="03548-148">-VpnProtocol</span></span>
<span data-ttu-id="03548-149">Lista protokołów tunelowania klienta sieci VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="03548-149">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03548-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03548-150">-Confirm</span></span>
<span data-ttu-id="03548-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03548-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03548-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03548-152">-WhatIf</span></span>
<span data-ttu-id="03548-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03548-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03548-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03548-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03548-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03548-155">CommonParameters</span></span>
<span data-ttu-id="03548-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03548-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03548-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03548-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03548-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03548-158">INPUTS</span></span>

### <span data-ttu-id="03548-159">Microsoft. Azure. Commands. Network. models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="03548-159">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="03548-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03548-160">OUTPUTS</span></span>

### <span data-ttu-id="03548-161">Microsoft. Azure. Commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="03548-161">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="03548-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03548-162">NOTES</span></span>

## <span data-ttu-id="03548-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03548-163">RELATED LINKS</span></span>
