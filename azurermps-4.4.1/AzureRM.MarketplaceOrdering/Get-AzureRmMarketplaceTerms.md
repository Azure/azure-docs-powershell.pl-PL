---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 29f3d645791dfa0b4f70ed936ccfcb4f72671038
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553836"
---
# <span data-ttu-id="4af47-101">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="4af47-101">Get-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="4af47-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4af47-102">SYNOPSIS</span></span>
<span data-ttu-id="4af47-103">Pobierz warunki umowy dla danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (Name).</span><span class="sxs-lookup"><span data-stu-id="4af47-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="4af47-104">W celu zaakceptowania warunków prawnych należy przekazać do Set-AzureRmMarketplaceTerms obiekt warunki, który jest zwracany przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="4af47-104">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4af47-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4af47-105">SYNTAX</span></span>

```
Get-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4af47-106">Opis</span><span class="sxs-lookup"><span data-stu-id="4af47-106">DESCRIPTION</span></span>
<span data-ttu-id="4af47-107">Polecenie cmdlet **Get-AzureRmMarketplaceTerms** zwraca warunki dotyczące danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (nazwy).</span><span class="sxs-lookup"><span data-stu-id="4af47-107">The **Get-AzureRmMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="4af47-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4af47-108">EXAMPLES</span></span>

### <span data-ttu-id="4af47-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4af47-109">Example 1</span></span>
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

## <span data-ttu-id="4af47-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4af47-110">PARAMETERS</span></span>

### <span data-ttu-id="4af47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af47-111">-DefaultProfile</span></span>
<span data-ttu-id="4af47-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4af47-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4af47-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4af47-113">-Name</span></span>
<span data-ttu-id="4af47-114">Identyfikator planu dla wdrożonego obrazu.</span><span class="sxs-lookup"><span data-stu-id="4af47-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="4af47-115">-Product</span><span class="sxs-lookup"><span data-stu-id="4af47-115">-Product</span></span>
<span data-ttu-id="4af47-116">Identyfikator oferty z wdrożonym obrazem.</span><span class="sxs-lookup"><span data-stu-id="4af47-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="4af47-117">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="4af47-117">-Publisher</span></span>
<span data-ttu-id="4af47-118">Ciąg identyfikatora wydawcy wdrażanego obrazu.</span><span class="sxs-lookup"><span data-stu-id="4af47-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="4af47-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af47-119">CommonParameters</span></span>
<span data-ttu-id="4af47-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4af47-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af47-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4af47-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af47-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4af47-122">INPUTS</span></span>

### <span data-ttu-id="4af47-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4af47-123">None</span></span>

## <span data-ttu-id="4af47-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4af47-124">OUTPUTS</span></span>

### <span data-ttu-id="4af47-125">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="4af47-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="4af47-126">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="4af47-126">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="4af47-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4af47-127">NOTES</span></span>

## <span data-ttu-id="4af47-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4af47-128">RELATED LINKS</span></span>

