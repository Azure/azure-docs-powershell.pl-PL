---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 59d1c7fa5d546652d8976dc42739c2e483164999
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335170"
---
# <span data-ttu-id="0daee-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="0daee-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="0daee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0daee-102">SYNOPSIS</span></span>

<span data-ttu-id="0daee-103">Pobiera plany usługi Azure Defender dla subskrypcji w centrum zabezpieczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0daee-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="0daee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0daee-104">SYNTAX</span></span>

### <span data-ttu-id="0daee-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0daee-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0daee-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="0daee-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0daee-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="0daee-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0daee-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0daee-108">DESCRIPTION</span></span>

<span data-ttu-id="0daee-109">Za pomocą tego polecenia cmdlet możesz wyświetlić każdy plan usługi Azure Defender, na abonament.</span><span class="sxs-lookup"><span data-stu-id="0daee-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="0daee-110">Aby uzyskać szczegółowe informacje o usłudze Azure Defender i dostępnych planach, zobacz [wprowadzenie do usługi Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span><span class="sxs-lookup"><span data-stu-id="0daee-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="0daee-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0daee-111">EXAMPLES</span></span>

### <span data-ttu-id="0daee-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0daee-112">Example 1</span></span>

```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                   Name                      PricingTier    FreeTrialRemainingTime
--                                                                                                                   ----                      -----------    ----------------------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines            VirtualMachines           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/Sqlservers                 SqlServers                Standard       00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices                AppServices               Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts            StorageAccounts           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlserverVirtualMachines   SqlservervirtualMachines  Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService          KubernetesService         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry          ContainerRegistry         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults                  KeyVaults                 Free           00:00:00
```

<span data-ttu-id="0daee-113">Pobiera stan każdego planu usługi Azure Defender dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0daee-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="0daee-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0daee-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="0daee-115">Pobiera szczegóły cennika dotyczące określonego identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="0daee-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="0daee-116">Gdzie ResourceId jest jednym z identyfikatorów zwróconych przez `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="0daee-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="0daee-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0daee-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="0daee-118">Pobiera szczegóły cennika dla nazwanego planu usługi Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="0daee-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="0daee-119">Gdzie `name` jest jedna z nazw zwracanych przez `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="0daee-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="0daee-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0daee-120">PARAMETERS</span></span>

### <span data-ttu-id="0daee-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0daee-121">-DefaultProfile</span></span>

<span data-ttu-id="0daee-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0daee-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0daee-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0daee-123">-Name</span></span>

<span data-ttu-id="0daee-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0daee-124">Resource name.</span></span>

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

### <span data-ttu-id="0daee-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0daee-125">-ResourceId</span></span>

<span data-ttu-id="0daee-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0daee-126">Resource ID.</span></span>

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

### <span data-ttu-id="0daee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0daee-127">CommonParameters</span></span>

<span data-ttu-id="0daee-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0daee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0daee-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0daee-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0daee-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0daee-130">INPUTS</span></span>

### <span data-ttu-id="0daee-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0daee-131">System.String</span></span>

## <span data-ttu-id="0daee-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0daee-132">OUTPUTS</span></span>

### <span data-ttu-id="0daee-133">Microsoft. Azure. Commands. Security. MODELES. ceny. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="0daee-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="0daee-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0daee-134">NOTES</span></span>

## <span data-ttu-id="0daee-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0daee-135">RELATED LINKS</span></span>
