---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233367"
---
# <span data-ttu-id="058e3-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="058e3-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="058e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="058e3-102">SYNOPSIS</span></span>
<span data-ttu-id="058e3-103">Aktualizuje lub tworzy ofertę w sklepie prywatnym.</span><span class="sxs-lookup"><span data-stu-id="058e3-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="058e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="058e3-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="058e3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="058e3-105">DESCRIPTION</span></span>
<span data-ttu-id="058e3-106">Umożliwia aktualizowanie lub tworzenie oferty dla prywatnego magazynu utworzonego w ramach zakresu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="058e3-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="058e3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="058e3-107">EXAMPLES</span></span>

### <span data-ttu-id="058e3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="058e3-108">Example 1</span></span>
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

<span data-ttu-id="058e3-109">Tworzenie oferty z prywatnymi i publicznymi planami dla prywatnego magazynu, które zostały utworzone w ramach zakresu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="058e3-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="058e3-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="058e3-110">Example 2</span></span>
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

<span data-ttu-id="058e3-111">Umożliwia tworzenie oferty za pomocą planów prywatnych tylko w przypadku prywatnego magazynu, który został utworzony w ramach zakresu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="058e3-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="058e3-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="058e3-112">Example 3</span></span>
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

<span data-ttu-id="058e3-113">Aktualizacje oferują prywatne i publiczne plany dla prywatnego sklepu, które zostały utworzone w ramach zakresu dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="058e3-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="058e3-114">Potrzebny jest element ETag.</span><span class="sxs-lookup"><span data-stu-id="058e3-114">Etag is needed.</span></span>

### <span data-ttu-id="058e3-115">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="058e3-115">Example 4</span></span>
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

<span data-ttu-id="058e3-116">Aktualizacje są oferowane tylko w sklepie prywatnym z planami prywatnymi, które zostały utworzone w ramach zakresu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="058e3-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="058e3-117">Potrzebny jest element ETag.</span><span class="sxs-lookup"><span data-stu-id="058e3-117">Etag is needed.</span></span>


## <span data-ttu-id="058e3-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="058e3-118">PARAMETERS</span></span>

### <span data-ttu-id="058e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="058e3-119">-DefaultProfile</span></span>
<span data-ttu-id="058e3-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="058e3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="058e3-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="058e3-121">-ETag</span></span>
<span data-ttu-id="058e3-122">Element eTag oferty usługi Azure Marketplace privateStore do aktualizacji</span><span class="sxs-lookup"><span data-stu-id="058e3-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="058e3-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="058e3-123">-OfferId</span></span>
<span data-ttu-id="058e3-124">Wymagana oferta usługi Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="058e3-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="058e3-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="058e3-125">-PrivateStoreId</span></span>
<span data-ttu-id="058e3-126">Wymagane oferty usługi Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="058e3-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="058e3-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="058e3-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="058e3-128">Wymagane ograniczenia dotyczące identyfikatorów planu dla usługi Azure Marketplace privateStore oferta</span><span class="sxs-lookup"><span data-stu-id="058e3-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

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

### <span data-ttu-id="058e3-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="058e3-129">-Confirm</span></span>
<span data-ttu-id="058e3-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="058e3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="058e3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="058e3-131">-WhatIf</span></span>
<span data-ttu-id="058e3-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="058e3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="058e3-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="058e3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="058e3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="058e3-134">CommonParameters</span></span>
<span data-ttu-id="058e3-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="058e3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="058e3-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="058e3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="058e3-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="058e3-137">INPUTS</span></span>

### <span data-ttu-id="058e3-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="058e3-138">None</span></span>

## <span data-ttu-id="058e3-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="058e3-139">OUTPUTS</span></span>

### <span data-ttu-id="058e3-140">Microsoft. Azure. Commands. Marketplace. modele. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="058e3-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="058e3-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="058e3-141">NOTES</span></span>

## <span data-ttu-id="058e3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="058e3-142">RELATED LINKS</span></span>
