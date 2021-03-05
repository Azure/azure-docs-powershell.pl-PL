---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: 42553004f8d084496a1f4809bca408e0b4c62cef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990025"
---
# <span data-ttu-id="49f31-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="49f31-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="49f31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49f31-102">SYNOPSIS</span></span>
<span data-ttu-id="49f31-103">Tworzy obiekt Azure Virtual Hub Route.</span><span class="sxs-lookup"><span data-stu-id="49f31-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="49f31-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49f31-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49f31-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="49f31-105">DESCRIPTION</span></span>
<span data-ttu-id="49f31-106">Tworzy obiekt Azure Virtual Hub Route.</span><span class="sxs-lookup"><span data-stu-id="49f31-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="49f31-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49f31-107">EXAMPLES</span></span>

### <span data-ttu-id="49f31-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49f31-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="49f31-109">Powyższe spowoduje utworzenie obiektu trasy centrum wirtualnego, który może zostać uwzględniony w tabeli tras centrum wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="49f31-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="49f31-110">Trasa centrum wirtualnego to obiekt w pamięci, za pomocą który można utworzyć obiekt VirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="49f31-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="49f31-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49f31-111">PARAMETERS</span></span>

### <span data-ttu-id="49f31-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="49f31-112">-AddressPrefix</span></span>
<span data-ttu-id="49f31-113">Lista prefiksów adresów.</span><span class="sxs-lookup"><span data-stu-id="49f31-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="49f31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f31-114">-DefaultProfile</span></span>
<span data-ttu-id="49f31-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49f31-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49f31-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="49f31-116">-NextHopIpAddress</span></span>
<span data-ttu-id="49f31-117">Adres IpAddress następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="49f31-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="49f31-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f31-118">CommonParameters</span></span>
<span data-ttu-id="49f31-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49f31-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f31-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49f31-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f31-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49f31-121">INPUTS</span></span>

### <span data-ttu-id="49f31-122">Brak</span><span class="sxs-lookup"><span data-stu-id="49f31-122">None</span></span>

## <span data-ttu-id="49f31-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49f31-123">OUTPUTS</span></span>

### <span data-ttu-id="49f31-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="49f31-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="49f31-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49f31-125">NOTES</span></span>

## <span data-ttu-id="49f31-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49f31-126">RELATED LINKS</span></span>

[<span data-ttu-id="49f31-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="49f31-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
