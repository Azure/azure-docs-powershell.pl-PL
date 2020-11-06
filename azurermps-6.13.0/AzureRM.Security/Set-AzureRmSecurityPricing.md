---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
ms.openlocfilehash: f5b23c9221fe8d344e9220590283ab7799a0a3fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544811"
---
# <span data-ttu-id="31f7e-101">Set-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="31f7e-101">Set-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="31f7e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="31f7e-103">Ustawia Cennik dla zakresu w warstwie usługi Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="31f7e-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31f7e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31f7e-104">SYNTAX</span></span>

### <span data-ttu-id="31f7e-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="31f7e-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31f7e-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="31f7e-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String> -PricingTier <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31f7e-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="31f7e-107">InputObject</span></span>
```
Set-AzureRmSecurityPricing -InputObject <PSAddPricingInputObject> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31f7e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="31f7e-108">DESCRIPTION</span></span>
<span data-ttu-id="31f7e-109">Ustawia Cennik dla zakresu w warstwie usługi Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="31f7e-109">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="31f7e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31f7e-110">EXAMPLES</span></span>

### <span data-ttu-id="31f7e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="31f7e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="31f7e-112">Ustawia warstwę cenową usługi Azure Security Center na "standardową"</span><span class="sxs-lookup"><span data-stu-id="31f7e-112">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="31f7e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="31f7e-113">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="31f7e-114">Ustawia warstwę zasobów Centrum zabezpieczeń usługi Azure w grupie zasób "myService1"</span><span class="sxs-lookup"><span data-stu-id="31f7e-114">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="31f7e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31f7e-115">PARAMETERS</span></span>

### <span data-ttu-id="31f7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f7e-116">-DefaultProfile</span></span>
<span data-ttu-id="31f7e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31f7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31f7e-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="31f7e-118">-InputObject</span></span>
<span data-ttu-id="31f7e-119">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="31f7e-119">Input Object.</span></span>

```yaml
Type: PSAddPricingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31f7e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="31f7e-120">-Name</span></span>
<span data-ttu-id="31f7e-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="31f7e-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7e-122">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="31f7e-122">-PricingTier</span></span>
<span data-ttu-id="31f7e-123">Warstwa cenowa.</span><span class="sxs-lookup"><span data-stu-id="31f7e-123">Pricing Tier.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f7e-124">-ResourceGroupName</span></span>
<span data-ttu-id="31f7e-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="31f7e-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7e-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31f7e-126">-Confirm</span></span>
<span data-ttu-id="31f7e-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31f7e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31f7e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31f7e-128">-WhatIf</span></span>
<span data-ttu-id="31f7e-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31f7e-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31f7e-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="31f7e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31f7e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f7e-131">CommonParameters</span></span>
<span data-ttu-id="31f7e-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f7e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f7e-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31f7e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f7e-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31f7e-134">INPUTS</span></span>

### <span data-ttu-id="31f7e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="31f7e-135">System.String</span></span>
<span data-ttu-id="31f7e-136">Microsoft. Azure. Commands. Security. cmdlet. ceny. PSAddPricingInputObject</span><span class="sxs-lookup"><span data-stu-id="31f7e-136">Microsoft.Azure.Commands.Security.Cmdlets.Pricings.PSAddPricingInputObject</span></span>

## <span data-ttu-id="31f7e-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31f7e-137">OUTPUTS</span></span>

### <span data-ttu-id="31f7e-138">Microsoft. Azure. Commands. Security. MODELES. ceny. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="31f7e-138">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="31f7e-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31f7e-139">NOTES</span></span>

## <span data-ttu-id="31f7e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31f7e-140">RELATED LINKS</span></span>
