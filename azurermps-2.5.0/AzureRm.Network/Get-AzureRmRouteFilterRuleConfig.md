---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: f3b641e3e9229706f3010e7db95480423b06361c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897930"
---
# <span data-ttu-id="c7a00-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7a00-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="c7a00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7a00-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a00-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="c7a00-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7a00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7a00-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7a00-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c7a00-105">DESCRIPTION</span></span>
<span data-ttu-id="c7a00-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="c7a00-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="c7a00-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7a00-107">EXAMPLES</span></span>

### <span data-ttu-id="c7a00-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c7a00-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c7a00-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="c7a00-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c7a00-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7a00-110">PARAMETERS</span></span>

### <span data-ttu-id="c7a00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a00-111">-DefaultProfile</span></span>
<span data-ttu-id="c7a00-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a00-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7a00-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c7a00-113">-Name</span></span>
<span data-ttu-id="c7a00-114">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="c7a00-114">The name of the route filter rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a00-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c7a00-115">-RouteFilter</span></span>
<span data-ttu-id="c7a00-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c7a00-116">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a00-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a00-117">CommonParameters</span></span>
<span data-ttu-id="c7a00-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a00-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a00-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a00-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a00-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7a00-120">INPUTS</span></span>

### <span data-ttu-id="c7a00-121">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c7a00-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c7a00-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7a00-122">OUTPUTS</span></span>

### <span data-ttu-id="c7a00-123">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="c7a00-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="c7a00-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7a00-124">NOTES</span></span>

## <span data-ttu-id="c7a00-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7a00-125">RELATED LINKS</span></span>

