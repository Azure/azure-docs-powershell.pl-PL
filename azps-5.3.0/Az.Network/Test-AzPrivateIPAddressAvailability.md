---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: af5e1591e0d5c497b0cfe854235536d7edf404c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490937"
---
# <span data-ttu-id="bfcfb-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="bfcfb-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="bfcfb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bfcfb-102">SYNOPSIS</span></span>
<span data-ttu-id="bfcfb-103">Przetestuj dostępność prywatnego adresu IP w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bfcfb-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="bfcfb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bfcfb-104">SYNTAX</span></span>

### <span data-ttu-id="bfcfb-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="bfcfb-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfcfb-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="bfcfb-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfcfb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bfcfb-107">DESCRIPTION</span></span>
<span data-ttu-id="bfcfb-108">Polecenie cmdlet **test-AzPrivateIPAddressAvailability** sprawdza, czy określony prywatny adres IP jest dostępny w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bfcfb-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="bfcfb-109">To polecenie cmdlet zwraca listę dostępnych prywatnych adresów IP, jeśli jest potrzebny żądany prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="bfcfb-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="bfcfb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bfcfb-110">EXAMPLES</span></span>

### <span data-ttu-id="bfcfb-111">Przykład 1: Sprawdzanie, czy adres IP jest dostępny za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="bfcfb-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="bfcfb-112">To polecenie uzyskuje sieć wirtualną i używa operatora potoku w celu przekazania go do **testu-AzPrivateIPAddressAvailability**, który sprawdza, czy określony prywatny adres IP jest dostępny.</span><span class="sxs-lookup"><span data-stu-id="bfcfb-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability**, which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="bfcfb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfcfb-113">PARAMETERS</span></span>

### <span data-ttu-id="bfcfb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfcfb-114">-DefaultProfile</span></span>
<span data-ttu-id="bfcfb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfcfb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfcfb-116">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="bfcfb-116">-IPAddress</span></span>
<span data-ttu-id="bfcfb-117">Określa adres IP do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="bfcfb-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="bfcfb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfcfb-118">-ResourceGroupName</span></span>
<span data-ttu-id="bfcfb-119">Określa nazwę grupy zasobów dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bfcfb-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcfb-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bfcfb-120">-VirtualNetwork</span></span>
<span data-ttu-id="bfcfb-121">Określa obiekt **PSVirtualNetwork** .</span><span class="sxs-lookup"><span data-stu-id="bfcfb-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: TestByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcfb-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="bfcfb-122">-VirtualNetworkName</span></span>
<span data-ttu-id="bfcfb-123">Określa nazwę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bfcfb-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcfb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfcfb-124">CommonParameters</span></span>
<span data-ttu-id="bfcfb-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfcfb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfcfb-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfcfb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfcfb-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfcfb-127">INPUTS</span></span>

### <span data-ttu-id="bfcfb-128">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bfcfb-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="bfcfb-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bfcfb-129">OUTPUTS</span></span>

### <span data-ttu-id="bfcfb-130">Microsoft. Azure. Commands. Network. models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="bfcfb-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="bfcfb-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bfcfb-131">NOTES</span></span>

## <span data-ttu-id="bfcfb-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfcfb-132">RELATED LINKS</span></span>

[<span data-ttu-id="bfcfb-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bfcfb-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


