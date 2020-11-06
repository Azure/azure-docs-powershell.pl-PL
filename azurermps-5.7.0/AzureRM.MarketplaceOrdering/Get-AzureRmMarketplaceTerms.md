---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/get-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
ms.openlocfilehash: b6f5b0ddecea600b0d3a7b23ad526b78417ae993
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526806"
---
# <span data-ttu-id="d5634-101">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="d5634-101">Get-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="d5634-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5634-102">SYNOPSIS</span></span>
<span data-ttu-id="d5634-103">Pobierz warunki umowy dla danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (Name).</span><span class="sxs-lookup"><span data-stu-id="d5634-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="d5634-104">W celu zaakceptowania warunków prawnych należy przekazać do Set-AzureRmMarketplaceTerms obiekt warunki, który jest zwracany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="d5634-104">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5634-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5634-105">SYNTAX</span></span>

```
Get-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5634-106">Opis</span><span class="sxs-lookup"><span data-stu-id="d5634-106">DESCRIPTION</span></span>
<span data-ttu-id="d5634-107">Polecenie cmdlet **Get-AzureRmMarketplaceTerms** zwraca warunki dotyczące danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (nazwy).</span><span class="sxs-lookup"><span data-stu-id="d5634-107">The **Get-AzureRmMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="d5634-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5634-108">EXAMPLES</span></span>

### <span data-ttu-id="d5634-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d5634-109">Example 1</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="d5634-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5634-110">PARAMETERS</span></span>

### <span data-ttu-id="d5634-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5634-111">-DefaultProfile</span></span>
<span data-ttu-id="d5634-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5634-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5634-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d5634-113">-Name</span></span>
<span data-ttu-id="d5634-114">Identyfikator planu dla wdrożonego obrazu.</span><span class="sxs-lookup"><span data-stu-id="d5634-114">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5634-115">-Product</span><span class="sxs-lookup"><span data-stu-id="d5634-115">-Product</span></span>
<span data-ttu-id="d5634-116">Identyfikator oferty z wdrożonym obrazem.</span><span class="sxs-lookup"><span data-stu-id="d5634-116">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5634-117">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="d5634-117">-Publisher</span></span>
<span data-ttu-id="d5634-118">Ciąg identyfikatora wydawcy wdrażanego obrazu.</span><span class="sxs-lookup"><span data-stu-id="d5634-118">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5634-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5634-119">CommonParameters</span></span>
<span data-ttu-id="d5634-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5634-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5634-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5634-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5634-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5634-122">INPUTS</span></span>

### <span data-ttu-id="d5634-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d5634-123">None</span></span>

## <span data-ttu-id="d5634-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5634-124">OUTPUTS</span></span>

### <span data-ttu-id="d5634-125">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="d5634-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="d5634-126">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="d5634-126">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="d5634-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5634-127">NOTES</span></span>

## <span data-ttu-id="d5634-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5634-128">RELATED LINKS</span></span>

