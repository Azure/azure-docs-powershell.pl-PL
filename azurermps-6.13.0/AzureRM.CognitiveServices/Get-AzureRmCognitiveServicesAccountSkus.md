---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: e1bacc62ca7efc3bd453be93196e83b0b6d67853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549408"
---
# <span data-ttu-id="3b2fa-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="3b2fa-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="3b2fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="3b2fa-103">Pobiera dostępne jednostki SKU dla konta.</span><span class="sxs-lookup"><span data-stu-id="3b2fa-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b2fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b2fa-104">SYNTAX</span></span>

### <span data-ttu-id="3b2fa-105">GetSkusWithAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3b2fa-105">GetSkusWithAccount (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b2fa-106">GetSkusWithFilter</span><span class="sxs-lookup"><span data-stu-id="3b2fa-106">GetSkusWithFilter</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b2fa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3b2fa-107">DESCRIPTION</span></span>
<span data-ttu-id="3b2fa-108">Polecenie cmdlet **Get-AzureRmCognitiveServicesAccountSkus** Pobiera dostępne jednostki SKU dla konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="3b2fa-108">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="3b2fa-109">Jednostka SKU jest planem warstw dla konta.</span><span class="sxs-lookup"><span data-stu-id="3b2fa-109">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="3b2fa-110">Definiuje cenę, limit rozmów i stawkę za konto.</span><span class="sxs-lookup"><span data-stu-id="3b2fa-110">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="3b2fa-111">F0 SKU jest bezpłatną warstwą.</span><span class="sxs-lookup"><span data-stu-id="3b2fa-111">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="3b2fa-112">Płatne warstwy obejmują S0, S1, S2 itd.</span><span class="sxs-lookup"><span data-stu-id="3b2fa-112">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="3b2fa-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b2fa-113">EXAMPLES</span></span>

### <span data-ttu-id="3b2fa-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b2fa-114">Example 1</span></span>
```powershell
PS C:\> (Get-AzureRmCognitiveServicesAccountSkus -ResourceGroupName cognitive-services-resource-group -Name myluis).Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="3b2fa-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b2fa-115">PARAMETERS</span></span>

### <span data-ttu-id="3b2fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b2fa-116">-DefaultProfile</span></span>
<span data-ttu-id="3b2fa-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3b2fa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b2fa-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3b2fa-118">-Location</span></span>
<span data-ttu-id="3b2fa-119">Lokalizacja konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="3b2fa-119">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2fa-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b2fa-120">-Name</span></span>
<span data-ttu-id="3b2fa-121">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="3b2fa-121">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b2fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="3b2fa-123">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="3b2fa-123">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2fa-124">-Type</span><span class="sxs-lookup"><span data-stu-id="3b2fa-124">-Type</span></span>
<span data-ttu-id="3b2fa-125">Typ konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="3b2fa-125">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b2fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b2fa-126">CommonParameters</span></span>
<span data-ttu-id="3b2fa-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b2fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b2fa-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b2fa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b2fa-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b2fa-129">INPUTS</span></span>

### <span data-ttu-id="3b2fa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3b2fa-130">System.String</span></span>

## <span data-ttu-id="3b2fa-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b2fa-131">OUTPUTS</span></span>

### <span data-ttu-id="3b2fa-132">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="3b2fa-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="3b2fa-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b2fa-133">NOTES</span></span>

## <span data-ttu-id="3b2fa-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b2fa-134">RELATED LINKS</span></span>
