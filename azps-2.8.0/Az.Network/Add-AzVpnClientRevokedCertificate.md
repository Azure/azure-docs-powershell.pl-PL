---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 041fc967bc5834ba21f96e75e2f5cdc3687d234c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870316"
---
# <span data-ttu-id="ea122-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ea122-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="ea122-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea122-102">SYNOPSIS</span></span>
<span data-ttu-id="ea122-103">Dodaje certyfikat odwołania klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="ea122-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="ea122-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea122-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea122-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ea122-105">DESCRIPTION</span></span>
<span data-ttu-id="ea122-106">Polecenie cmdlet **Add-AzVpnClientRevokedCertificate** przypisuje certyfikat odwołania klienta do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ea122-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="ea122-107">Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="ea122-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="ea122-108">Aby użyć tego polecenia cmdlet, należy określić zarówno nazwę certyfikatu, jak i odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="ea122-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="ea122-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea122-109">EXAMPLES</span></span>

### <span data-ttu-id="ea122-110">Przykład 1: Dodawanie nowego certyfikatu odwołania klienta do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ea122-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="ea122-111">To polecenie dodaje nowy certyfikat odwołania klienta do bramy sieci wirtualnej o nazwie ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="ea122-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="ea122-112">Aby dodać certyfikat, musisz określić zarówno nazwę certyfikatu, jak i odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="ea122-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="ea122-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea122-113">PARAMETERS</span></span>

### <span data-ttu-id="ea122-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea122-114">-DefaultProfile</span></span>
<span data-ttu-id="ea122-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea122-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea122-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea122-116">-ResourceGroupName</span></span>
<span data-ttu-id="ea122-117">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ea122-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="ea122-118">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea122-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="ea122-119">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="ea122-119">-Thumbprint</span></span>
<span data-ttu-id="ea122-120">Określa unikatowy identyfikator dodawanego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="ea122-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="ea122-121">Na przykład:-odcisk palca "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" możesz uzyskać informacje o odcisku palca, korzystając z polecenia programu Windows PowerShell podobnego do poniższego: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="ea122-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="ea122-122">Powyższe polecenie pobiera informacje dotyczące wszystkich certyfikatów komputerów lokalnych odnalezionych w głównym magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="ea122-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="ea122-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ea122-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ea122-124">Określa nazwę bramy sieci wirtualnej, w której ma zostać dodany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="ea122-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="ea122-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="ea122-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="ea122-126">Określa nazwę certyfikatu klienta sieci VPN, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="ea122-126">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="ea122-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea122-127">CommonParameters</span></span>
<span data-ttu-id="ea122-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea122-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea122-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea122-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea122-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea122-130">INPUTS</span></span>

### <span data-ttu-id="ea122-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ea122-131">System.String</span></span>

## <span data-ttu-id="ea122-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea122-132">OUTPUTS</span></span>

### <span data-ttu-id="ea122-133">Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ea122-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="ea122-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea122-134">NOTES</span></span>

## <span data-ttu-id="ea122-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea122-135">RELATED LINKS</span></span>

[<span data-ttu-id="ea122-136">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ea122-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="ea122-137">Nowe — AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ea122-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="ea122-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ea122-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


