---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: de2640d8a2044a8124fb87bed53b9ee433977716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546979"
---
# <span data-ttu-id="6fec4-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="6fec4-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="6fec4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fec4-102">SYNOPSIS</span></span>
<span data-ttu-id="6fec4-103">Pobiera dostępne jednostki SKU dla konta.</span><span class="sxs-lookup"><span data-stu-id="6fec4-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fec4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fec4-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fec4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6fec4-105">DESCRIPTION</span></span>
<span data-ttu-id="6fec4-106">Polecenie cmdlet **Get-AzureRmCognitiveServicesAccountSkus** Pobiera dostępne jednostki SKU dla konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="6fec4-106">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>

<span data-ttu-id="6fec4-107">Jednostka SKU jest planem warstw dla konta.</span><span class="sxs-lookup"><span data-stu-id="6fec4-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="6fec4-108">Definiuje cenę, limit rozmów i stawkę za konto.</span><span class="sxs-lookup"><span data-stu-id="6fec4-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="6fec4-109">F0 SKU jest bezpłatną warstwą.</span><span class="sxs-lookup"><span data-stu-id="6fec4-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="6fec4-110">Płatne warstwy obejmują S0, S1, S2 itd.</span><span class="sxs-lookup"><span data-stu-id="6fec4-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="6fec4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fec4-111">EXAMPLES</span></span>

## <span data-ttu-id="6fec4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fec4-112">PARAMETERS</span></span>

### <span data-ttu-id="6fec4-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6fec4-113">-Name</span></span>
<span data-ttu-id="6fec4-114">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="6fec4-114">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fec4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fec4-115">-ResourceGroupName</span></span>
<span data-ttu-id="6fec4-116">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="6fec4-116">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fec4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fec4-117">-DefaultProfile</span></span>
<span data-ttu-id="6fec4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fec4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fec4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fec4-119">CommonParameters</span></span>
<span data-ttu-id="6fec4-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fec4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fec4-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fec4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fec4-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fec4-122">INPUTS</span></span>

## <span data-ttu-id="6fec4-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fec4-123">OUTPUTS</span></span>

### <span data-ttu-id="6fec4-124">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="6fec4-124">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="6fec4-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fec4-125">NOTES</span></span>

## <span data-ttu-id="6fec4-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fec4-126">RELATED LINKS</span></span>

