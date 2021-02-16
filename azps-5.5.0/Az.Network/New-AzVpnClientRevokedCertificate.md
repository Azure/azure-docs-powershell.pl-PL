---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193539"
---
# <span data-ttu-id="69bf0-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="69bf0-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="69bf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="69bf0-103">Tworzy nowy certyfikat odwołania klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="69bf0-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="69bf0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69bf0-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69bf0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="69bf0-105">DESCRIPTION</span></span>
<span data-ttu-id="69bf0-106">Polecenie cmdlet **New-AzVpnClientRevokedCertificate** tworzy nowy certyfikat odwołania klienta wirtualnej sieci prywatnej (VPN) do użytku w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="69bf0-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="69bf0-107">Certyfikaty odwołań klientów uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="69bf0-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="69bf0-108">To polecenie cmdlet tworzy autonomiczny certyfikat, który nie jest przypisany do bramy wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="69bf0-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="69bf0-109">Zamiast tego certyfikat utworzony przez **new-AzVpnClientRevokedCertificate** jest używany w połączeniu z poleceniem cmdlet New-AzVirtualNetworkGateway podczas tworzenia nowej bramy.</span><span class="sxs-lookup"><span data-stu-id="69bf0-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="69bf0-110">Załóżmy na przykład, że tworzysz nowy certyfikat i przechowujesz go w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="69bf0-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="69bf0-111">Następnie można użyć tego obiektu certyfikatu podczas tworzenia nowej bramy wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="69bf0-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="69bf0-112">Na przykład: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="69bf0-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="69bf0-113">Aby uzyskać więcej informacji, zapoznaj się z dokumentacją tego New-AzVirtualNetworkGateway cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69bf0-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="69bf0-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69bf0-114">EXAMPLES</span></span>

### <span data-ttu-id="69bf0-115">Przykład 1. Tworzenie nowego certyfikatu z odwołaniem klienta</span><span class="sxs-lookup"><span data-stu-id="69bf0-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="69bf0-116">To polecenie tworzy nowy certyfikat odwołany przez klienta i przechowuje obiekt certyfikatu w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="69bf0-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="69bf0-117">Ta zmienna może być następnie używana przez polecenie cmdlet **New-AzVirtualNetworkGateway** w celu dodania certyfikatu do nowej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="69bf0-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="69bf0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69bf0-118">PARAMETERS</span></span>

### <span data-ttu-id="69bf0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69bf0-119">-DefaultProfile</span></span>
<span data-ttu-id="69bf0-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69bf0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69bf0-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="69bf0-121">-Name</span></span>
<span data-ttu-id="69bf0-122">Określa unikatową nazwę dla nowego certyfikatu odwołania klienta.</span><span class="sxs-lookup"><span data-stu-id="69bf0-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="69bf0-123">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="69bf0-123">-Thumbprint</span></span>
<span data-ttu-id="69bf0-124">Określa identyfikator unikatowy dodawana certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="69bf0-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="69bf0-125">Możesz zwrócić informacje dotyczące kciuka w certyfikatach za pomocą polecenia programu Windows PowerShell podobnego do tego: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="69bf0-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="69bf0-126">Poprzednie polecenie zwraca informacje dotyczące wszystkich certyfikatów Komputer lokalny znalezionych w głównym magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="69bf0-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="69bf0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69bf0-127">CommonParameters</span></span>
<span data-ttu-id="69bf0-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69bf0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69bf0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69bf0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69bf0-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69bf0-130">INPUTS</span></span>

### <span data-ttu-id="69bf0-131">Brak</span><span class="sxs-lookup"><span data-stu-id="69bf0-131">None</span></span>

## <span data-ttu-id="69bf0-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69bf0-132">OUTPUTS</span></span>

### <span data-ttu-id="69bf0-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="69bf0-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="69bf0-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69bf0-134">NOTES</span></span>

## <span data-ttu-id="69bf0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69bf0-135">RELATED LINKS</span></span>

[<span data-ttu-id="69bf0-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="69bf0-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="69bf0-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="69bf0-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="69bf0-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="69bf0-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


