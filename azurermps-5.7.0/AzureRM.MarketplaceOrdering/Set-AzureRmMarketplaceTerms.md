---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 33662eed86e5ad7269c81694bc92cd2bf27f93cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526805"
---
# <span data-ttu-id="ca3d0-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ca3d0-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="ca3d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ca3d0-103">Zaakceptuj lub Odrzuć warunki związane z danym identyfikatorem wydawcy (wydawcy), identyfikatorem oferty (produktu) i identyfikatorem planu (Name).</span><span class="sxs-lookup"><span data-stu-id="ca3d0-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="ca3d0-104">Skorzystaj z Get-AzureRmMarketplaceTerms, aby uzyskać postanowienia umowy.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca3d0-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca3d0-105">SYNTAX</span></span>

### <span data-ttu-id="ca3d0-106">AgreementAcceptParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ca3d0-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca3d0-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca3d0-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca3d0-108">InputObjectAcceptParametrSet</span><span class="sxs-lookup"><span data-stu-id="ca3d0-108">InputObjectAcceptParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca3d0-109">InputObjectRejectParametrSet</span><span class="sxs-lookup"><span data-stu-id="ca3d0-109">InputObjectRejectParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca3d0-110">Opis</span><span class="sxs-lookup"><span data-stu-id="ca3d0-110">DESCRIPTION</span></span>
<span data-ttu-id="ca3d0-111">Polecenie cmdlet **Set-AzureRmMarketplaceTerms** zapisuje obiekt terminy dla danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (Name).</span><span class="sxs-lookup"><span data-stu-id="ca3d0-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="ca3d0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca3d0-112">EXAMPLES</span></span>

### <span data-ttu-id="ca3d0-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca3d0-113">Example 1</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

### <span data-ttu-id="ca3d0-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ca3d0-114">Example 2</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

## <span data-ttu-id="ca3d0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca3d0-115">PARAMETERS</span></span>

### <span data-ttu-id="ca3d0-116">-Accept</span><span class="sxs-lookup"><span data-stu-id="ca3d0-116">-Accept</span></span>
<span data-ttu-id="ca3d0-117">Przekaż to, aby zaakceptować postanowienia prawne.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-117">Pass this to accept the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca3d0-118">-DefaultProfile</span></span>
<span data-ttu-id="ca3d0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca3d0-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ca3d0-120">-InputObject</span></span>
<span data-ttu-id="ca3d0-121">Obiekt terms zwrócony w Get-AzureRmMarketplaceTerms polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-121">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="ca3d0-122">Jest to parametr obowiązkowy, jeśli argument akceptowany ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-122">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d0-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca3d0-123">-Name</span></span>
<span data-ttu-id="ca3d0-124">Identyfikator planu dla wdrożonego obrazu.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-124">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d0-125">-Product</span><span class="sxs-lookup"><span data-stu-id="ca3d0-125">-Product</span></span>
<span data-ttu-id="ca3d0-126">Identyfikator oferty z wdrożonym obrazem.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-126">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d0-127">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="ca3d0-127">-Publisher</span></span>
<span data-ttu-id="ca3d0-128">Ciąg identyfikatora wydawcy wdrażanego obrazu.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-128">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d0-129">-Odrzuć</span><span class="sxs-lookup"><span data-stu-id="ca3d0-129">-Reject</span></span>
<span data-ttu-id="ca3d0-130">Przekaż to, aby odrzucić postanowienia prawne.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-130">Pass this to reject the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d0-131">-Terminy</span><span class="sxs-lookup"><span data-stu-id="ca3d0-131">-Terms</span></span>
<span data-ttu-id="ca3d0-132">Obiekt terms zwrócony w Get-AzureRmMarketplaceTerms polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-132">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="ca3d0-133">Jest to parametr obowiązkowy, jeśli argument akceptowany ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-133">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d0-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca3d0-134">-Confirm</span></span>
<span data-ttu-id="ca3d0-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca3d0-136">-WhatIf</span></span>
<span data-ttu-id="ca3d0-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca3d0-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca3d0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca3d0-139">CommonParameters</span></span>
<span data-ttu-id="ca3d0-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca3d0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca3d0-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca3d0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca3d0-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca3d0-142">INPUTS</span></span>

### <span data-ttu-id="ca3d0-143">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="ca3d0-143">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="ca3d0-144">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="ca3d0-144">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="ca3d0-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca3d0-145">OUTPUTS</span></span>

### <span data-ttu-id="ca3d0-146">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="ca3d0-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="ca3d0-147">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="ca3d0-147">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="ca3d0-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca3d0-148">NOTES</span></span>

## <span data-ttu-id="ca3d0-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca3d0-149">RELATED LINKS</span></span>

