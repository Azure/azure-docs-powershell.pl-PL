---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063930"
---
# <span data-ttu-id="33976-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="33976-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="33976-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33976-102">SYNOPSIS</span></span>
<span data-ttu-id="33976-103">Tworzy obiekt StaticRoute, który można następnie dodać do obiektu RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="33976-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="33976-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33976-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33976-105">Opis</span><span class="sxs-lookup"><span data-stu-id="33976-105">DESCRIPTION</span></span>
<span data-ttu-id="33976-106">Tworzy obiekt StaticRoute.</span><span class="sxs-lookup"><span data-stu-id="33976-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="33976-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33976-107">EXAMPLES</span></span>

### <span data-ttu-id="33976-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="33976-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="33976-109">Powyższe polecenie utworzy obiekt StaticRoute, który można następnie dodać do obiektu RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="33976-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="33976-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33976-110">PARAMETERS</span></span>

### <span data-ttu-id="33976-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33976-111">-DefaultProfile</span></span>
<span data-ttu-id="33976-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33976-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33976-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="33976-113">-AddressPrefix</span></span>
<span data-ttu-id="33976-114">Lista prefiksów adresów.</span><span class="sxs-lookup"><span data-stu-id="33976-114">List of address prefixes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33976-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="33976-115">-Name</span></span>
<span data-ttu-id="33976-116">Nazwa trasy.</span><span class="sxs-lookup"><span data-stu-id="33976-116">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33976-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="33976-117">-NextHopIpAddress</span></span>
<span data-ttu-id="33976-118">Adres IP następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="33976-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="33976-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33976-119">CommonParameters</span></span>
<span data-ttu-id="33976-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33976-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33976-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33976-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33976-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33976-122">INPUTS</span></span>

### <span data-ttu-id="33976-123">System. String</span><span class="sxs-lookup"><span data-stu-id="33976-123">System.String</span></span>

## <span data-ttu-id="33976-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33976-124">OUTPUTS</span></span>

### <span data-ttu-id="33976-125">Microsoft. Azure. Commands. Network. models. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="33976-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="33976-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33976-126">NOTES</span></span>

## <span data-ttu-id="33976-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33976-127">RELATED LINKS</span></span>

[<span data-ttu-id="33976-128">Nowe — AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="33976-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
