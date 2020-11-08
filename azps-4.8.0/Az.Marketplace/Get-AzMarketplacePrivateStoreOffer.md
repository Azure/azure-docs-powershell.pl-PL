---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064422"
---
# <span data-ttu-id="8b8f7-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="8b8f7-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="8b8f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b8f7-102">SYNOPSIS</span></span>
<span data-ttu-id="8b8f7-103">Uzyskaj jeden lub więcej oferty prywatnego sklepu.</span><span class="sxs-lookup"><span data-stu-id="8b8f7-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="8b8f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b8f7-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b8f7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8b8f7-105">DESCRIPTION</span></span>
<span data-ttu-id="8b8f7-106">Uzyskaj jeden lub więcej oferty prywatnego sklepu za pomocą planów publicznych + prywatnych, które zostały dodane w ramach zakresu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="8b8f7-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="8b8f7-107">Jeśli jest wyświetlany identyfikator subskrypcji, uzyskaj jeden lub więcej ofert w magazynie prywatnym z planami prywatnymi tylko w zakresie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="8b8f7-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="8b8f7-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b8f7-108">EXAMPLES</span></span>

### <span data-ttu-id="8b8f7-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b8f7-109">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional ,azure_managedservices_professional-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="8b8f7-110">Pobierz oferty sklepu prywatnego za pomocą prywatnego i publicznego planu, które zostały dodane w ramach zakresu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="8b8f7-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="8b8f7-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8b8f7-111">Example 2</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="8b8f7-112">Pobierz oferty sklepu prywatnego za pomocą planów prywatnych tylko, które zostały dodane w ramach zakresu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8b8f7-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="8b8f7-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8b8f7-113">Example 3</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="8b8f7-114">Pobierz ofertę magazynu prywatnego za pomocą prywatnego i publicznego planu, które zostały dodane w ramach zakresu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="8b8f7-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="8b8f7-115">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="8b8f7-115">Example 4</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="8b8f7-116">Pobierz ofertę Sklepu prywatnego za pomocą planów prywatnych tylko, które zostały dodane w ramach zakresu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="8b8f7-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="8b8f7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b8f7-117">PARAMETERS</span></span>

### <span data-ttu-id="8b8f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b8f7-118">-DefaultProfile</span></span>
<span data-ttu-id="8b8f7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b8f7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b8f7-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="8b8f7-120">-OfferId</span></span>
<span data-ttu-id="8b8f7-121">Wymagana oferta usługi Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="8b8f7-121">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b8f7-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="8b8f7-122">-PrivateStoreId</span></span>
<span data-ttu-id="8b8f7-123">Wymagane oferty usługi Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="8b8f7-123">Required Azure Marketplace privateStore offers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b8f7-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8b8f7-124">-SubscriptionId</span></span>
<span data-ttu-id="8b8f7-125">Identyfikator subskrypcji usługi Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="8b8f7-125">Azure Marketplace subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b8f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b8f7-126">CommonParameters</span></span>
<span data-ttu-id="8b8f7-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b8f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b8f7-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b8f7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b8f7-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b8f7-129">INPUTS</span></span>

### <span data-ttu-id="8b8f7-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8b8f7-130">None</span></span>

## <span data-ttu-id="8b8f7-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b8f7-131">OUTPUTS</span></span>

### <span data-ttu-id="8b8f7-132">Microsoft. Azure. Commands. Marketplace. modele. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="8b8f7-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="8b8f7-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b8f7-133">NOTES</span></span>

## <span data-ttu-id="8b8f7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b8f7-134">RELATED LINKS</span></span>
