---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 942669106e70bbb8c5b5b6f059fe934effe9b7fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892733"
---
# <span data-ttu-id="7dad7-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7dad7-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="7dad7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7dad7-102">SYNOPSIS</span></span>
<span data-ttu-id="7dad7-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="7dad7-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="7dad7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7dad7-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dad7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7dad7-105">DESCRIPTION</span></span>
<span data-ttu-id="7dad7-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="7dad7-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="7dad7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7dad7-107">EXAMPLES</span></span>

### <span data-ttu-id="7dad7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7dad7-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7dad7-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="7dad7-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="7dad7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7dad7-110">PARAMETERS</span></span>

### <span data-ttu-id="7dad7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7dad7-111">-AsJob</span></span>
<span data-ttu-id="7dad7-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7dad7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7dad7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dad7-113">-DefaultProfile</span></span>
<span data-ttu-id="7dad7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7dad7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dad7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7dad7-115">-Force</span></span>
<span data-ttu-id="7dad7-116">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="7dad7-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="7dad7-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7dad7-117">-RouteFilter</span></span>
<span data-ttu-id="7dad7-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7dad7-118">The RouteFilter</span></span>

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

### <span data-ttu-id="7dad7-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7dad7-119">-Confirm</span></span>
<span data-ttu-id="7dad7-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dad7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dad7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dad7-121">-WhatIf</span></span>
<span data-ttu-id="7dad7-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dad7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7dad7-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7dad7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dad7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dad7-124">CommonParameters</span></span>
<span data-ttu-id="7dad7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dad7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dad7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dad7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dad7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dad7-127">INPUTS</span></span>

### <span data-ttu-id="7dad7-128">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7dad7-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7dad7-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7dad7-129">OUTPUTS</span></span>

### <span data-ttu-id="7dad7-130">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7dad7-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7dad7-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7dad7-131">NOTES</span></span>

## <span data-ttu-id="7dad7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dad7-132">RELATED LINKS</span></span>

