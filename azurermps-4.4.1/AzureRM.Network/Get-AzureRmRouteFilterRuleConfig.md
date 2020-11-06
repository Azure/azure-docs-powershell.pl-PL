---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: cb8c6fcca5fb64427efc17123320d1e2a8156aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546959"
---
# <span data-ttu-id="41911-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41911-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="41911-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41911-102">SYNOPSIS</span></span>
<span data-ttu-id="41911-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="41911-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41911-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41911-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41911-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41911-105">DESCRIPTION</span></span>
<span data-ttu-id="41911-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="41911-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="41911-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41911-107">EXAMPLES</span></span>

### <span data-ttu-id="41911-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="41911-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="41911-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="41911-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="41911-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41911-110">PARAMETERS</span></span>

### <span data-ttu-id="41911-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41911-111">-Name</span></span>
<span data-ttu-id="41911-112">Nazwa reguły filtrowania tras</span><span class="sxs-lookup"><span data-stu-id="41911-112">The name of the route filter rule</span></span>

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

### <span data-ttu-id="41911-113">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="41911-113">-RouteFilter</span></span>
<span data-ttu-id="41911-114">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="41911-114">The RouteFilter</span></span>

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

### <span data-ttu-id="41911-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41911-115">-DefaultProfile</span></span>
<span data-ttu-id="41911-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41911-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41911-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41911-117">CommonParameters</span></span>
<span data-ttu-id="41911-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41911-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41911-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41911-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41911-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41911-120">INPUTS</span></span>

### <span data-ttu-id="41911-121">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="41911-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="41911-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41911-122">OUTPUTS</span></span>

### <span data-ttu-id="41911-123">Microsoft. Azure. Commands. Network. models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="41911-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="41911-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41911-124">NOTES</span></span>

## <span data-ttu-id="41911-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41911-125">RELATED LINKS</span></span>

