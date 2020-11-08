---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: e9dfe0e7ed4612ca99a2decf3aa91b521a7e9664
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219843"
---
# <span data-ttu-id="77b26-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="77b26-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="77b26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77b26-102">SYNOPSIS</span></span>
<span data-ttu-id="77b26-103">Ustawia Cennik dla zakresu w warstwie usługi Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="77b26-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="77b26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77b26-104">SYNTAX</span></span>

### <span data-ttu-id="77b26-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77b26-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77b26-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="77b26-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77b26-107">Opis</span><span class="sxs-lookup"><span data-stu-id="77b26-107">DESCRIPTION</span></span>
<span data-ttu-id="77b26-108">Ustawia Cennik dla zakresu w warstwie usługi Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="77b26-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="77b26-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77b26-109">EXAMPLES</span></span>

### <span data-ttu-id="77b26-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77b26-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="77b26-111">Ustawia warstwę cenową usługi Azure Security Center na "standardową"</span><span class="sxs-lookup"><span data-stu-id="77b26-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>


## <span data-ttu-id="77b26-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77b26-112">PARAMETERS</span></span>

### <span data-ttu-id="77b26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b26-113">-DefaultProfile</span></span>
<span data-ttu-id="77b26-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77b26-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b26-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77b26-115">-InputObject</span></span>
<span data-ttu-id="77b26-116">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="77b26-116">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77b26-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77b26-117">-Name</span></span>
<span data-ttu-id="77b26-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="77b26-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b26-119">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="77b26-119">-PricingTier</span></span>
<span data-ttu-id="77b26-120">Warstwa cenowa.</span><span class="sxs-lookup"><span data-stu-id="77b26-120">Pricing Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b26-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77b26-121">-Confirm</span></span>
<span data-ttu-id="77b26-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77b26-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77b26-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77b26-123">-WhatIf</span></span>
<span data-ttu-id="77b26-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77b26-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77b26-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77b26-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77b26-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b26-126">CommonParameters</span></span>
<span data-ttu-id="77b26-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77b26-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b26-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77b26-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b26-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77b26-129">INPUTS</span></span>

### <span data-ttu-id="77b26-130">Microsoft. Azure. Commands. Security. MODELES. ceny. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="77b26-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="77b26-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77b26-131">OUTPUTS</span></span>

### <span data-ttu-id="77b26-132">Microsoft. Azure. Commands. Security. MODELES. ceny. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="77b26-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="77b26-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77b26-133">NOTES</span></span>

## <span data-ttu-id="77b26-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77b26-134">RELATED LINKS</span></span>
