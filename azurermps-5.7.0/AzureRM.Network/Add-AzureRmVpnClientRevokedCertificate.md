---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8f1c81dbfb3d8c42b359464ce33a0053fdc25143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718910"
---
# <span data-ttu-id="94710-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="94710-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="94710-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94710-102">SYNOPSIS</span></span>
<span data-ttu-id="94710-103">Dodaje certyfikat odwołania klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="94710-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94710-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94710-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94710-105">Opis</span><span class="sxs-lookup"><span data-stu-id="94710-105">DESCRIPTION</span></span>
<span data-ttu-id="94710-106">Polecenie cmdlet **Add-AzureRmVpnClientRevokedCertificate** przypisuje certyfikat odwołania klienta do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="94710-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="94710-107">Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="94710-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="94710-108">Aby użyć tego polecenia cmdlet, należy określić zarówno nazwę certyfikatu, jak i odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="94710-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="94710-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94710-109">EXAMPLES</span></span>

### <span data-ttu-id="94710-110">Przykład 1: Dodawanie nowego certyfikatu odwołania klienta do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="94710-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="94710-111">To polecenie dodaje nowy certyfikat odwołania klienta do bramy sieci wirtualnej o nazwie ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="94710-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="94710-112">Aby dodać certyfikat, musisz określić zarówno nazwę certyfikatu, jak i odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="94710-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="94710-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94710-113">PARAMETERS</span></span>

### <span data-ttu-id="94710-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94710-114">-DefaultProfile</span></span>
<span data-ttu-id="94710-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94710-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94710-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94710-116">-ResourceGroupName</span></span>
<span data-ttu-id="94710-117">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="94710-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="94710-118">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94710-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="94710-119">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="94710-119">-Thumbprint</span></span>
<span data-ttu-id="94710-120">Określa unikatowy identyfikator dodawanego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="94710-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="94710-121">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="94710-121">For example:</span></span>

<span data-ttu-id="94710-122">-Odcisk palca "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="94710-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="94710-123">Informacje dotyczące odcisków palców można uzyskać za pomocą polecenia programu Windows PowerShell podobnego do poniższego `Get-ChildItem -Path Cert:\LocalMachine\Root` :</span><span class="sxs-lookup"><span data-stu-id="94710-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="94710-124">Powyższe polecenie pobiera informacje dotyczące wszystkich certyfikatów komputerów lokalnych odnalezionych w głównym magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="94710-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="94710-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="94710-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="94710-126">Określa nazwę bramy sieci wirtualnej, w której ma zostać dodany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="94710-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="94710-127">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="94710-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="94710-128">Określa nazwę certyfikatu klienta sieci VPN, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="94710-128">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="94710-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94710-129">CommonParameters</span></span>
<span data-ttu-id="94710-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94710-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94710-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94710-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94710-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94710-132">INPUTS</span></span>

### <span data-ttu-id="94710-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="94710-133">None</span></span>
<span data-ttu-id="94710-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="94710-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="94710-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94710-135">OUTPUTS</span></span>

### <span data-ttu-id="94710-136">Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="94710-136">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="94710-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94710-137">NOTES</span></span>

## <span data-ttu-id="94710-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94710-138">RELATED LINKS</span></span>

[<span data-ttu-id="94710-139">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="94710-139">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="94710-140">Nowe — AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="94710-140">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="94710-141">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="94710-141">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


