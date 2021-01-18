---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: baf349f56d3ebbf55c21d99dbfefd64ad7b295a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501239"
---
# <span data-ttu-id="3f898-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="3f898-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="3f898-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f898-102">SYNOPSIS</span></span>
<span data-ttu-id="3f898-103">Tworzy obiekt trasy wirtualnego centrum platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3f898-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="3f898-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f898-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f898-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f898-105">DESCRIPTION</span></span>
<span data-ttu-id="3f898-106">Tworzy obiekt trasy wirtualnego centrum platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3f898-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="3f898-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f898-107">EXAMPLES</span></span>

### <span data-ttu-id="3f898-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3f898-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="3f898-109">Powyższy element utworzy obiekt wirtualnej trasy, który będzie można uwzględnić w tabeli routingu centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="3f898-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="3f898-110">Trasa koncentratora wirtualnego jest obiektem znajdującym się w pamięci, za pomocą którego można utworzyć obiekt VirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="3f898-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="3f898-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f898-111">PARAMETERS</span></span>

### <span data-ttu-id="3f898-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3f898-112">-AddressPrefix</span></span>
<span data-ttu-id="3f898-113">Lista prefiksów adresów.</span><span class="sxs-lookup"><span data-stu-id="3f898-113">List of Address Prefixes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f898-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f898-114">-DefaultProfile</span></span>
<span data-ttu-id="3f898-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f898-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f898-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f898-116">-NextHopIpAddress</span></span>
<span data-ttu-id="3f898-117">Adres IP następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="3f898-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="3f898-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f898-118">CommonParameters</span></span>
<span data-ttu-id="3f898-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f898-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f898-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f898-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f898-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f898-121">INPUTS</span></span>

### <span data-ttu-id="3f898-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3f898-122">None</span></span>

## <span data-ttu-id="3f898-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f898-123">OUTPUTS</span></span>

### <span data-ttu-id="3f898-124">Microsoft. Azure. Commands. Network. models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="3f898-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="3f898-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f898-125">NOTES</span></span>

## <span data-ttu-id="3f898-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f898-126">RELATED LINKS</span></span>

[<span data-ttu-id="3f898-127">Nowe — AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3f898-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
