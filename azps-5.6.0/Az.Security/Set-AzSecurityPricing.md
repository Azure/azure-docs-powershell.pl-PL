---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: f55c42178daacdbf2be80982fb151514372d2d3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986497"
---
# <span data-ttu-id="72ba4-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="72ba4-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="72ba4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72ba4-102">SYNOPSIS</span></span>

<span data-ttu-id="72ba4-103">Włączenie lub wyłączenie planów usługi Azure Defender dla subskrypcji w Centrum zabezpieczeń Azure.</span><span class="sxs-lookup"><span data-stu-id="72ba4-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="72ba4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="72ba4-104">SYNTAX</span></span>

### <span data-ttu-id="72ba4-105">SubscriptionLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="72ba4-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72ba4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="72ba4-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72ba4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="72ba4-107">DESCRIPTION</span></span>

<span data-ttu-id="72ba4-108">Włącz lub wyłącz dowolne plany usługi Azure Defender dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="72ba4-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="72ba4-109">Aby uzyskać szczegółowe informacje o usłudze Azure Defender i dostępnych planach, [zobacz wprowadzenie do usługi Azure Defender.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="72ba4-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="72ba4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="72ba4-110">EXAMPLES</span></span>

### <span data-ttu-id="72ba4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="72ba4-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="72ba4-112">Włącza **usługę Azure Defender dla serwerów** dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="72ba4-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="72ba4-113">"Standardowy" oznacza stan "Wł" dla planu usługi Azure Defender, jak pokazano w obszarze cen i ustawień Centrum zabezpieczeń Azure w Portalu Azure.</span><span class="sxs-lookup"><span data-stu-id="72ba4-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="72ba4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72ba4-114">PARAMETERS</span></span>

### <span data-ttu-id="72ba4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ba4-115">-DefaultProfile</span></span>

<span data-ttu-id="72ba4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="72ba4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72ba4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72ba4-117">-InputObject</span></span>

<span data-ttu-id="72ba4-118">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="72ba4-118">Input Object.</span></span>

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

### <span data-ttu-id="72ba4-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="72ba4-119">-Name</span></span>

<span data-ttu-id="72ba4-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="72ba4-120">Resource name.</span></span>

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

### <span data-ttu-id="72ba4-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="72ba4-121">-PricingTier</span></span>

<span data-ttu-id="72ba4-122">Warstwa cenowa.</span><span class="sxs-lookup"><span data-stu-id="72ba4-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="72ba4-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72ba4-123">-Confirm</span></span>

<span data-ttu-id="72ba4-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72ba4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72ba4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ba4-125">-WhatIf</span></span>

<span data-ttu-id="72ba4-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72ba4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72ba4-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="72ba4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72ba4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ba4-128">CommonParameters</span></span>

<span data-ttu-id="72ba4-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ba4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ba4-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72ba4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ba4-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72ba4-131">INPUTS</span></span>

### <span data-ttu-id="72ba4-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="72ba4-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="72ba4-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72ba4-133">OUTPUTS</span></span>

### <span data-ttu-id="72ba4-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="72ba4-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="72ba4-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="72ba4-135">NOTES</span></span>

## <span data-ttu-id="72ba4-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72ba4-136">RELATED LINKS</span></span>
