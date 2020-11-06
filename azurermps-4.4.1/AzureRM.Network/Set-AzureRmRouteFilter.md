---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 56f0c3ec3a69819ad7faa28b10d33a3cf751c48f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543204"
---
# <span data-ttu-id="2ac41-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2ac41-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="2ac41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ac41-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac41-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="2ac41-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ac41-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ac41-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ac41-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2ac41-105">DESCRIPTION</span></span>
<span data-ttu-id="2ac41-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="2ac41-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2ac41-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ac41-107">EXAMPLES</span></span>

### <span data-ttu-id="2ac41-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ac41-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2ac41-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="2ac41-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="2ac41-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ac41-110">PARAMETERS</span></span>

### <span data-ttu-id="2ac41-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2ac41-111">-Force</span></span>
<span data-ttu-id="2ac41-112">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="2ac41-112">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="2ac41-113">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2ac41-113">-RouteFilter</span></span>
<span data-ttu-id="2ac41-114">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2ac41-114">The RouteFilter</span></span>

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

### <span data-ttu-id="2ac41-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ac41-115">-Confirm</span></span>
<span data-ttu-id="2ac41-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ac41-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ac41-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ac41-117">-WhatIf</span></span>
<span data-ttu-id="2ac41-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ac41-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ac41-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2ac41-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ac41-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac41-120">-DefaultProfile</span></span>
<span data-ttu-id="2ac41-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac41-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ac41-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac41-122">CommonParameters</span></span>
<span data-ttu-id="2ac41-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac41-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac41-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac41-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac41-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ac41-125">INPUTS</span></span>

### <span data-ttu-id="2ac41-126">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2ac41-126">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2ac41-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ac41-127">OUTPUTS</span></span>

### <span data-ttu-id="2ac41-128">Microsoft. Azure. Commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2ac41-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2ac41-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ac41-129">NOTES</span></span>

## <span data-ttu-id="2ac41-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ac41-130">RELATED LINKS</span></span>

