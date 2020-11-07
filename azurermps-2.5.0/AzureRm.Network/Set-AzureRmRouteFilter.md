---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 895819175f9fe4215d926d57c55307bbb4c75ab3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899064"
---
# <span data-ttu-id="47a59-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="47a59-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="47a59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47a59-102">SYNOPSIS</span></span>
<span data-ttu-id="47a59-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="47a59-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47a59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47a59-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47a59-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47a59-105">DESCRIPTION</span></span>
<span data-ttu-id="47a59-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="47a59-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="47a59-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47a59-107">EXAMPLES</span></span>

### <span data-ttu-id="47a59-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="47a59-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="47a59-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="47a59-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="47a59-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47a59-110">PARAMETERS</span></span>

### <span data-ttu-id="47a59-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47a59-111">-AsJob</span></span>
<span data-ttu-id="47a59-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="47a59-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a59-113">-DefaultProfile</span></span>
<span data-ttu-id="47a59-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47a59-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47a59-115">-Force</span><span class="sxs-lookup"><span data-stu-id="47a59-115">-Force</span></span>
<span data-ttu-id="47a59-116">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="47a59-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a59-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="47a59-117">-RouteFilter</span></span>
<span data-ttu-id="47a59-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="47a59-118">The RouteFilter</span></span>

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

### <span data-ttu-id="47a59-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47a59-119">-Confirm</span></span>
<span data-ttu-id="47a59-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47a59-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a59-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47a59-121">-WhatIf</span></span>
<span data-ttu-id="47a59-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47a59-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47a59-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="47a59-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a59-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a59-124">CommonParameters</span></span>
<span data-ttu-id="47a59-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a59-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a59-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47a59-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a59-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47a59-127">INPUTS</span></span>

### <span data-ttu-id="47a59-128">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="47a59-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="47a59-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47a59-129">OUTPUTS</span></span>

### <span data-ttu-id="47a59-130">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="47a59-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="47a59-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47a59-131">NOTES</span></span>

## <span data-ttu-id="47a59-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47a59-132">RELATED LINKS</span></span>

