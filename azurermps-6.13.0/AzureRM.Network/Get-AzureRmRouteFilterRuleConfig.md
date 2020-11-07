---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 96122c68317166f078d40be8cee9d0124c4d713e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717068"
---
# <span data-ttu-id="da9b5-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da9b5-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="da9b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da9b5-102">SYNOPSIS</span></span>
<span data-ttu-id="da9b5-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="da9b5-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da9b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da9b5-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da9b5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da9b5-105">DESCRIPTION</span></span>
<span data-ttu-id="da9b5-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="da9b5-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="da9b5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da9b5-107">EXAMPLES</span></span>

### <span data-ttu-id="da9b5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da9b5-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="da9b5-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="da9b5-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="da9b5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da9b5-110">PARAMETERS</span></span>

### <span data-ttu-id="da9b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da9b5-111">-DefaultProfile</span></span>
<span data-ttu-id="da9b5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da9b5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da9b5-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da9b5-113">-Name</span></span>
<span data-ttu-id="da9b5-114">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="da9b5-114">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da9b5-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="da9b5-115">-RouteFilter</span></span>
<span data-ttu-id="da9b5-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="da9b5-116">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da9b5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da9b5-117">CommonParameters</span></span>
<span data-ttu-id="da9b5-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da9b5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da9b5-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da9b5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da9b5-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da9b5-120">INPUTS</span></span>

### <span data-ttu-id="da9b5-121">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="da9b5-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="da9b5-122">Parametry: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="da9b5-122">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="da9b5-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da9b5-123">OUTPUTS</span></span>

### <span data-ttu-id="da9b5-124">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="da9b5-124">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="da9b5-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da9b5-125">NOTES</span></span>

## <span data-ttu-id="da9b5-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da9b5-126">RELATED LINKS</span></span>
