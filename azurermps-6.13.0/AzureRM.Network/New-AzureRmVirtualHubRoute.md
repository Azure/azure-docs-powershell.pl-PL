---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
ms.openlocfilehash: 7197c90e5d5cb0c8a0e15b5e16d1a3c05aaeebf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549344"
---
# <span data-ttu-id="718a5-101">New-AzureRmVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="718a5-101">New-AzureRmVirtualHubRoute</span></span>

## <span data-ttu-id="718a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="718a5-102">SYNOPSIS</span></span>
<span data-ttu-id="718a5-103">Tworzy obiekt trasy wirtualnego centrum platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="718a5-103">Creates an Azure Virtual Hub Route object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="718a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="718a5-104">SYNTAX</span></span>

```
New-AzureRmVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="718a5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="718a5-105">DESCRIPTION</span></span>
<span data-ttu-id="718a5-106">Tworzy obiekt trasy wirtualnego centrum platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="718a5-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="718a5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="718a5-107">EXAMPLES</span></span>

### <span data-ttu-id="718a5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="718a5-108">Example 1</span></span>

```powershell
PS C:\> $route1 = 

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="718a5-109">Powyższy element utworzy obiekt wirtualnej trasy, który będzie można uwzględnić w tabeli routingu centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="718a5-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="718a5-110">Trasa koncentratora wirtualnego jest obiektem znajdującym się w pamięci, za pomocą którego można utworzyć obiekt VirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="718a5-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="718a5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="718a5-111">PARAMETERS</span></span>

### <span data-ttu-id="718a5-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="718a5-112">-AddressPrefix</span></span>
<span data-ttu-id="718a5-113">Lista prefiksów adresów.</span><span class="sxs-lookup"><span data-stu-id="718a5-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="718a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="718a5-114">-DefaultProfile</span></span>
<span data-ttu-id="718a5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="718a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="718a5-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="718a5-116">-NextHopIpAddress</span></span>
<span data-ttu-id="718a5-117">Adres IP następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="718a5-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="718a5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="718a5-118">CommonParameters</span></span>
<span data-ttu-id="718a5-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="718a5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="718a5-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="718a5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="718a5-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="718a5-121">INPUTS</span></span>

### <span data-ttu-id="718a5-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="718a5-122">None</span></span>

## <span data-ttu-id="718a5-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="718a5-123">OUTPUTS</span></span>

### <span data-ttu-id="718a5-124">Microsoft. Azure. Commands. Network. models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="718a5-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="718a5-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="718a5-125">NOTES</span></span>

## <span data-ttu-id="718a5-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="718a5-126">RELATED LINKS</span></span>
