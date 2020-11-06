---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: bb6a4c13b65697de624e9a9913e2f0f9cc6ea476
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543731"
---
# <span data-ttu-id="368cd-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="368cd-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="368cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="368cd-102">SYNOPSIS</span></span>
<span data-ttu-id="368cd-103">Pobiera informacje o certyfikatach odwołań klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="368cd-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="368cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="368cd-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="368cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="368cd-105">DESCRIPTION</span></span>
<span data-ttu-id="368cd-106">Polecenie cmdlet **Get-AzureRmVpnClientRevokedCertificate** zwraca informacje o certyfikatach odwołania klienta przypisanych do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="368cd-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="368cd-107">Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="368cd-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="368cd-108">Polecenie **Get-AzureRmVpnClientRevokedCertificate** umożliwia zwrócenie informacji o wszystkich certyfikatach odwołania klienta na bramie lub za pomocą parametru *VpnClientRevokedCertificateName* w celu uzyskania informacji o jednym certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="368cd-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="368cd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="368cd-109">EXAMPLES</span></span>

### <span data-ttu-id="368cd-110">Przykład 1: uzyskiwanie informacji o wszystkich certyfikatach odwołania klienta</span><span class="sxs-lookup"><span data-stu-id="368cd-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="368cd-111">To polecenie pobiera informacje o wszystkich certyfikatach odwołania klienta skojarzonych z bramą sieci wirtualnej o nazwie ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="368cd-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="368cd-112">Przykład 2: uzyskiwanie informacji o określonych certyfikatach odwołań klienta</span><span class="sxs-lookup"><span data-stu-id="368cd-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="368cd-113">To polecenie to odmiana polecenia pokazanego w przykładzie 1.</span><span class="sxs-lookup"><span data-stu-id="368cd-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="368cd-114">Jednak w tym przypadku parametr *VpnClientRevokedCertificateName* jest wykorzystywany do ograniczania zwracanych danych do określonego certyfikatu odwołanego przez klienta: certyfikat o nazwie ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="368cd-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="368cd-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="368cd-115">PARAMETERS</span></span>

### <span data-ttu-id="368cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="368cd-116">-DefaultProfile</span></span>
<span data-ttu-id="368cd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="368cd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="368cd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="368cd-118">-ResourceGroupName</span></span>
<span data-ttu-id="368cd-119">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="368cd-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="368cd-120">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="368cd-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="368cd-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="368cd-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="368cd-122">Określa nazwę bramy sieci wirtualnej, do której przypisano odwołane informacje o certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="368cd-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="368cd-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="368cd-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="368cd-124">Określa nazwę certyfikatu klienta sieci VPN, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="368cd-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="368cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="368cd-125">CommonParameters</span></span>
<span data-ttu-id="368cd-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="368cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="368cd-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="368cd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="368cd-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="368cd-128">INPUTS</span></span>

### <span data-ttu-id="368cd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="368cd-129">System.String</span></span>

## <span data-ttu-id="368cd-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="368cd-130">OUTPUTS</span></span>

### <span data-ttu-id="368cd-131">Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="368cd-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="368cd-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="368cd-132">NOTES</span></span>

## <span data-ttu-id="368cd-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="368cd-133">RELATED LINKS</span></span>

[<span data-ttu-id="368cd-134">Dodaj-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="368cd-134">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="368cd-135">Nowe — AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="368cd-135">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="368cd-136">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="368cd-136">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


