---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222479"
---
# <span data-ttu-id="a74cf-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="a74cf-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="a74cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a74cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a74cf-103">Zaakceptuj lub Odrzuć warunki związane z danym identyfikatorem wydawcy (wydawcy), identyfikatorem oferty (produktu) i identyfikatorem planu (Name).</span><span class="sxs-lookup"><span data-stu-id="a74cf-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="a74cf-104">Skorzystaj z Get-AzMarketplaceTerms, aby uzyskać postanowienia umowy.</span><span class="sxs-lookup"><span data-stu-id="a74cf-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="a74cf-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a74cf-105">SYNTAX</span></span>

### <span data-ttu-id="a74cf-106">AgreementAcceptParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a74cf-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a74cf-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a74cf-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a74cf-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="a74cf-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a74cf-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a74cf-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a74cf-110">Opis</span><span class="sxs-lookup"><span data-stu-id="a74cf-110">DESCRIPTION</span></span>
<span data-ttu-id="a74cf-111">Polecenie cmdlet **Set-AzMarketplaceTerms** zapisuje obiekt terminy dla danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (Name).</span><span class="sxs-lookup"><span data-stu-id="a74cf-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="a74cf-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a74cf-112">EXAMPLES</span></span>

### <span data-ttu-id="a74cf-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a74cf-113">Example 1</span></span>
<span data-ttu-id="a74cf-114">Uzyskiwanie umowy dotyczącej programu Publisher Marketplace</span><span class="sxs-lookup"><span data-stu-id="a74cf-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="a74cf-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a74cf-115">Example 2</span></span>
<span data-ttu-id="a74cf-116">Ustaw umowę o wydawcy na "zaakceptuj".</span><span class="sxs-lookup"><span data-stu-id="a74cf-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="a74cf-117">Pobierz wartość parametru "warunki" z polecenia cmdlet "Get-AzMarketplaceTerms"</span><span class="sxs-lookup"><span data-stu-id="a74cf-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="a74cf-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a74cf-118">PARAMETERS</span></span>

### <span data-ttu-id="a74cf-119">-Accept</span><span class="sxs-lookup"><span data-stu-id="a74cf-119">-Accept</span></span>
<span data-ttu-id="a74cf-120">Przekaż to, aby zaakceptować postanowienia prawne.</span><span class="sxs-lookup"><span data-stu-id="a74cf-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74cf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74cf-121">-DefaultProfile</span></span>
<span data-ttu-id="a74cf-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a74cf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a74cf-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a74cf-123">-InputObject</span></span>
<span data-ttu-id="a74cf-124">Obiekt terms zwrócony w Get-AzMarketplaceTerms polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a74cf-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="a74cf-125">Jest to parametr obowiązkowy, jeśli parametr zaakceptowany ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="a74cf-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a74cf-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a74cf-126">-Name</span></span>
<span data-ttu-id="a74cf-127">Identyfikator planu dla wdrożonego obrazu.</span><span class="sxs-lookup"><span data-stu-id="a74cf-127">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74cf-128">-Product</span><span class="sxs-lookup"><span data-stu-id="a74cf-128">-Product</span></span>
<span data-ttu-id="a74cf-129">Identyfikator oferty z wdrożonym obrazem.</span><span class="sxs-lookup"><span data-stu-id="a74cf-129">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74cf-130">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="a74cf-130">-Publisher</span></span>
<span data-ttu-id="a74cf-131">Ciąg identyfikatora wydawcy wdrażanego obrazu.</span><span class="sxs-lookup"><span data-stu-id="a74cf-131">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74cf-132">-Odrzuć</span><span class="sxs-lookup"><span data-stu-id="a74cf-132">-Reject</span></span>
<span data-ttu-id="a74cf-133">Przekaż to, aby odrzucić postanowienia prawne.</span><span class="sxs-lookup"><span data-stu-id="a74cf-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74cf-134">-Terminy</span><span class="sxs-lookup"><span data-stu-id="a74cf-134">-Terms</span></span>
<span data-ttu-id="a74cf-135">Obiekt terms zwrócony w Get-AzMarketplaceTerms polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a74cf-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="a74cf-136">Jest to parametr obowiązkowy, jeśli parametr zaakceptowany ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="a74cf-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74cf-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a74cf-137">-Confirm</span></span>
<span data-ttu-id="a74cf-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a74cf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a74cf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a74cf-139">-WhatIf</span></span>
<span data-ttu-id="a74cf-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a74cf-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a74cf-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a74cf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a74cf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74cf-142">CommonParameters</span></span>
<span data-ttu-id="a74cf-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a74cf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74cf-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a74cf-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74cf-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a74cf-145">INPUTS</span></span>

### <span data-ttu-id="a74cf-146">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a74cf-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="a74cf-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a74cf-147">OUTPUTS</span></span>

### <span data-ttu-id="a74cf-148">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a74cf-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="a74cf-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a74cf-149">NOTES</span></span>

## <span data-ttu-id="a74cf-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a74cf-150">RELATED LINKS</span></span>
