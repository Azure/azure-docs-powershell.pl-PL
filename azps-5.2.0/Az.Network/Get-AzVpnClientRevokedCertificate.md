---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 04bc51a7040cae1310fd3c4fe51fd45c425fad8e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370671"
---
# <span data-ttu-id="55933-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="55933-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="55933-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55933-102">SYNOPSIS</span></span>
<span data-ttu-id="55933-103">Pobiera informacje o certyfikatach odwołań klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="55933-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="55933-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55933-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55933-105">Opis</span><span class="sxs-lookup"><span data-stu-id="55933-105">DESCRIPTION</span></span>
<span data-ttu-id="55933-106">Polecenie cmdlet **Get-AzVpnClientRevokedCertificate** zwraca informacje o certyfikatach odwołania klienta przypisanych do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="55933-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="55933-107">Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="55933-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="55933-108">Polecenie **Get-AzVpnClientRevokedCertificate** umożliwia zwrócenie informacji o wszystkich certyfikatach odwołania klienta na bramie lub za pomocą parametru *VpnClientRevokedCertificateName* w celu uzyskania informacji o jednym certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="55933-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="55933-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55933-109">EXAMPLES</span></span>

### <span data-ttu-id="55933-110">Przykład 1: uzyskiwanie informacji o wszystkich certyfikatach odwołania klienta</span><span class="sxs-lookup"><span data-stu-id="55933-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="55933-111">To polecenie pobiera informacje o wszystkich certyfikatach odwołania klienta skojarzonych z bramą sieci wirtualnej o nazwie ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="55933-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="55933-112">Przykład 2: uzyskiwanie informacji o określonych certyfikatach odwołań klienta</span><span class="sxs-lookup"><span data-stu-id="55933-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="55933-113">To polecenie to odmiana polecenia pokazanego w przykładzie 1.</span><span class="sxs-lookup"><span data-stu-id="55933-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="55933-114">Jednak w tym przypadku parametr *VpnClientRevokedCertificateName* jest wykorzystywany do ograniczania zwracanych danych do określonego certyfikatu odwołanego przez klienta: certyfikat o nazwie ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="55933-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="55933-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55933-115">PARAMETERS</span></span>

### <span data-ttu-id="55933-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55933-116">-DefaultProfile</span></span>
<span data-ttu-id="55933-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55933-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55933-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55933-118">-ResourceGroupName</span></span>
<span data-ttu-id="55933-119">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="55933-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="55933-120">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55933-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="55933-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="55933-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="55933-122">Określa nazwę bramy sieci wirtualnej, do której przypisano odwołane informacje o certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="55933-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="55933-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="55933-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="55933-124">Określa nazwę certyfikatu klienta sieci VPN, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55933-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="55933-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55933-125">CommonParameters</span></span>
<span data-ttu-id="55933-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55933-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55933-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55933-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55933-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55933-128">INPUTS</span></span>

### <span data-ttu-id="55933-129">System. String</span><span class="sxs-lookup"><span data-stu-id="55933-129">System.String</span></span>

## <span data-ttu-id="55933-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55933-130">OUTPUTS</span></span>

### <span data-ttu-id="55933-131">Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="55933-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="55933-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55933-132">NOTES</span></span>

## <span data-ttu-id="55933-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55933-133">RELATED LINKS</span></span>

[<span data-ttu-id="55933-134">Dodaj-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="55933-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="55933-135">Nowe — AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="55933-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="55933-136">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="55933-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


