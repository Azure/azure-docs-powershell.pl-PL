---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 85a35fe4c6b988ce6f5320d308582fb722cc5791
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964097"
---
# <span data-ttu-id="25c03-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="25c03-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="25c03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25c03-102">SYNOPSIS</span></span>
<span data-ttu-id="25c03-103">Tworzy nowy certyfikat odwołania klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="25c03-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="25c03-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25c03-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25c03-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="25c03-105">DESCRIPTION</span></span>
<span data-ttu-id="25c03-106">Polecenie cmdlet **New-AzVpnClientRevokedCertificate** tworzy nowy certyfikat odwołania klienta wirtualnej sieci prywatnej (VPN) do użytku w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="25c03-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="25c03-107">Certyfikaty odwołań klientów uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="25c03-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="25c03-108">To polecenie cmdlet tworzy autonomiczny certyfikat, który nie jest przypisany do bramy wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="25c03-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="25c03-109">Zamiast tego certyfikat utworzony przez **new-AzVpnClientRevokedCertificate** jest używany w połączeniu z poleceniem cmdlet New-AzVirtualNetworkGateway podczas tworzenia nowej bramy.</span><span class="sxs-lookup"><span data-stu-id="25c03-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="25c03-110">Załóżmy na przykład, że tworzysz nowy certyfikat i przechowujesz go w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="25c03-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="25c03-111">Następnie można użyć tego obiektu certyfikatu podczas tworzenia nowej bramy wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="25c03-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="25c03-112">Na przykład: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="25c03-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="25c03-113">Aby uzyskać więcej informacji, zapoznaj się z dokumentacją tego New-AzVirtualNetworkGateway cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25c03-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="25c03-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25c03-114">EXAMPLES</span></span>

### <span data-ttu-id="25c03-115">Przykład 1. Tworzenie nowego certyfikatu z odwołaniem klienta</span><span class="sxs-lookup"><span data-stu-id="25c03-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="25c03-116">To polecenie tworzy nowy certyfikat odwołany przez klienta i przechowuje obiekt certyfikatu w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="25c03-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="25c03-117">Ta zmienna może być następnie używana przez polecenie cmdlet **New-AzVirtualNetworkGateway** w celu dodania certyfikatu do nowej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="25c03-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="25c03-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25c03-118">PARAMETERS</span></span>

### <span data-ttu-id="25c03-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25c03-119">-DefaultProfile</span></span>
<span data-ttu-id="25c03-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="25c03-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25c03-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="25c03-121">-Name</span></span>
<span data-ttu-id="25c03-122">Określa unikatową nazwę dla nowego certyfikatu odwołania klienta.</span><span class="sxs-lookup"><span data-stu-id="25c03-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="25c03-123">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="25c03-123">-Thumbprint</span></span>
<span data-ttu-id="25c03-124">Określa identyfikator unikatowy dodawana certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="25c03-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="25c03-125">Możesz zwrócić informacje dotyczące kciuka w certyfikatach za pomocą polecenia programu Windows PowerShell podobnego do tego: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="25c03-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="25c03-126">Poprzednie polecenie zwraca informacje dotyczące wszystkich certyfikatów Komputer lokalny znalezionych w magazynie certyfikatów głównych.</span><span class="sxs-lookup"><span data-stu-id="25c03-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="25c03-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25c03-127">CommonParameters</span></span>
<span data-ttu-id="25c03-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25c03-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25c03-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25c03-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25c03-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25c03-130">INPUTS</span></span>

### <span data-ttu-id="25c03-131">Brak</span><span class="sxs-lookup"><span data-stu-id="25c03-131">None</span></span>

## <span data-ttu-id="25c03-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25c03-132">OUTPUTS</span></span>

### <span data-ttu-id="25c03-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="25c03-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="25c03-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25c03-134">NOTES</span></span>

## <span data-ttu-id="25c03-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25c03-135">RELATED LINKS</span></span>

[<span data-ttu-id="25c03-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="25c03-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="25c03-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="25c03-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="25c03-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="25c03-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


