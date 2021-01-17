---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 2dee180dff1489779dd2eb34f8bd5e3d8be10b91
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361930"
---
# <span data-ttu-id="a3be5-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a3be5-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="a3be5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3be5-102">SYNOPSIS</span></span>
<span data-ttu-id="a3be5-103">Usuwa certyfikat odwołania klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="a3be5-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="a3be5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3be5-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3be5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3be5-105">DESCRIPTION</span></span>
<span data-ttu-id="a3be5-106">Polecenie cmdlet **Remove-AzVpnClientRevokedCertificate** usuwa certyfikat odwołania od klienta z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a3be5-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="a3be5-107">Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="a3be5-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="a3be5-108">Po usunięciu komputerów klienckich z certyfikatem odwołania klienckiego można użyć certyfikatu, który został wcześniej zabroniony, aby utworzyć połączenie wirtualnej sieci prywatnej (VPN).</span><span class="sxs-lookup"><span data-stu-id="a3be5-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="a3be5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3be5-109">EXAMPLES</span></span>

### <span data-ttu-id="a3be5-110">Przykład 1: Usuwanie certyfikatu odwołania klienta z bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a3be5-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```powershell
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="a3be5-111">To polecenie usuwa certyfikat odwołania klienta z bramy sieci wirtualnej o nazwie ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="a3be5-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="a3be5-112">Aby usunąć certyfikat odwołania od klienta, należy określić zarówno nazwę certyfikatu, jak i odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a3be5-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="a3be5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3be5-113">PARAMETERS</span></span>

### <span data-ttu-id="a3be5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3be5-114">-DefaultProfile</span></span>
<span data-ttu-id="a3be5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3be5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3be5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3be5-116">-ResourceGroupName</span></span>
<span data-ttu-id="a3be5-117">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a3be5-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="a3be5-118">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3be5-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="a3be5-119">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="a3be5-119">-Thumbprint</span></span>
<span data-ttu-id="a3be5-120">Określa unikatowy identyfikator usuwanego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a3be5-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="a3be5-121">Możesz zwrócić informacje o odcisku palca dotyczące certyfikatów przy użyciu polecenia programu Windows PowerShell podobnej do następującego: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="a3be5-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="a3be5-122">Powyższe polecenie zwraca informacje dotyczące wszystkich certyfikatów komputerów lokalnych znajdujących się w głównym magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="a3be5-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="a3be5-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a3be5-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a3be5-124">Określa nazwę bramy sieci wirtualnej, do której jest przypisany dany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="a3be5-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="a3be5-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="a3be5-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="a3be5-126">Określa nazwę certyfikatu klienta sieci VPN, który jest usuwany.</span><span class="sxs-lookup"><span data-stu-id="a3be5-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="a3be5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3be5-127">CommonParameters</span></span>
<span data-ttu-id="a3be5-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3be5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3be5-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3be5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3be5-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3be5-130">INPUTS</span></span>

### <span data-ttu-id="a3be5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a3be5-131">System.String</span></span>

## <span data-ttu-id="a3be5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3be5-132">OUTPUTS</span></span>

### <span data-ttu-id="a3be5-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3be5-133">System.Boolean</span></span>

## <span data-ttu-id="a3be5-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3be5-134">NOTES</span></span>

## <span data-ttu-id="a3be5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3be5-135">RELATED LINKS</span></span>

[<span data-ttu-id="a3be5-136">Dodaj-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a3be5-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="a3be5-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a3be5-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="a3be5-138">Nowe — AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a3be5-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


