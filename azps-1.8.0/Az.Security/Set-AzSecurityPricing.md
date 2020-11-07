---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: a52ae3b59cc7cbf99bf7f4751a36f271bc9610de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708188"
---
# <span data-ttu-id="d8515-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="d8515-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="d8515-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8515-102">SYNOPSIS</span></span>
<span data-ttu-id="d8515-103">Ustawia Cennik dla zakresu w warstwie usługi Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="d8515-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="d8515-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8515-104">SYNTAX</span></span>

### <span data-ttu-id="d8515-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d8515-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8515-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="d8515-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8515-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d8515-107">DESCRIPTION</span></span>
<span data-ttu-id="d8515-108">Ustawia Cennik dla zakresu w warstwie usługi Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="d8515-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="d8515-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8515-109">EXAMPLES</span></span>

### <span data-ttu-id="d8515-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d8515-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="d8515-111">Ustawia warstwę cenową usługi Azure Security Center na "standardową"</span><span class="sxs-lookup"><span data-stu-id="d8515-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="d8515-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d8515-112">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="d8515-113">Ustawia warstwę zasobów Centrum zabezpieczeń usługi Azure w grupie zasób "myService1"</span><span class="sxs-lookup"><span data-stu-id="d8515-113">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="d8515-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8515-114">PARAMETERS</span></span>

### <span data-ttu-id="d8515-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8515-115">-DefaultProfile</span></span>
<span data-ttu-id="d8515-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8515-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8515-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d8515-117">-InputObject</span></span>
<span data-ttu-id="d8515-118">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="d8515-118">Input Object.</span></span>

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

### <span data-ttu-id="d8515-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d8515-119">-Name</span></span>
<span data-ttu-id="d8515-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d8515-120">Resource name.</span></span>

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

### <span data-ttu-id="d8515-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="d8515-121">-PricingTier</span></span>
<span data-ttu-id="d8515-122">Warstwa cenowa.</span><span class="sxs-lookup"><span data-stu-id="d8515-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="d8515-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8515-123">-Confirm</span></span>
<span data-ttu-id="d8515-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8515-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8515-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8515-125">-WhatIf</span></span>
<span data-ttu-id="d8515-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8515-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8515-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d8515-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8515-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8515-128">CommonParameters</span></span>
<span data-ttu-id="d8515-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8515-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8515-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8515-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8515-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8515-131">INPUTS</span></span>

### <span data-ttu-id="d8515-132">Microsoft. Azure. Commands. Security. MODELES. ceny. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="d8515-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="d8515-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8515-133">OUTPUTS</span></span>

### <span data-ttu-id="d8515-134">Microsoft. Azure. Commands. Security. MODELES. ceny. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="d8515-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="d8515-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8515-135">NOTES</span></span>

## <span data-ttu-id="d8515-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8515-136">RELATED LINKS</span></span>
