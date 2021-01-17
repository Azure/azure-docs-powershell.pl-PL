---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385394"
---
# <span data-ttu-id="f292d-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="f292d-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="f292d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f292d-102">SYNOPSIS</span></span>
<span data-ttu-id="f292d-103">Tworzy obiekt StaticRoute, który można następnie dodać do obiektu RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f292d-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="f292d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f292d-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f292d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f292d-105">DESCRIPTION</span></span>
<span data-ttu-id="f292d-106">Tworzy obiekt StaticRoute.</span><span class="sxs-lookup"><span data-stu-id="f292d-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="f292d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f292d-107">EXAMPLES</span></span>

### <span data-ttu-id="f292d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f292d-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="f292d-109">Powyższe polecenie utworzy obiekt StaticRoute, który można następnie dodać do obiektu RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f292d-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="f292d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f292d-110">PARAMETERS</span></span>

### <span data-ttu-id="f292d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f292d-111">-DefaultProfile</span></span>
<span data-ttu-id="f292d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f292d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f292d-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f292d-113">-AddressPrefix</span></span>
<span data-ttu-id="f292d-114">Lista prefiksów adresów.</span><span class="sxs-lookup"><span data-stu-id="f292d-114">List of address prefixes.</span></span>

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

### <span data-ttu-id="f292d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f292d-115">-Name</span></span>
<span data-ttu-id="f292d-116">Nazwa trasy.</span><span class="sxs-lookup"><span data-stu-id="f292d-116">The route name.</span></span>

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

### <span data-ttu-id="f292d-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="f292d-117">-NextHopIpAddress</span></span>
<span data-ttu-id="f292d-118">Adres IP następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="f292d-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="f292d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f292d-119">CommonParameters</span></span>
<span data-ttu-id="f292d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f292d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f292d-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f292d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f292d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f292d-122">INPUTS</span></span>

### <span data-ttu-id="f292d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f292d-123">System.String</span></span>

## <span data-ttu-id="f292d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f292d-124">OUTPUTS</span></span>

### <span data-ttu-id="f292d-125">Microsoft. Azure. Commands. Network. models. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="f292d-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="f292d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f292d-126">NOTES</span></span>

## <span data-ttu-id="f292d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f292d-127">RELATED LINKS</span></span>

[<span data-ttu-id="f292d-128">Nowe — AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="f292d-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
