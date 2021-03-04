---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: 2cf661ab2bcc531c0a88ae86934a53b212bb91d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953777"
---
# <span data-ttu-id="60e5b-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="60e5b-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="60e5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="60e5b-103">Tworzy obiekt StaticRoute, który można następnie dodać do obiektu RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="60e5b-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="60e5b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="60e5b-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60e5b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="60e5b-105">DESCRIPTION</span></span>
<span data-ttu-id="60e5b-106">Tworzy obiekt StaticRoute.</span><span class="sxs-lookup"><span data-stu-id="60e5b-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="60e5b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="60e5b-107">EXAMPLES</span></span>

### <span data-ttu-id="60e5b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60e5b-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="60e5b-109">Powyższe polecenie utworzy obiekt StaticRoute, który można następnie dodać do obiektu RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="60e5b-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="60e5b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60e5b-110">PARAMETERS</span></span>

### <span data-ttu-id="60e5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e5b-111">-DefaultProfile</span></span>
<span data-ttu-id="60e5b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="60e5b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60e5b-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="60e5b-113">-AddressPrefix</span></span>
<span data-ttu-id="60e5b-114">Lista prefiksów adresów.</span><span class="sxs-lookup"><span data-stu-id="60e5b-114">List of address prefixes.</span></span>

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

### <span data-ttu-id="60e5b-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="60e5b-115">-Name</span></span>
<span data-ttu-id="60e5b-116">Nazwa trasy.</span><span class="sxs-lookup"><span data-stu-id="60e5b-116">The route name.</span></span>

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

### <span data-ttu-id="60e5b-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="60e5b-117">-NextHopIpAddress</span></span>
<span data-ttu-id="60e5b-118">Adres IP następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="60e5b-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="60e5b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e5b-119">CommonParameters</span></span>
<span data-ttu-id="60e5b-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60e5b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e5b-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60e5b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e5b-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60e5b-122">INPUTS</span></span>

### <span data-ttu-id="60e5b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="60e5b-123">System.String</span></span>

## <span data-ttu-id="60e5b-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60e5b-124">OUTPUTS</span></span>

### <span data-ttu-id="60e5b-125">Microsoft.Azure.Commands.Network.Models.PS ZSzybkiRoute</span><span class="sxs-lookup"><span data-stu-id="60e5b-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="60e5b-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="60e5b-126">NOTES</span></span>

## <span data-ttu-id="60e5b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60e5b-127">RELATED LINKS</span></span>

[<span data-ttu-id="60e5b-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="60e5b-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
