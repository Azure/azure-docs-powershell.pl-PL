---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: b46f346c1aa58b8c6f155ad9a742271fa121f630
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202665"
---
# <span data-ttu-id="048ab-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="048ab-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="048ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="048ab-102">SYNOPSIS</span></span>
<span data-ttu-id="048ab-103">Utwórz nową konfigurację VpnServerConfiguration dla połączeń punktowych z witryną.</span><span class="sxs-lookup"><span data-stu-id="048ab-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="048ab-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="048ab-104">SYNTAX</span></span>

```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="048ab-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="048ab-105">DESCRIPTION</span></span>
<span data-ttu-id="048ab-106">Polecenie cmdlet **New-AzVpnServerConfiguration** umożliwia utworzenie nowej konfiguracji VpnServerConfiguration z różnymi parametrami VpnProtocols, VpnAuthenticationTypes, IpsecPolicies oraz ustawienie wybranych parametrów powiązanych z uwierzytelnianiem sieci vpn zgodnie z wymaganiami klienta w zakresie łączności typu Point to site.</span><span class="sxs-lookup"><span data-stu-id="048ab-106">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="048ab-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="048ab-107">EXAMPLES</span></span>

### <span data-ttu-id="048ab-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="048ab-108">Example 1</span></span>
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

<span data-ttu-id="048ab-109">Powyższe polecenie utworzy nową konfigurację VpnServerConfiguration z certyfikatem VpnAuthenticationType.</span><span class="sxs-lookup"><span data-stu-id="048ab-109">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="048ab-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="048ab-110">Example 2</span></span>

<span data-ttu-id="048ab-111">Utwórz nową konfigurację VpnServerConfiguration dla połączeń punktowych z witryną.</span><span class="sxs-lookup"><span data-stu-id="048ab-111">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="048ab-112">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="048ab-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="048ab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="048ab-113">PARAMETERS</span></span>

### <span data-ttu-id="048ab-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="048ab-114">-AadAudience</span></span>
<span data-ttu-id="048ab-115">Odbiorcy AAD do uwierzytelniania P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="048ab-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="048ab-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="048ab-116">-AadIssuer</span></span>
<span data-ttu-id="048ab-117">Wystawca AAD dla uwierzytelniania P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="048ab-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="048ab-118">- AadTenant</span><span class="sxs-lookup"><span data-stu-id="048ab-118">-AadTenant</span></span>
<span data-ttu-id="048ab-119">Dzierżawa AAD do uwierzytelniania P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="048ab-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="048ab-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="048ab-120">-AsJob</span></span>
<span data-ttu-id="048ab-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="048ab-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="048ab-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048ab-122">-DefaultProfile</span></span>
<span data-ttu-id="048ab-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="048ab-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="048ab-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="048ab-124">-Location</span></span>
<span data-ttu-id="048ab-125">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="048ab-125">The resource location.</span></span>

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

### <span data-ttu-id="048ab-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="048ab-126">-Name</span></span>
<span data-ttu-id="048ab-127">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="048ab-127">The resource name.</span></span>

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

### <span data-ttu-id="048ab-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="048ab-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="048ab-129">Lista ścieżek plików RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="048ab-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="048ab-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="048ab-130">-RadiusServerAddress</span></span>
<span data-ttu-id="048ab-131">Adres serwera o promieniu zewnętrznym P2S.</span><span class="sxs-lookup"><span data-stu-id="048ab-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="048ab-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="048ab-132">-RadiusServerList</span></span>
<span data-ttu-id="048ab-133">P2S Zewnętrzne serwery o wielu promieniach.</span><span class="sxs-lookup"><span data-stu-id="048ab-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="048ab-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="048ab-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="048ab-135">Lista ścieżek plików RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="048ab-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="048ab-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="048ab-136">-RadiusServerSecret</span></span>
<span data-ttu-id="048ab-137">Tajny serwer o promieniu zewnętrznym P2S.</span><span class="sxs-lookup"><span data-stu-id="048ab-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="048ab-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="048ab-138">-ResourceGroupName</span></span>
<span data-ttu-id="048ab-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="048ab-139">The resource group name.</span></span>

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

### <span data-ttu-id="048ab-140">— Tag</span><span class="sxs-lookup"><span data-stu-id="048ab-140">-Tag</span></span>
<span data-ttu-id="048ab-141">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="048ab-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="048ab-142">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="048ab-142">-VpnAuthenticationType</span></span>
<span data-ttu-id="048ab-143">Lista protokołów szyfrowania klienta SIECI VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="048ab-143">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="048ab-144">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="048ab-144">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="048ab-145">Lista zasad IPSec dla konfiguracji vpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="048ab-145">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="048ab-146">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="048ab-146">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="048ab-147">Lista vpnClientCertificates, które mają zostać odwołane ścieżki plików</span><span class="sxs-lookup"><span data-stu-id="048ab-147">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="048ab-148">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="048ab-148">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="048ab-149">Lista elementów VpnClientRootCertificates, które mają zostać dodane ścieżki plików</span><span class="sxs-lookup"><span data-stu-id="048ab-149">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="048ab-150">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="048ab-150">-VpnProtocol</span></span>
<span data-ttu-id="048ab-151">Lista protokołów szyfrowania klienta SIECI VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="048ab-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="048ab-152">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="048ab-152">-Confirm</span></span>
<span data-ttu-id="048ab-153">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="048ab-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="048ab-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="048ab-154">-WhatIf</span></span>
<span data-ttu-id="048ab-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="048ab-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="048ab-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="048ab-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="048ab-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048ab-157">CommonParameters</span></span>
<span data-ttu-id="048ab-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="048ab-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048ab-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="048ab-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048ab-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="048ab-160">INPUTS</span></span>

### <span data-ttu-id="048ab-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="048ab-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="048ab-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="048ab-162">OUTPUTS</span></span>

### <span data-ttu-id="048ab-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="048ab-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="048ab-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="048ab-164">NOTES</span></span>

## <span data-ttu-id="048ab-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="048ab-165">RELATED LINKS</span></span>
