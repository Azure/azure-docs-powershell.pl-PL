---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 861ea7bcfbfbe8a713934e2dc80a4448a2a98c48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709055"
---
# <span data-ttu-id="413d6-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="413d6-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="413d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="413d6-102">SYNOPSIS</span></span>
<span data-ttu-id="413d6-103">Usuwa certyfikat odwołania klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="413d6-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="413d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="413d6-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="413d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="413d6-105">DESCRIPTION</span></span>
<span data-ttu-id="413d6-106">Polecenie cmdlet **Remove-AzVpnClientRevokedCertificate** usuwa certyfikat odwołania od klienta z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="413d6-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="413d6-107">Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="413d6-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="413d6-108">Po usunięciu komputerów klienckich z certyfikatem odwołania klienckiego można użyć certyfikatu, który został wcześniej zabroniony, aby utworzyć połączenie wirtualnej sieci prywatnej (VPN).</span><span class="sxs-lookup"><span data-stu-id="413d6-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="413d6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="413d6-109">EXAMPLES</span></span>

### <span data-ttu-id="413d6-110">Przykład 1: Usuwanie certyfikatu odwołania klienta z bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="413d6-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="413d6-111">To polecenie usuwa certyfikat odwołania klienta z bramy sieci wirtualnej o nazwie ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="413d6-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="413d6-112">Aby usunąć certyfikat odwołania od klienta, należy określić zarówno nazwę certyfikatu, jak i odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="413d6-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="413d6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="413d6-113">PARAMETERS</span></span>

### <span data-ttu-id="413d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413d6-114">-DefaultProfile</span></span>
<span data-ttu-id="413d6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="413d6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="413d6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="413d6-116">-ResourceGroupName</span></span>
<span data-ttu-id="413d6-117">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="413d6-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="413d6-118">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="413d6-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="413d6-119">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="413d6-119">-Thumbprint</span></span>
<span data-ttu-id="413d6-120">Określa unikatowy identyfikator usuwanego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="413d6-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="413d6-121">Możesz zwrócić informacje o odcisku palca dotyczące certyfikatów przy użyciu polecenia programu Windows PowerShell podobnej do następującego: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="413d6-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="413d6-122">Powyższe polecenie zwraca informacje dotyczące wszystkich certyfikatów komputerów lokalnych znajdujących się w głównym magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="413d6-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="413d6-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="413d6-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="413d6-124">Określa nazwę bramy sieci wirtualnej, do której jest przypisany dany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="413d6-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="413d6-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="413d6-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="413d6-126">Określa nazwę certyfikatu klienta sieci VPN, który jest usuwany.</span><span class="sxs-lookup"><span data-stu-id="413d6-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="413d6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413d6-127">CommonParameters</span></span>
<span data-ttu-id="413d6-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="413d6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413d6-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="413d6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413d6-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="413d6-130">INPUTS</span></span>

### <span data-ttu-id="413d6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="413d6-131">System.String</span></span>

## <span data-ttu-id="413d6-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="413d6-132">OUTPUTS</span></span>

### <span data-ttu-id="413d6-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="413d6-133">System.Boolean</span></span>

## <span data-ttu-id="413d6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="413d6-134">NOTES</span></span>

## <span data-ttu-id="413d6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="413d6-135">RELATED LINKS</span></span>

[<span data-ttu-id="413d6-136">Dodaj-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="413d6-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="413d6-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="413d6-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="413d6-138">Nowe — AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="413d6-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


