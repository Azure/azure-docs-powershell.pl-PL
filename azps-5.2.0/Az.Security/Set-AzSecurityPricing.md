---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: 96f5a9d4791dc2668e4ec82abc140f17cbce7c44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355162"
---
# <span data-ttu-id="bb3da-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="bb3da-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="bb3da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb3da-102">SYNOPSIS</span></span>

<span data-ttu-id="bb3da-103">Włącza lub wyłącza plany usługi Azure Defender dla subskrypcji w usłudze Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="bb3da-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="bb3da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb3da-104">SYNTAX</span></span>

### <span data-ttu-id="bb3da-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bb3da-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb3da-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb3da-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb3da-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bb3da-107">DESCRIPTION</span></span>

<span data-ttu-id="bb3da-108">Włączanie lub wyłączanie dowolnego planu usługi Azure Defender dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bb3da-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="bb3da-109">Aby uzyskać szczegółowe informacje o usłudze Azure Defender i dostępnych planach, zobacz [wprowadzenie do usługi Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span><span class="sxs-lookup"><span data-stu-id="bb3da-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="bb3da-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb3da-110">EXAMPLES</span></span>

### <span data-ttu-id="bb3da-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb3da-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="bb3da-112">Włącza **usługę Azure Defender dla serwerów** subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bb3da-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="bb3da-113">"Standard" oznacza stan "włączone" dla planu usługi Azure Defender, jak pokazano w obszarze cenniki i ustawienia usługi Azure Security Center w portalu Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3da-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="bb3da-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb3da-114">PARAMETERS</span></span>

### <span data-ttu-id="bb3da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb3da-115">-DefaultProfile</span></span>

<span data-ttu-id="bb3da-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3da-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb3da-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb3da-117">-InputObject</span></span>

<span data-ttu-id="bb3da-118">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="bb3da-118">Input Object.</span></span>

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

### <span data-ttu-id="bb3da-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bb3da-119">-Name</span></span>

<span data-ttu-id="bb3da-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="bb3da-120">Resource name.</span></span>

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

### <span data-ttu-id="bb3da-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="bb3da-121">-PricingTier</span></span>

<span data-ttu-id="bb3da-122">Warstwa cenowa.</span><span class="sxs-lookup"><span data-stu-id="bb3da-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="bb3da-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb3da-123">-Confirm</span></span>

<span data-ttu-id="bb3da-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb3da-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb3da-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb3da-125">-WhatIf</span></span>

<span data-ttu-id="bb3da-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb3da-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb3da-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bb3da-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb3da-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb3da-128">CommonParameters</span></span>

<span data-ttu-id="bb3da-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb3da-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb3da-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb3da-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb3da-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb3da-131">INPUTS</span></span>

### <span data-ttu-id="bb3da-132">Microsoft. Azure. Commands. Security. MODELES. ceny. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="bb3da-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="bb3da-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb3da-133">OUTPUTS</span></span>

### <span data-ttu-id="bb3da-134">Microsoft. Azure. Commands. Security. MODELES. ceny. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="bb3da-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="bb3da-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb3da-135">NOTES</span></span>

## <span data-ttu-id="bb3da-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb3da-136">RELATED LINKS</span></span>
