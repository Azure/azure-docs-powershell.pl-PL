---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: aa93fee1aa1cf9242d87239625e1c25612498e09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708208"
---
# <span data-ttu-id="b847d-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="b847d-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="b847d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b847d-102">SYNOPSIS</span></span>
<span data-ttu-id="b847d-103">Pobiera dane warstwy cenowej dla usługi Azure Security Center dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="b847d-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="b847d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b847d-104">SYNTAX</span></span>

### <span data-ttu-id="b847d-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b847d-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b847d-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b847d-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b847d-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="b847d-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b847d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b847d-108">DESCRIPTION</span></span>
<span data-ttu-id="b847d-109">Dla warstwy cenowej usługi Azure Security Center ustalana jest dla każdego zakresu, za pomocą tego polecenia cmdlet można uzyskać skonfigurowane warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="b847d-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="b847d-110">Warstwa cenowa abonamentu obejmuje wszystkie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b847d-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="b847d-111">Warstwa cenowa grupy zasobów zastąpi warstwę cenową abonamentu.</span><span class="sxs-lookup"><span data-stu-id="b847d-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="b847d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b847d-112">EXAMPLES</span></span>

### <span data-ttu-id="b847d-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b847d-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="b847d-114">Pobiera wszystkie skonfigurowane warstwy cenowe dla subskrypcji i grup zasobów pod nimi.</span><span class="sxs-lookup"><span data-stu-id="b847d-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="b847d-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b847d-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="b847d-116">Pobiera skonfigurowaną warstwę cenową dla gorup zasobów "myService1".</span><span class="sxs-lookup"><span data-stu-id="b847d-116">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="b847d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b847d-117">PARAMETERS</span></span>

### <span data-ttu-id="b847d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b847d-118">-DefaultProfile</span></span>
<span data-ttu-id="b847d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b847d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b847d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b847d-120">-Name</span></span>
<span data-ttu-id="b847d-121">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b847d-121">Resource name.</span></span>

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

### <span data-ttu-id="b847d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b847d-122">-ResourceId</span></span>
<span data-ttu-id="b847d-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b847d-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b847d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b847d-124">CommonParameters</span></span>
<span data-ttu-id="b847d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b847d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b847d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b847d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b847d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b847d-127">INPUTS</span></span>

### <span data-ttu-id="b847d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b847d-128">System.String</span></span>

## <span data-ttu-id="b847d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b847d-129">OUTPUTS</span></span>

### <span data-ttu-id="b847d-130">Microsoft. Azure. Commands. Security. MODELES. ceny. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="b847d-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="b847d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b847d-131">NOTES</span></span>

## <span data-ttu-id="b847d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b847d-132">RELATED LINKS</span></span>