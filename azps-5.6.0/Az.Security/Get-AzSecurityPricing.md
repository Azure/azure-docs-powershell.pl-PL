---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 588f9a057767e1e78b43664c35a61f26e6edf972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016001"
---
# <span data-ttu-id="cde83-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="cde83-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="cde83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cde83-102">SYNOPSIS</span></span>

<span data-ttu-id="cde83-103">Pobiera plany usługi Azure Defender dla subskrypcji w usłudze Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="cde83-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="cde83-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cde83-104">SYNTAX</span></span>

### <span data-ttu-id="cde83-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cde83-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cde83-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="cde83-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cde83-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cde83-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cde83-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cde83-108">DESCRIPTION</span></span>

<span data-ttu-id="cde83-109">To polecenie cmdlet umożliwia wyświetlanie poszczególnych planów usługi Azure Defender według subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cde83-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="cde83-110">Aby uzyskać szczegółowe informacje o usłudze Azure Defender i dostępnych planach, [zobacz wprowadzenie do usługi Azure Defender.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="cde83-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="cde83-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cde83-111">EXAMPLES</span></span>

### <span data-ttu-id="cde83-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cde83-112">Example 1</span></span>

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

<span data-ttu-id="cde83-113">Otrzymuje stan każdego planu usługi Azure Defender dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cde83-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="cde83-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cde83-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="cde83-115">Pobiera szczegóły cen dla określonego identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="cde83-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="cde83-116">Where ResourceId is one the ID returned by `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="cde83-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="cde83-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cde83-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="cde83-118">Pobiera szczegółowe ceny nazwanego planu usługi Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="cde83-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="cde83-119">Gdzie `name` znajduje się jedna z nazw zwróconych `Get-AzSecurityPricing` przez.</span><span class="sxs-lookup"><span data-stu-id="cde83-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="cde83-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cde83-120">PARAMETERS</span></span>

### <span data-ttu-id="cde83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde83-121">-DefaultProfile</span></span>

<span data-ttu-id="cde83-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cde83-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cde83-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cde83-123">-Name</span></span>

<span data-ttu-id="cde83-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cde83-124">Resource name.</span></span>

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

### <span data-ttu-id="cde83-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cde83-125">-ResourceId</span></span>

<span data-ttu-id="cde83-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="cde83-126">Resource ID.</span></span>

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

### <span data-ttu-id="cde83-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde83-127">CommonParameters</span></span>

<span data-ttu-id="cde83-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cde83-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde83-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cde83-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde83-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cde83-130">INPUTS</span></span>

### <span data-ttu-id="cde83-131">System.String</span><span class="sxs-lookup"><span data-stu-id="cde83-131">System.String</span></span>

## <span data-ttu-id="cde83-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cde83-132">OUTPUTS</span></span>

### <span data-ttu-id="cde83-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="cde83-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="cde83-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cde83-134">NOTES</span></span>

## <span data-ttu-id="cde83-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cde83-135">RELATED LINKS</span></span>
