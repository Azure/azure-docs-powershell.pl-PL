---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 3cf1bea87824320b659def722d0d0f0166fa177d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053828"
---
# <span data-ttu-id="a7b45-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7b45-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="a7b45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7b45-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b45-103">Pobiera informacje o certyfikatach głównych sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="a7b45-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="a7b45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7b45-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7b45-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a7b45-105">DESCRIPTION</span></span>
<span data-ttu-id="a7b45-106">Polecenie cmdlet **Get-AzVpnClientRootCertificate** zwraca informacje o certyfikatach głównych przypisanych do bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a7b45-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="a7b45-107">Certyfikaty główne to certyfikaty X. 509, które identyfikują główny urząd certyfikacji: wszystkie inne certyfikaty używane w bramie ufają certyfikatowi głównemu.</span><span class="sxs-lookup"><span data-stu-id="a7b45-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="a7b45-108">Domyślnie funkcja **Get-AzVpnClientRootCertificate** zwraca informacje o wszystkich certyfikatach głównych przypisanych do bramy.</span><span class="sxs-lookup"><span data-stu-id="a7b45-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="a7b45-109">(Bramy mogą mieć więcej niż jeden certyfikat główny). Jednak dołączając parametr **VpnClientRootCertificateName** , możesz ograniczyć zwrócone dane do określonego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a7b45-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="a7b45-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7b45-110">EXAMPLES</span></span>

### <span data-ttu-id="a7b45-111">Przykład 1: uzyskiwanie informacji o wszystkich certyfikatach głównych</span><span class="sxs-lookup"><span data-stu-id="a7b45-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="a7b45-112">To polecenie pobiera informacje o wszystkich certyfikatach głównych przypisanych do bramy sieci wirtualnej o nazwie ContosoVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="a7b45-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="a7b45-113">Przykład 2: uzyskiwanie informacji o określonych certyfikatach głównych</span><span class="sxs-lookup"><span data-stu-id="a7b45-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="a7b45-114">To polecenie to odmiana polecenia pokazanego w przykładzie 1.</span><span class="sxs-lookup"><span data-stu-id="a7b45-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="a7b45-115">W tym przypadku jednak parametr *VpnClientRootCertificateName* jest uwzględniany w celu ograniczenia zwracanych danych do określonego certyfikatu głównego: ContosoRootClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="a7b45-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="a7b45-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7b45-116">PARAMETERS</span></span>

### <span data-ttu-id="a7b45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b45-117">-DefaultProfile</span></span>
<span data-ttu-id="a7b45-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b45-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7b45-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7b45-119">-ResourceGroupName</span></span>
<span data-ttu-id="a7b45-120">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a7b45-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="a7b45-121">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b45-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="a7b45-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a7b45-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a7b45-123">Określa nazwę bramy sieci wirtualnej, do której jest przypisany certyfikat główny.</span><span class="sxs-lookup"><span data-stu-id="a7b45-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="a7b45-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="a7b45-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="a7b45-125">Określa nazwę certyfikatu głównego klienta, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7b45-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b45-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b45-126">CommonParameters</span></span>
<span data-ttu-id="a7b45-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7b45-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b45-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7b45-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b45-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7b45-129">INPUTS</span></span>

### <span data-ttu-id="a7b45-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a7b45-130">System.String</span></span>

## <span data-ttu-id="a7b45-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7b45-131">OUTPUTS</span></span>

### <span data-ttu-id="a7b45-132">Microsoft. Azure. Commands. Network. models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7b45-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="a7b45-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7b45-133">NOTES</span></span>

## <span data-ttu-id="a7b45-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7b45-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7b45-135">Dodaj-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7b45-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="a7b45-136">Nowe — AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7b45-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="a7b45-137">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a7b45-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


