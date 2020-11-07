---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: c73f65866b2a23527540319744854e50f6639268
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718161"
---
# <span data-ttu-id="9bf9a-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9bf9a-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="9bf9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bf9a-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf9a-103">Dodaje certyfikat odwołania klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bf9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bf9a-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bf9a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9bf9a-105">DESCRIPTION</span></span>
<span data-ttu-id="9bf9a-106">Polecenie cmdlet **Add-AzureRmVpnClientRevokedCertificate** przypisuje certyfikat odwołania klienta do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="9bf9a-107">Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="9bf9a-108">Aby użyć tego polecenia cmdlet, należy określić zarówno nazwę certyfikatu, jak i odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="9bf9a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bf9a-109">EXAMPLES</span></span>

### <span data-ttu-id="9bf9a-110">Przykład 1: Dodawanie nowego certyfikatu odwołania klienta do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9bf9a-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="9bf9a-111">To polecenie dodaje nowy certyfikat odwołania klienta do bramy sieci wirtualnej o nazwie ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="9bf9a-112">Aby dodać certyfikat, musisz określić zarówno nazwę certyfikatu, jak i odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="9bf9a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bf9a-113">PARAMETERS</span></span>

### <span data-ttu-id="9bf9a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf9a-114">-ResourceGroupName</span></span>
<span data-ttu-id="9bf9a-115">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-115">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="9bf9a-116">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-116">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="9bf9a-117">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="9bf9a-117">-Thumbprint</span></span>
<span data-ttu-id="9bf9a-118">Określa unikatowy identyfikator dodawanego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-118">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="9bf9a-119">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="9bf9a-119">For example:</span></span>

<span data-ttu-id="9bf9a-120">-Odcisk palca "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="9bf9a-120">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="9bf9a-121">Informacje dotyczące odcisków palców można uzyskać za pomocą polecenia programu Windows PowerShell podobnego do poniższego `Get-ChildItem -Path Cert:\LocalMachine\Root` :</span><span class="sxs-lookup"><span data-stu-id="9bf9a-121">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="9bf9a-122">Powyższe polecenie pobiera informacje dotyczące wszystkich certyfikatów komputerów lokalnych odnalezionych w głównym magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="9bf9a-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="9bf9a-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="9bf9a-124">Określa nazwę bramy sieci wirtualnej, w której ma zostać dodany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="9bf9a-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="9bf9a-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="9bf9a-126">Określa nazwę certyfikatu klienta sieci VPN, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-126">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="9bf9a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf9a-127">-DefaultProfile</span></span>
<span data-ttu-id="9bf9a-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bf9a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf9a-129">CommonParameters</span></span>
<span data-ttu-id="9bf9a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf9a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf9a-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bf9a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf9a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bf9a-132">INPUTS</span></span>

## <span data-ttu-id="9bf9a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bf9a-133">OUTPUTS</span></span>

### <span data-ttu-id="9bf9a-134">Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9bf9a-134">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="9bf9a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bf9a-135">NOTES</span></span>

## <span data-ttu-id="9bf9a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bf9a-136">RELATED LINKS</span></span>

[<span data-ttu-id="9bf9a-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9bf9a-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="9bf9a-138">Nowe — AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9bf9a-138">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="9bf9a-139">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9bf9a-139">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)

