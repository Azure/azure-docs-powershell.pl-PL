---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 7c6457e30140e10c5e6746c69a213f5ac4932cc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550875"
---
# <span data-ttu-id="4d934-101">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="4d934-101">Remove-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="4d934-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d934-102">SYNOPSIS</span></span>
<span data-ttu-id="4d934-103">Usuwa certyfikat odwołania klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="4d934-103">Removes a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d934-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d934-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d934-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d934-105">DESCRIPTION</span></span>
<span data-ttu-id="4d934-106">Polecenie cmdlet **Remove-AzureRmVpnClientRevokedCertificate** usuwa certyfikat odwołania od klienta z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4d934-106">The **Remove-AzureRmVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="4d934-107">Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="4d934-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="4d934-108">Po usunięciu komputerów klienckich z certyfikatem odwołania klienckiego można użyć certyfikatu, który został wcześniej zabroniony, aby utworzyć połączenie wirtualnej sieci prywatnej (VPN).</span><span class="sxs-lookup"><span data-stu-id="4d934-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="4d934-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d934-109">EXAMPLES</span></span>

### <span data-ttu-id="4d934-110">Przykład 1: Usuwanie certyfikatu odwołania klienta z bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4d934-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="4d934-111">To polecenie usuwa certyfikat odwołania klienta z bramy sieci wirtualnej o nazwie ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="4d934-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="4d934-112">Aby usunąć certyfikat odwołania od klienta, należy określić zarówno nazwę certyfikatu, jak i odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="4d934-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="4d934-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d934-113">PARAMETERS</span></span>

### <span data-ttu-id="4d934-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d934-114">-ResourceGroupName</span></span>
<span data-ttu-id="4d934-115">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4d934-115">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="4d934-116">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d934-116">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="4d934-117">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="4d934-117">-Thumbprint</span></span>
<span data-ttu-id="4d934-118">Określa unikatowy identyfikator usuwanego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="4d934-118">Specifies the unique identifier of the certificate being removed.</span></span>

<span data-ttu-id="4d934-119">Możesz zwrócić informacje o odcisku palca dotyczące certyfikatów przy użyciu polecenia programu Windows PowerShell podobnej do następującego:</span><span class="sxs-lookup"><span data-stu-id="4d934-119">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

<span data-ttu-id="4d934-120">Powyższe polecenie zwraca informacje dotyczące wszystkich certyfikatów komputerów lokalnych znajdujących się w głównym magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="4d934-120">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="4d934-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="4d934-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="4d934-122">Określa nazwę bramy sieci wirtualnej, do której jest przypisany dany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="4d934-122">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="4d934-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="4d934-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="4d934-124">Określa nazwę certyfikatu klienta sieci VPN, który jest usuwany.</span><span class="sxs-lookup"><span data-stu-id="4d934-124">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="4d934-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d934-125">-DefaultProfile</span></span>
<span data-ttu-id="4d934-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d934-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d934-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d934-127">CommonParameters</span></span>
<span data-ttu-id="4d934-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d934-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d934-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d934-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d934-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d934-130">INPUTS</span></span>

## <span data-ttu-id="4d934-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d934-131">OUTPUTS</span></span>

## <span data-ttu-id="4d934-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d934-132">NOTES</span></span>

## <span data-ttu-id="4d934-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d934-133">RELATED LINKS</span></span>

[<span data-ttu-id="4d934-134">Dodaj-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="4d934-134">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="4d934-135">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="4d934-135">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="4d934-136">Nowe — AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="4d934-136">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)


