---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: 62fc89cefadc91445a64850d6a0e5ee23d6163f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898330"
---
# <span data-ttu-id="5bbc6-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5bbc6-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="5bbc6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5bbc6-102">SYNOPSIS</span></span>
<span data-ttu-id="5bbc6-103">Pobiera informacje o certyfikatach odwołań klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bbc6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5bbc6-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bbc6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5bbc6-105">DESCRIPTION</span></span>
<span data-ttu-id="5bbc6-106">Polecenie cmdlet **Get-AzureRmVpnClientRevokedCertificate** zwraca informacje o certyfikatach odwołania klienta przypisanych do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="5bbc6-107">Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="5bbc6-108">Polecenie **Get-AzureRmVpnClientRevokedCertificate** umożliwia zwrócenie informacji o wszystkich certyfikatach odwołania klienta na bramie lub za pomocą parametru *VpnClientRevokedCertificateName* w celu uzyskania informacji o jednym certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="5bbc6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5bbc6-109">EXAMPLES</span></span>

### <span data-ttu-id="5bbc6-110">Przykład 1: uzyskiwanie informacji o wszystkich certyfikatach odwołania klienta</span><span class="sxs-lookup"><span data-stu-id="5bbc6-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="5bbc6-111">To polecenie pobiera informacje o wszystkich certyfikatach odwołania klienta skojarzonych z bramą sieci wirtualnej o nazwie ContosoVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="5bbc6-112">Przykład 2: uzyskiwanie informacji o określonych certyfikatach odwołań klienta</span><span class="sxs-lookup"><span data-stu-id="5bbc6-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="5bbc6-113">To polecenie to odmiana polecenia pokazanego w przykładzie 1.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="5bbc6-114">Jednak w tym przypadku parametr *VpnClientRevokedCertificateName* jest wykorzystywany do ograniczania zwracanych danych do określonego certyfikatu odwołanego przez klienta: certyfikat o nazwie ContosoRevokedClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="5bbc6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5bbc6-115">PARAMETERS</span></span>

### <span data-ttu-id="5bbc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bbc6-116">-DefaultProfile</span></span>
<span data-ttu-id="5bbc6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bbc6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bbc6-118">-ResourceGroupName</span></span>
<span data-ttu-id="5bbc6-119">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="5bbc6-120">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="5bbc6-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5bbc6-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5bbc6-122">Określa nazwę bramy sieci wirtualnej, do której przypisano odwołane informacje o certyfikacie.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="5bbc6-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="5bbc6-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="5bbc6-124">Określa nazwę certyfikatu klienta sieci VPN, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bbc6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bbc6-125">CommonParameters</span></span>
<span data-ttu-id="5bbc6-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bbc6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bbc6-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bbc6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bbc6-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bbc6-128">INPUTS</span></span>

## <span data-ttu-id="5bbc6-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5bbc6-129">OUTPUTS</span></span>

###  
<span data-ttu-id="5bbc6-130">Polecenie **Get-AzureRmVpnClientRevokedCertificate** zwraca wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate** .</span><span class="sxs-lookup"><span data-stu-id="5bbc6-130">**Get-AzureRmVpnClientRevokedCertificate** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="5bbc6-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5bbc6-131">NOTES</span></span>

## <span data-ttu-id="5bbc6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bbc6-132">RELATED LINKS</span></span>

[<span data-ttu-id="5bbc6-133">Dodaj-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5bbc6-133">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="5bbc6-134">Nowe — AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5bbc6-134">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="5bbc6-135">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5bbc6-135">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


