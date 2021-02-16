---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 2dee180dff1489779dd2eb34f8bd5e3d8be10b91
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179410"
---
# <span data-ttu-id="bf67e-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bf67e-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="bf67e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf67e-102">SYNOPSIS</span></span>
<span data-ttu-id="bf67e-103">Usuwa certyfikat odwołania klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="bf67e-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="bf67e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bf67e-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf67e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bf67e-105">DESCRIPTION</span></span>
<span data-ttu-id="bf67e-106">Polecenie **cmdlet Remove-AzVpnClientRevokedCertificate** usuwa certyfikat odwołania klienta z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bf67e-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="bf67e-107">Certyfikaty odwołań klientów uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="bf67e-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="bf67e-108">Jeśli usuniesz klientów klientów z certyfikatem odwołania klienta, mogą użyć poprzednio zablokowanego certyfikatu w celu nawiązaniu połączenia z wirtualną siecią prywatną (VPN).</span><span class="sxs-lookup"><span data-stu-id="bf67e-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="bf67e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bf67e-109">EXAMPLES</span></span>

### <span data-ttu-id="bf67e-110">Przykład 1. Usuwanie certyfikatu odwołania klienta z bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="bf67e-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```powershell
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="bf67e-111">To polecenie usuwa certyfikat odwołania klienta z wirtualnej bramy sieciowej o nazwie ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="bf67e-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="bf67e-112">Aby usunąć certyfikat odwołania klienta, należy określić zarówno nazwę certyfikatu, jak i certyfikat thumbprint.</span><span class="sxs-lookup"><span data-stu-id="bf67e-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="bf67e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf67e-113">PARAMETERS</span></span>

### <span data-ttu-id="bf67e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf67e-114">-DefaultProfile</span></span>
<span data-ttu-id="bf67e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf67e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf67e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf67e-116">-ResourceGroupName</span></span>
<span data-ttu-id="bf67e-117">Określa nazwę grupy zasobów, do których przypisano bramę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bf67e-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="bf67e-118">Grupy zasobów kategoryzowają elementy, aby uprościć zarządzanie zapasami i ogólną administrację azure.</span><span class="sxs-lookup"><span data-stu-id="bf67e-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="bf67e-119">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="bf67e-119">-Thumbprint</span></span>
<span data-ttu-id="bf67e-120">Określa identyfikator unikatowy usunięcia certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bf67e-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="bf67e-121">Możesz zwrócić informacje dotyczące kciuka w certyfikatach za pomocą polecenia programu Windows PowerShell podobnego do tego: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="bf67e-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="bf67e-122">Poprzednie polecenie zwraca informacje dotyczące wszystkich certyfikatów Komputer lokalny znalezionych w głównym magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="bf67e-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="bf67e-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="bf67e-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="bf67e-124">Określa nazwę bramy sieci wirtualnej, do których jest przypisany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="bf67e-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="bf67e-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="bf67e-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="bf67e-126">Określa nazwę usuwanego certyfikatu klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="bf67e-126">Specifies the name of the VPN client certificate being removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf67e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf67e-127">CommonParameters</span></span>
<span data-ttu-id="bf67e-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf67e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf67e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf67e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf67e-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf67e-130">INPUTS</span></span>

### <span data-ttu-id="bf67e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bf67e-131">System.String</span></span>

## <span data-ttu-id="bf67e-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf67e-132">OUTPUTS</span></span>

### <span data-ttu-id="bf67e-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf67e-133">System.Boolean</span></span>

## <span data-ttu-id="bf67e-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bf67e-134">NOTES</span></span>

## <span data-ttu-id="bf67e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf67e-135">RELATED LINKS</span></span>

[<span data-ttu-id="bf67e-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bf67e-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="bf67e-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bf67e-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="bf67e-138">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="bf67e-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


