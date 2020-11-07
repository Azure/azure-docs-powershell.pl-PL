---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 07618d546ebdadfb3313e17b881a7afbe09d1ff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548887"
---
# <span data-ttu-id="8716a-101">New-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="8716a-101">New-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="8716a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8716a-102">SYNOPSIS</span></span>
<span data-ttu-id="8716a-103">To polecenie umożliwia użytkownikom tworzenie pakietu profilu sieci VPN na podstawie wstępnie skonfigurowanych ustawień sieci VPN w bramie sieci VPN, oprócz dodatkowych ustawień, które mogą być potrzebne użytkownikom do skonfigurowania (na przykład niektóre certyfikaty główne).</span><span class="sxs-lookup"><span data-stu-id="8716a-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8716a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8716a-104">SYNTAX</span></span>

```
New-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8716a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8716a-105">DESCRIPTION</span></span>
<span data-ttu-id="8716a-106">Dzięki temu użytkownicy mogą utworzyć pakiet profilów sieci VPN na podstawie wstępnie skonfigurowanych ustawień sieci VPN w bramie sieci VPN, oprócz dodatkowych ustawień, które użytkownicy mogą potrzebować skonfigurować, na przykład niektóre certyfikaty główne.</span><span class="sxs-lookup"><span data-stu-id="8716a-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="8716a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8716a-107">EXAMPLES</span></span>

### <span data-ttu-id="8716a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8716a-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="8716a-109">To polecenie cmdlet służy do tworzenia pliku zip profilu klienta VPN dla "ContosoVirtualNetworkGateway" w przystawce "ContosoResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="8716a-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="8716a-110">Profil jest generowany dla wstępnie skonfigurowanego serwera RADIUS, który jest skonfigurowany do używania metody uwierzytelniania "EAPTLS" z plikiem certyfikatu VpnProfileRadiusCert.</span><span class="sxs-lookup"><span data-stu-id="8716a-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="8716a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8716a-111">PARAMETERS</span></span>

### <span data-ttu-id="8716a-112">-Metodę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="8716a-112">-AuthenticationMethod</span></span>
<span data-ttu-id="8716a-113">Metoda uwierzytelniania może pobierać wartości EAPMSCHAPv2 lub EAPTLS.</span><span class="sxs-lookup"><span data-stu-id="8716a-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="8716a-114">Gdy EAPMSCHAPv2 jest określony, polecenie cmdlet generuje Instalator konfiguracji klienta dla uwierzytelniania nazwy użytkownika i hasła, który używa protokołu uwierzytelniania EAP-MSCHAPv2.</span><span class="sxs-lookup"><span data-stu-id="8716a-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="8716a-115">Jeśli EAPTLS jest określony, polecenie cmdlet generuje instalatora konfiguracji klienta w celu uwierzytelnienia przy użyciu protokołu EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="8716a-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="8716a-116">Opcja "EapTls" może być używana zarówno do uwierzytelniania certyfikatu opartego na usłudze RADIUS, jak i uwierzytelniania certyfikacji przeprowadzanych przez wirtualną bramę sieciową przez przekazanie zaufanego certyfikatu głównego.</span><span class="sxs-lookup"><span data-stu-id="8716a-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="8716a-117">Polecenie cmdlet automatycznie wykrywa, co jest skonfigurowane.</span><span class="sxs-lookup"><span data-stu-id="8716a-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8716a-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="8716a-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="8716a-119">Lista ścieżek certyfikatów głównych klienta</span><span class="sxs-lookup"><span data-stu-id="8716a-119">A list of client root certificate paths</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8716a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8716a-120">-DefaultProfile</span></span>
<span data-ttu-id="8716a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8716a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8716a-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8716a-122">-Name</span></span>
<span data-ttu-id="8716a-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8716a-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8716a-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="8716a-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="8716a-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="8716a-125">ProcessorArchitecture</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8716a-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="8716a-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="8716a-127">Ścieżka głównego certyfikatu serwera usługi RADIUS.</span><span class="sxs-lookup"><span data-stu-id="8716a-127">Radius server root certificate path.</span></span> <span data-ttu-id="8716a-128">Jest to obowiązkowy parametr, który należy określić, gdy jest używana funkcja EAP-TLS z uwierzytelnianiem usługi RADIUS.</span><span class="sxs-lookup"><span data-stu-id="8716a-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="8716a-129">Jest to pełna nazwa ścieżki pliku CER zawierającego główny certyfikat RADIUS używany przez klienta do sprawdzania poprawności serwera RADIUS podczas uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="8716a-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="8716a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8716a-130">-ResourceGroupName</span></span>
<span data-ttu-id="8716a-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8716a-131">The resource group name.</span></span>

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

### <span data-ttu-id="8716a-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8716a-132">-Confirm</span></span>
<span data-ttu-id="8716a-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8716a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8716a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8716a-134">-WhatIf</span></span>
<span data-ttu-id="8716a-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8716a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8716a-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8716a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8716a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8716a-137">CommonParameters</span></span>
<span data-ttu-id="8716a-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8716a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8716a-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8716a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8716a-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8716a-140">INPUTS</span></span>

### <span data-ttu-id="8716a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8716a-141">System.String</span></span>
<span data-ttu-id="8716a-142">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8716a-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8716a-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8716a-143">OUTPUTS</span></span>

### <span data-ttu-id="8716a-144">Microsoft. Azure. Commands. Network. models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="8716a-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="8716a-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8716a-145">NOTES</span></span>

## <span data-ttu-id="8716a-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8716a-146">RELATED LINKS</span></span>
