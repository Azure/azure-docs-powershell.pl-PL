---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: 3130aec4a5032fd62423aa35dec73d7acd6e14b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872059"
---
# <span data-ttu-id="5cab5-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="5cab5-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="5cab5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5cab5-102">SYNOPSIS</span></span>
<span data-ttu-id="5cab5-103">Przetestuj dostępność prywatnego adresu IP w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5cab5-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="5cab5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5cab5-104">SYNTAX</span></span>

### <span data-ttu-id="5cab5-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="5cab5-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cab5-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="5cab5-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cab5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5cab5-107">DESCRIPTION</span></span>
<span data-ttu-id="5cab5-108">Polecenie cmdlet **test-AzPrivateIPAddressAvailability** sprawdza, czy określony prywatny adres IP jest dostępny w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5cab5-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="5cab5-109">To polecenie cmdlet zwraca listę dostępnych prywatnych adresów IP, jeśli jest potrzebny żądany prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="5cab5-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="5cab5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5cab5-110">EXAMPLES</span></span>

### <span data-ttu-id="5cab5-111">Przykład 1: Sprawdzanie, czy adres IP jest dostępny za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="5cab5-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="5cab5-112">To polecenie uzyskuje sieć wirtualną i używa operatora potoku w celu przekazania go do **testu-AzPrivateIPAddressAvailability** , który sprawdza, czy określony prywatny adres IP jest dostępny.</span><span class="sxs-lookup"><span data-stu-id="5cab5-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="5cab5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5cab5-113">PARAMETERS</span></span>

### <span data-ttu-id="5cab5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cab5-114">-DefaultProfile</span></span>
<span data-ttu-id="5cab5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5cab5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cab5-116">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="5cab5-116">-IPAddress</span></span>
<span data-ttu-id="5cab5-117">Określa adres IP do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="5cab5-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="5cab5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cab5-118">-ResourceGroupName</span></span>
<span data-ttu-id="5cab5-119">Określa nazwę grupy zasobów dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5cab5-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="5cab5-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cab5-120">-VirtualNetwork</span></span>
<span data-ttu-id="5cab5-121">Określa obiekt **PSVirtualNetwork** .</span><span class="sxs-lookup"><span data-stu-id="5cab5-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="5cab5-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5cab5-122">-VirtualNetworkName</span></span>
<span data-ttu-id="5cab5-123">Określa nazwę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5cab5-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="5cab5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cab5-124">CommonParameters</span></span>
<span data-ttu-id="5cab5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cab5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cab5-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cab5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cab5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cab5-127">INPUTS</span></span>

### <span data-ttu-id="5cab5-128">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cab5-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5cab5-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5cab5-129">OUTPUTS</span></span>

### <span data-ttu-id="5cab5-130">Microsoft. Azure. Commands. Network. models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="5cab5-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="5cab5-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5cab5-131">NOTES</span></span>

## <span data-ttu-id="5cab5-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cab5-132">RELATED LINKS</span></span>

[<span data-ttu-id="5cab5-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cab5-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


