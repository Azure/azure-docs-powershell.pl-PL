---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: d041d18713efa4d094a46747a9697eb76dcea578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869187"
---
# <span data-ttu-id="671ea-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="671ea-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="671ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="671ea-102">SYNOPSIS</span></span>
<span data-ttu-id="671ea-103">Pobiera dostępne jednostki SKU dla konta.</span><span class="sxs-lookup"><span data-stu-id="671ea-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="671ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="671ea-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="671ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="671ea-105">DESCRIPTION</span></span>
<span data-ttu-id="671ea-106">Polecenie cmdlet **Get-AzCognitiveServicesAccountSku** Pobiera dostępne jednostki SKU dla konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="671ea-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="671ea-107">Jednostka SKU jest planem warstw dla konta.</span><span class="sxs-lookup"><span data-stu-id="671ea-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="671ea-108">Definiuje cenę, limit rozmów i stawkę za konto.</span><span class="sxs-lookup"><span data-stu-id="671ea-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="671ea-109">F0 SKU jest bezpłatną warstwą.</span><span class="sxs-lookup"><span data-stu-id="671ea-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="671ea-110">Płatne warstwy obejmują S0, S1, S2 itd.</span><span class="sxs-lookup"><span data-stu-id="671ea-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="671ea-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="671ea-111">EXAMPLES</span></span>

### <span data-ttu-id="671ea-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="671ea-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="671ea-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="671ea-113">PARAMETERS</span></span>

### <span data-ttu-id="671ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="671ea-114">-DefaultProfile</span></span>
<span data-ttu-id="671ea-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="671ea-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="671ea-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="671ea-116">-Location</span></span>
<span data-ttu-id="671ea-117">Lokalizacja konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="671ea-117">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="671ea-118">-Type</span><span class="sxs-lookup"><span data-stu-id="671ea-118">-Type</span></span>
<span data-ttu-id="671ea-119">Typ konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="671ea-119">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="671ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="671ea-120">CommonParameters</span></span>
<span data-ttu-id="671ea-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="671ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="671ea-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="671ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="671ea-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="671ea-123">INPUTS</span></span>

### <span data-ttu-id="671ea-124">System. String</span><span class="sxs-lookup"><span data-stu-id="671ea-124">System.String</span></span>

## <span data-ttu-id="671ea-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="671ea-125">OUTPUTS</span></span>

### <span data-ttu-id="671ea-126">Microsoft. Azure. Management. CognitiveServices. MODELES. ResourceSku</span><span class="sxs-lookup"><span data-stu-id="671ea-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="671ea-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="671ea-127">NOTES</span></span>

## <span data-ttu-id="671ea-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="671ea-128">RELATED LINKS</span></span>
