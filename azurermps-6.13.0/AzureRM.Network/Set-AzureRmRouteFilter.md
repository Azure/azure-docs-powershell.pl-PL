---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 5dc2b6a9650cdf4110858edf1b061f69adac48f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717388"
---
# <span data-ttu-id="0b8e8-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0b8e8-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="0b8e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b8e8-102">SYNOPSIS</span></span>
<span data-ttu-id="0b8e8-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="0b8e8-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b8e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b8e8-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b8e8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0b8e8-105">DESCRIPTION</span></span>
<span data-ttu-id="0b8e8-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="0b8e8-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="0b8e8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b8e8-107">EXAMPLES</span></span>

### <span data-ttu-id="0b8e8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0b8e8-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0b8e8-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="0b8e8-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="0b8e8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b8e8-110">PARAMETERS</span></span>

### <span data-ttu-id="0b8e8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b8e8-111">-AsJob</span></span>
<span data-ttu-id="0b8e8-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0b8e8-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b8e8-113">-DefaultProfile</span></span>
<span data-ttu-id="0b8e8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b8e8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0b8e8-115">-Force</span></span>
<span data-ttu-id="0b8e8-116">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="0b8e8-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8e8-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0b8e8-117">-RouteFilter</span></span>
<span data-ttu-id="0b8e8-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0b8e8-118">The RouteFilter</span></span>

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

### <span data-ttu-id="0b8e8-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b8e8-119">-Confirm</span></span>
<span data-ttu-id="0b8e8-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8e8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b8e8-121">-WhatIf</span></span>
<span data-ttu-id="0b8e8-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b8e8-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b8e8-124">CommonParameters</span></span>
<span data-ttu-id="0b8e8-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b8e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b8e8-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b8e8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b8e8-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b8e8-127">INPUTS</span></span>

### <span data-ttu-id="0b8e8-128">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0b8e8-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="0b8e8-129">Parametry: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0b8e8-129">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="0b8e8-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b8e8-130">OUTPUTS</span></span>

### <span data-ttu-id="0b8e8-131">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0b8e8-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="0b8e8-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b8e8-132">NOTES</span></span>

## <span data-ttu-id="0b8e8-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b8e8-133">RELATED LINKS</span></span>
