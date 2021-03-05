---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: e5dd9da25bfa2c27bd605dc80b04f8e47fb7f95b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964122"
---
# <span data-ttu-id="e6565-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6565-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="e6565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6565-102">SYNOPSIS</span></span>
<span data-ttu-id="e6565-103">To polecenie umożliwia użytkownikom utworzenie pakietu profilu vpn na podstawie wstępnie skonfigurowanych ustawień sieci VPN w bramie VPN, a także niektórych dodatkowych ustawień, które użytkownicy mogą konfigurować na przykład na niektórych certyfikatach głównych.</span><span class="sxs-lookup"><span data-stu-id="e6565-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="e6565-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e6565-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6565-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e6565-105">DESCRIPTION</span></span>
<span data-ttu-id="e6565-106">umożliwia to użytkownikom utworzenie pakietu profilu VPN na podstawie wstępnie skonfigurowanych ustawień sieci VPN w bramie VPN, a także niektórych dodatkowych ustawień, które użytkownicy mogą konfigurować na przykład na niektórych certyfikatach głównych.</span><span class="sxs-lookup"><span data-stu-id="e6565-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="e6565-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e6565-107">EXAMPLES</span></span>

### <span data-ttu-id="e6565-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e6565-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="e6565-109">To polecenie cmdlet służy do tworzenia pliku zip profilu klienta VPN dla pliku "ContosoVirtualNetworkGateway" w grupie zasobów "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="e6565-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="e6565-110">Profil jest generowany dla wstępnie skonfigurowanego serwera promieni, który jest skonfigurowany do używania metody uwierzytelniania "EAPTLS" z plikiem certyfikatu VpnProfileRadiusCert.</span><span class="sxs-lookup"><span data-stu-id="e6565-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="e6565-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6565-111">PARAMETERS</span></span>

### <span data-ttu-id="e6565-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="e6565-112">-AuthenticationMethod</span></span>
<span data-ttu-id="e6565-113">Metoda uwierzytelniania może przyjmować wartości EAPMSCHAPv2 lub EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="e6565-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="e6565-114">Gdy zostanie określony protokół EAPMSCHAPv2, polecenie cmdlet generuje instalator konfiguracji klienta dla nazwy użytkownika/uwierzytelnianie hasłem korzystającego z protokołu EAP-MSCHAPv2 uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="e6565-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="e6565-115">Jeśli zostanie określony protokół EAPTLS, polecenie cmdlet wygeneruje instalatora konfiguracji klienta dla uwierzytelniania certyfikatów, który korzysta z protokołu EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="e6565-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="e6565-116">Opcja "EapTls" może być używana zarówno w przypadku uwierzytelniania certyfikatów opartego na funkcji RADIUS, jak i uwierzytelniania certyfikacji wykonywanego przez wirtualną bramę sieciową przez przekazanie zaufanego katalogu głównego.</span><span class="sxs-lookup"><span data-stu-id="e6565-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="e6565-117">Polecenie cmdlet automatycznie wykrywa skonfigurowane ustawienia.</span><span class="sxs-lookup"><span data-stu-id="e6565-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6565-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="e6565-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="e6565-119">Lista głównych ścieżek certyfikatów klienta</span><span class="sxs-lookup"><span data-stu-id="e6565-119">A list of client root certificate paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6565-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6565-120">-DefaultProfile</span></span>
<span data-ttu-id="e6565-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6565-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6565-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e6565-122">-Name</span></span>
<span data-ttu-id="e6565-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e6565-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6565-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="e6565-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="e6565-125">ProcesorArchitecture</span><span class="sxs-lookup"><span data-stu-id="e6565-125">ProcessorArchitecture</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6565-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="e6565-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="e6565-127">Ścieżka certyfikatu głównego serwera Radius.</span><span class="sxs-lookup"><span data-stu-id="e6565-127">Radius server root certificate path.</span></span> <span data-ttu-id="e6565-128">Jest to obowiązkowy parametr, który należy określić podczas korzystania z protokołu EAP-TLS z uwierzytelnianiem RADIUS.</span><span class="sxs-lookup"><span data-stu-id="e6565-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="e6565-129">Jest to nazwa pełnej ścieżki pliku cer zawierającego certyfikat główny RADIUS, który jest używany przez klienta do sprawdzania poprawności serwera RADIUS podczas uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="e6565-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6565-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6565-130">-ResourceGroupName</span></span>
<span data-ttu-id="e6565-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e6565-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6565-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6565-132">-Confirm</span></span>
<span data-ttu-id="e6565-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e6565-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6565-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6565-134">-WhatIf</span></span>
<span data-ttu-id="e6565-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6565-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6565-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e6565-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6565-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6565-137">CommonParameters</span></span>
<span data-ttu-id="e6565-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6565-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6565-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6565-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6565-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6565-140">INPUTS</span></span>

### <span data-ttu-id="e6565-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e6565-141">System.String</span></span>

### <span data-ttu-id="e6565-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e6565-142">System.String[]</span></span>

## <span data-ttu-id="e6565-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6565-143">OUTPUTS</span></span>

### <span data-ttu-id="e6565-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="e6565-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="e6565-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e6565-145">NOTES</span></span>

## <span data-ttu-id="e6565-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6565-146">RELATED LINKS</span></span>

[<span data-ttu-id="e6565-147">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6565-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
