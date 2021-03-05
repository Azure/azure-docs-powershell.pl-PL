---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 9a2f5744f5595b7be4a0a59c3181435e4f1d0eb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009617"
---
# <span data-ttu-id="910e6-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="910e6-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="910e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="910e6-102">SYNOPSIS</span></span>
<span data-ttu-id="910e6-103">Aktualizacje lub tworzenie oferty dla sklepu prywatnego.</span><span class="sxs-lookup"><span data-stu-id="910e6-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="910e6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="910e6-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="910e6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="910e6-105">DESCRIPTION</span></span>
<span data-ttu-id="910e6-106">Aktualizacje lub tworzenie oferty dla sklepu prywatnego, który został utworzony w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="910e6-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="910e6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="910e6-107">EXAMPLES</span></span>

### <span data-ttu-id="910e6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="910e6-108">Example 1</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73, PublisherEnterpriseLinux73-ARM, PublisherEnterpriseLinux73-ARM-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="910e6-109">Tworzy ofertę z planami prywatnymi + publicznymi dla sklepu prywatnego, który został utworzony w ramach zakresu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="910e6-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="910e6-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="910e6-110">Example 2</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-ARM-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="910e6-111">Tworzy ofertę z planami prywatnymi tylko dla sklepu prywatnego, który został utworzony w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="910e6-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="910e6-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="910e6-112">Example 3</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="910e6-113">Oferta aktualizacji z planami prywatnymi i publicznymi dla sklepu prywatnego, który został utworzony w ramach zakresu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="910e6-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="910e6-114">Jest wymagany tag etag.</span><span class="sxs-lookup"><span data-stu-id="910e6-114">Etag is needed.</span></span>

### <span data-ttu-id="910e6-115">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="910e6-115">Example 4</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux73-pr") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="910e6-116">Oferty aktualizacji dla sklepu prywatnego z planami prywatnymi tylko te, które zostały utworzone w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="910e6-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="910e6-117">Jest wymagany tag etag.</span><span class="sxs-lookup"><span data-stu-id="910e6-117">Etag is needed.</span></span>


## <span data-ttu-id="910e6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="910e6-118">PARAMETERS</span></span>

### <span data-ttu-id="910e6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="910e6-119">-DefaultProfile</span></span>
<span data-ttu-id="910e6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="910e6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="910e6-121">— ETag</span><span class="sxs-lookup"><span data-stu-id="910e6-121">-ETag</span></span>
<span data-ttu-id="910e6-122">Usługa Azure Marketplace privateStore oferuje tag eTag dla aktualizacji</span><span class="sxs-lookup"><span data-stu-id="910e6-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="910e6-123">- OfferId</span><span class="sxs-lookup"><span data-stu-id="910e6-123">-OfferId</span></span>
<span data-ttu-id="910e6-124">Wymagana oferta z witryny Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="910e6-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="910e6-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="910e6-125">-PrivateStoreId</span></span>
<span data-ttu-id="910e6-126">Wymagane oferty z witryny Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="910e6-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="910e6-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="910e6-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="910e6-128">Wymagane ograniczenie identyfikatorów planu wymaganego dla usługi Azure Marketplace z witryny PrivateStore</span><span class="sxs-lookup"><span data-stu-id="910e6-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="910e6-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="910e6-129">-Confirm</span></span>
<span data-ttu-id="910e6-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="910e6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="910e6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="910e6-131">-WhatIf</span></span>
<span data-ttu-id="910e6-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="910e6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="910e6-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="910e6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="910e6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="910e6-134">CommonParameters</span></span>
<span data-ttu-id="910e6-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="910e6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="910e6-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="910e6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="910e6-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="910e6-137">INPUTS</span></span>

### <span data-ttu-id="910e6-138">Brak</span><span class="sxs-lookup"><span data-stu-id="910e6-138">None</span></span>

## <span data-ttu-id="910e6-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="910e6-139">OUTPUTS</span></span>

### <span data-ttu-id="910e6-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="910e6-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="910e6-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="910e6-141">NOTES</span></span>

## <span data-ttu-id="910e6-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="910e6-142">RELATED LINKS</span></span>
