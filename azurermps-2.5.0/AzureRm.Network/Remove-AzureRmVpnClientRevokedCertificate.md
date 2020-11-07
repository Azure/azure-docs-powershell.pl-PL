---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: ce4d2c61feb20c750d908b6f235d89dafa713e62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899221"
---
# <span data-ttu-id="5448b-101">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5448b-101">Remove-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="5448b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5448b-102">SYNOPSIS</span></span>
<span data-ttu-id="5448b-103">Usuwa certyfikat odwołania klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="5448b-103">Removes a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5448b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5448b-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5448b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5448b-105">DESCRIPTION</span></span>
<span data-ttu-id="5448b-106">Polecenie cmdlet **Remove-AzureRmVpnClientRevokedCertificate** usuwa certyfikat odwołania od klienta z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5448b-106">The **Remove-AzureRmVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="5448b-107">Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="5448b-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="5448b-108">Po usunięciu komputerów klienckich z certyfikatem odwołania klienckiego można użyć certyfikatu, który został wcześniej zabroniony, aby utworzyć połączenie wirtualnej sieci prywatnej (VPN).</span><span class="sxs-lookup"><span data-stu-id="5448b-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="5448b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5448b-109">EXAMPLES</span></span>

### <span data-ttu-id="5448b-110">Przykład 1: Usuwanie certyfikatu odwołania klienta z bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5448b-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="5448b-111">To polecenie usuwa certyfikat odwołania klienta z bramy sieci wirtualnej o nazwie ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="5448b-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="5448b-112">Aby usunąć certyfikat odwołania od klienta, należy określić zarówno nazwę certyfikatu, jak i odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5448b-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="5448b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5448b-113">PARAMETERS</span></span>

### <span data-ttu-id="5448b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5448b-114">-DefaultProfile</span></span>
<span data-ttu-id="5448b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5448b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5448b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5448b-116">-ResourceGroupName</span></span>
<span data-ttu-id="5448b-117">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5448b-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="5448b-118">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5448b-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="5448b-119">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="5448b-119">-Thumbprint</span></span>
<span data-ttu-id="5448b-120">Określa unikatowy identyfikator usuwanego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="5448b-120">Specifies the unique identifier of the certificate being removed.</span></span>

<span data-ttu-id="5448b-121">Możesz zwrócić informacje o odcisku palca dotyczące certyfikatów przy użyciu polecenia programu Windows PowerShell podobnej do następującego:</span><span class="sxs-lookup"><span data-stu-id="5448b-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

<span data-ttu-id="5448b-122">Powyższe polecenie zwraca informacje dotyczące wszystkich certyfikatów komputerów lokalnych znajdujących się w głównym magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="5448b-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="5448b-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5448b-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5448b-124">Określa nazwę bramy sieci wirtualnej, do której jest przypisany dany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="5448b-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="5448b-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="5448b-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="5448b-126">Określa nazwę certyfikatu klienta sieci VPN, który jest usuwany.</span><span class="sxs-lookup"><span data-stu-id="5448b-126">Specifies the name of the VPN client certificate being removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5448b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5448b-127">CommonParameters</span></span>
<span data-ttu-id="5448b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5448b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5448b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5448b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5448b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5448b-130">INPUTS</span></span>

## <span data-ttu-id="5448b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5448b-131">OUTPUTS</span></span>

## <span data-ttu-id="5448b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5448b-132">NOTES</span></span>

## <span data-ttu-id="5448b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5448b-133">RELATED LINKS</span></span>

[<span data-ttu-id="5448b-134">Dodaj-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5448b-134">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="5448b-135">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5448b-135">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="5448b-136">Nowe — AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5448b-136">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)


