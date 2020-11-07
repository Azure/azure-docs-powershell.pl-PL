---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 730861b055259fd0aee5490de2421abe96afc10b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704876"
---
# <span data-ttu-id="a2292-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="a2292-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="a2292-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2292-102">SYNOPSIS</span></span>
<span data-ttu-id="a2292-103">Pobierz warunki umowy dla danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (Name).</span><span class="sxs-lookup"><span data-stu-id="a2292-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="a2292-104">W celu zaakceptowania warunków prawnych należy przekazać do Set-AzMarketplaceTerms obiekt warunki, który jest zwracany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="a2292-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="a2292-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2292-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2292-106">Opis</span><span class="sxs-lookup"><span data-stu-id="a2292-106">DESCRIPTION</span></span>
<span data-ttu-id="a2292-107">Polecenie cmdlet **Get-AzMarketplaceTerms** zwraca warunki dotyczące danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (nazwy).</span><span class="sxs-lookup"><span data-stu-id="a2292-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="a2292-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2292-108">EXAMPLES</span></span>

### <span data-ttu-id="a2292-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2292-109">Example 1</span></span>
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

## <span data-ttu-id="a2292-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2292-110">PARAMETERS</span></span>

### <span data-ttu-id="a2292-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2292-111">-DefaultProfile</span></span>
<span data-ttu-id="a2292-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2292-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2292-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a2292-113">-Name</span></span>
<span data-ttu-id="a2292-114">Identyfikator planu dla wdrożonego obrazu.</span><span class="sxs-lookup"><span data-stu-id="a2292-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="a2292-115">-Product</span><span class="sxs-lookup"><span data-stu-id="a2292-115">-Product</span></span>
<span data-ttu-id="a2292-116">Identyfikator oferty z wdrożonym obrazem.</span><span class="sxs-lookup"><span data-stu-id="a2292-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="a2292-117">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="a2292-117">-Publisher</span></span>
<span data-ttu-id="a2292-118">Ciąg identyfikatora wydawcy wdrażanego obrazu.</span><span class="sxs-lookup"><span data-stu-id="a2292-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="a2292-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2292-119">CommonParameters</span></span>
<span data-ttu-id="a2292-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2292-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2292-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2292-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2292-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2292-122">INPUTS</span></span>

### <span data-ttu-id="a2292-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a2292-123">None</span></span>

## <span data-ttu-id="a2292-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2292-124">OUTPUTS</span></span>

### <span data-ttu-id="a2292-125">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a2292-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="a2292-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2292-126">NOTES</span></span>

## <span data-ttu-id="a2292-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2292-127">RELATED LINKS</span></span>
