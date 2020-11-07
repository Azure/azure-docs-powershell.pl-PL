---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
ms.openlocfilehash: 769f8a5f8f95e5a97af8a495e0edbaba6b75a5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545532"
---
# <span data-ttu-id="e36c1-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="e36c1-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="e36c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e36c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e36c1-103">Przetestuj dostępność prywatnego adresu IP w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e36c1-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e36c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e36c1-104">SYNTAX</span></span>

### <span data-ttu-id="e36c1-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="e36c1-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e36c1-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="e36c1-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e36c1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e36c1-107">DESCRIPTION</span></span>
<span data-ttu-id="e36c1-108">Polecenie cmdlet **test-AzureRmPrivateIPAddressAvailability** sprawdza, czy określony prywatny adres IP jest dostępny w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e36c1-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="e36c1-109">To polecenie cmdlet zwraca listę dostępnych prywatnych adresów IP, jeśli jest potrzebny żądany prywatny adres IP.</span><span class="sxs-lookup"><span data-stu-id="e36c1-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="e36c1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e36c1-110">EXAMPLES</span></span>

### <span data-ttu-id="e36c1-111">Przykład 1: Sprawdzanie, czy adres IP jest dostępny za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="e36c1-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="e36c1-112">To polecenie uzyskuje sieć wirtualną i używa operatora potoku w celu przekazania go do **testu-AzureRmPrivateIPAddressAvailability** , który sprawdza, czy określony prywatny adres IP jest dostępny.</span><span class="sxs-lookup"><span data-stu-id="e36c1-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="e36c1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e36c1-113">PARAMETERS</span></span>

### <span data-ttu-id="e36c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36c1-114">-DefaultProfile</span></span>
<span data-ttu-id="e36c1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e36c1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e36c1-116">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="e36c1-116">-IPAddress</span></span>
<span data-ttu-id="e36c1-117">Określa adres IP do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="e36c1-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="e36c1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e36c1-118">-ResourceGroupName</span></span>
<span data-ttu-id="e36c1-119">Określa nazwę grupy zasobów dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e36c1-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36c1-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e36c1-120">-VirtualNetwork</span></span>
<span data-ttu-id="e36c1-121">Określa obiekt **PSVirtualNetwork** .</span><span class="sxs-lookup"><span data-stu-id="e36c1-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: TestByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e36c1-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e36c1-122">-VirtualNetworkName</span></span>
<span data-ttu-id="e36c1-123">Określa nazwę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e36c1-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36c1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36c1-124">CommonParameters</span></span>
<span data-ttu-id="e36c1-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36c1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36c1-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e36c1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36c1-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e36c1-127">INPUTS</span></span>

### <span data-ttu-id="e36c1-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e36c1-128">PSVirtualNetwork</span></span>
<span data-ttu-id="e36c1-129">Parametr "VirtualNetwork" akceptuje wartość typu "PSVirtualNetwork" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="e36c1-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="e36c1-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e36c1-130">OUTPUTS</span></span>

### <span data-ttu-id="e36c1-131">Microsoft. Azure. Commands. Network. models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="e36c1-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="e36c1-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e36c1-132">NOTES</span></span>

## <span data-ttu-id="e36c1-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e36c1-133">RELATED LINKS</span></span>

[<span data-ttu-id="e36c1-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e36c1-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

