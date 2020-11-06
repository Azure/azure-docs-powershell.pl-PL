---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
ms.openlocfilehash: 27d27cf3df8c41eaa507d9223c73f2b36637a04c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526041"
---
# <span data-ttu-id="841fa-101">Get-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="841fa-101">Get-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="841fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="841fa-102">SYNOPSIS</span></span>
<span data-ttu-id="841fa-103">Pobiera dane warstwy cenowej dla usługi Azure Security Center dla zakresu.</span><span class="sxs-lookup"><span data-stu-id="841fa-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="841fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="841fa-104">SYNTAX</span></span>

### <span data-ttu-id="841fa-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="841fa-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="841fa-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="841fa-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="841fa-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="841fa-107">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="841fa-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="841fa-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="841fa-109">Zasobów</span><span class="sxs-lookup"><span data-stu-id="841fa-109">ResourceId</span></span>
```
Get-AzureRmSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="841fa-110">Opis</span><span class="sxs-lookup"><span data-stu-id="841fa-110">DESCRIPTION</span></span>
<span data-ttu-id="841fa-111">Dla warstwy cenowej usługi Azure Security Center ustalana jest dla każdego zakresu, za pomocą tego polecenia cmdlet można uzyskać skonfigurowane warstwy cenowe.</span><span class="sxs-lookup"><span data-stu-id="841fa-111">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="841fa-112">Warstwa cenowa abonamentu obejmuje wszystkie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="841fa-112">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="841fa-113">Warstwa cenowa grupy zasobów zastąpi warstwę cenową abonamentu.</span><span class="sxs-lookup"><span data-stu-id="841fa-113">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="841fa-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="841fa-114">EXAMPLES</span></span>

### <span data-ttu-id="841fa-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="841fa-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="841fa-116">Pobiera wszystkie skonfigurowane warstwy cenowe dla subskrypcji i grup zasobów pod nimi.</span><span class="sxs-lookup"><span data-stu-id="841fa-116">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="841fa-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="841fa-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="841fa-118">Pobiera skonfigurowaną warstwę cenową dla gorup zasobów "myService1".</span><span class="sxs-lookup"><span data-stu-id="841fa-118">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="841fa-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="841fa-119">PARAMETERS</span></span>

### <span data-ttu-id="841fa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="841fa-120">-DefaultProfile</span></span>
<span data-ttu-id="841fa-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="841fa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="841fa-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="841fa-122">-Name</span></span>
<span data-ttu-id="841fa-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="841fa-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="841fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="841fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="841fa-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="841fa-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="841fa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="841fa-126">-ResourceId</span></span>
<span data-ttu-id="841fa-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="841fa-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="841fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="841fa-128">CommonParameters</span></span>
<span data-ttu-id="841fa-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="841fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="841fa-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="841fa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="841fa-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="841fa-131">INPUTS</span></span>

### <span data-ttu-id="841fa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="841fa-132">System.String</span></span>

## <span data-ttu-id="841fa-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="841fa-133">OUTPUTS</span></span>

### <span data-ttu-id="841fa-134">Microsoft. Azure. Commands. Security. MODELES. ceny. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="841fa-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="841fa-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="841fa-135">NOTES</span></span>

## <span data-ttu-id="841fa-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="841fa-136">RELATED LINKS</span></span>
