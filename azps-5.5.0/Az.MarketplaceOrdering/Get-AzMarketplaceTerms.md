---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: b729eb0ca1c0cc3b051600b59f260ebfb16d6b6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180259"
---
# <span data-ttu-id="98903-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="98903-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="98903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98903-102">SYNOPSIS</span></span>
<span data-ttu-id="98903-103">Uzyskaj warunki umowy dotyczące danego identyfikatora wydawcy(Publisher), identyfikatora oferty (Produkt) i identyfikatora planu (Nazwa).</span><span class="sxs-lookup"><span data-stu-id="98903-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="98903-104">Obiekt "terminy" zwrócony za pomocą tego polecenia powinien zostać przekazany Set-AzMarketplaceTerms w celu zaakceptowania postanowień prawnych.</span><span class="sxs-lookup"><span data-stu-id="98903-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="98903-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="98903-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98903-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="98903-106">DESCRIPTION</span></span>
<span data-ttu-id="98903-107">Polecenie **cmdlet Get-AzMarketplaceTerms** zwraca terminy dla danego identyfikatora wydawcy(Publisher), identyfikatora oferty(Produktu) i krotki identyfikator planu (Nazwa).</span><span class="sxs-lookup"><span data-stu-id="98903-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="98903-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="98903-108">EXAMPLES</span></span>

### <span data-ttu-id="98903-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="98903-109">Example 1</span></span>
```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="98903-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98903-110">PARAMETERS</span></span>

### <span data-ttu-id="98903-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98903-111">-DefaultProfile</span></span>
<span data-ttu-id="98903-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="98903-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98903-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="98903-113">-Name</span></span>
<span data-ttu-id="98903-114">Plan identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="98903-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="98903-115">— Produkt</span><span class="sxs-lookup"><span data-stu-id="98903-115">-Product</span></span>
<span data-ttu-id="98903-116">Zaoferuj ciąg identyfikatora obrazu wdrażany.</span><span class="sxs-lookup"><span data-stu-id="98903-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="98903-117">— Publisher</span><span class="sxs-lookup"><span data-stu-id="98903-117">-Publisher</span></span>
<span data-ttu-id="98903-118">Wdrożony ciąg identyfikatora wydawcy obrazu.</span><span class="sxs-lookup"><span data-stu-id="98903-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="98903-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98903-119">CommonParameters</span></span>
<span data-ttu-id="98903-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98903-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98903-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98903-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98903-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98903-122">INPUTS</span></span>

### <span data-ttu-id="98903-123">Brak</span><span class="sxs-lookup"><span data-stu-id="98903-123">None</span></span>

## <span data-ttu-id="98903-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98903-124">OUTPUTS</span></span>

### <span data-ttu-id="98903-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="98903-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="98903-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="98903-126">NOTES</span></span>

## <span data-ttu-id="98903-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98903-127">RELATED LINKS</span></span>
