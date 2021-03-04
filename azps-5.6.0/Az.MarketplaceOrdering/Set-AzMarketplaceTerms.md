---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: b4098481db78bf045abad04aee4e2e5076f71ce1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952330"
---
# <span data-ttu-id="69857-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="69857-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="69857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69857-102">SYNOPSIS</span></span>
<span data-ttu-id="69857-103">Akceptowanie lub odrzucanie warunków dla danego identyfikatora wydawcy(Publisher), identyfikatora oferty (Produkt) i identyfikatora planu(Nazwa).</span><span class="sxs-lookup"><span data-stu-id="69857-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="69857-104">Skorzystaj z Get-AzMarketplaceTerms, aby uzyskać warunki umowy.</span><span class="sxs-lookup"><span data-stu-id="69857-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="69857-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69857-105">SYNTAX</span></span>

### <span data-ttu-id="69857-106">AgreementAcceptParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="69857-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69857-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69857-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69857-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="69857-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69857-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69857-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69857-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="69857-110">DESCRIPTION</span></span>
<span data-ttu-id="69857-111">Polecenie **cmdlet Set-AzMarketplaceTerms** zapisuje obiekt terms dla podanego identyfikatora wydawcy(Publisher), identyfikatora oferty(produktu) i krotki identyfikator planu (Nazwa).</span><span class="sxs-lookup"><span data-stu-id="69857-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="69857-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69857-112">EXAMPLES</span></span>

### <span data-ttu-id="69857-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69857-113">Example 1</span></span>
<span data-ttu-id="69857-114">Uzyskiwanie umowy wydawcy w witrynie Marketplace</span><span class="sxs-lookup"><span data-stu-id="69857-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="69857-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="69857-115">Example 2</span></span>
<span data-ttu-id="69857-116">Ustaw umowę wydawcy na "Zaakceptuj".</span><span class="sxs-lookup"><span data-stu-id="69857-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="69857-117">Uzyskiwanie wartości parametru "Terms" z polecenia cmdlet "Get-AzMarketplaceTerms"</span><span class="sxs-lookup"><span data-stu-id="69857-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="69857-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69857-118">PARAMETERS</span></span>

### <span data-ttu-id="69857-119">— Zaakceptuj</span><span class="sxs-lookup"><span data-stu-id="69857-119">-Accept</span></span>
<span data-ttu-id="69857-120">Zaakceptuj to, aby zaakceptować postanowienia prawne.</span><span class="sxs-lookup"><span data-stu-id="69857-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="69857-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69857-121">-DefaultProfile</span></span>
<span data-ttu-id="69857-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69857-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69857-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69857-123">-InputObject</span></span>
<span data-ttu-id="69857-124">Obiekt Terms zwrócony w Get-AzMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69857-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="69857-125">Jest to parametr obowiązkowy, jeśli parametr Accepted ma wartość True (Zaakceptowany parametr).</span><span class="sxs-lookup"><span data-stu-id="69857-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="69857-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="69857-126">-Name</span></span>
<span data-ttu-id="69857-127">Plan identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="69857-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="69857-128">— Produkt</span><span class="sxs-lookup"><span data-stu-id="69857-128">-Product</span></span>
<span data-ttu-id="69857-129">Zaoferuj ciąg identyfikatora obrazu wdrażany.</span><span class="sxs-lookup"><span data-stu-id="69857-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="69857-130">— Publisher</span><span class="sxs-lookup"><span data-stu-id="69857-130">-Publisher</span></span>
<span data-ttu-id="69857-131">Wdrożony ciąg identyfikatora wydawcy obrazu.</span><span class="sxs-lookup"><span data-stu-id="69857-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="69857-132">— Odrzuć</span><span class="sxs-lookup"><span data-stu-id="69857-132">-Reject</span></span>
<span data-ttu-id="69857-133">Przejmij to, aby odrzucić postanowienia prawne.</span><span class="sxs-lookup"><span data-stu-id="69857-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="69857-134">—Warunki</span><span class="sxs-lookup"><span data-stu-id="69857-134">-Terms</span></span>
<span data-ttu-id="69857-135">Obiekt Terms zwrócony w Get-AzMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69857-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="69857-136">Jest to parametr obowiązkowy, jeśli parametr Accepted ma wartość True (Zaakceptowany parametr).</span><span class="sxs-lookup"><span data-stu-id="69857-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="69857-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69857-137">-Confirm</span></span>
<span data-ttu-id="69857-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="69857-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69857-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69857-139">-WhatIf</span></span>
<span data-ttu-id="69857-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69857-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69857-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="69857-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69857-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69857-142">CommonParameters</span></span>
<span data-ttu-id="69857-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69857-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69857-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69857-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69857-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69857-145">INPUTS</span></span>

### <span data-ttu-id="69857-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="69857-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="69857-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69857-147">OUTPUTS</span></span>

### <span data-ttu-id="69857-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="69857-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="69857-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69857-149">NOTES</span></span>

## <span data-ttu-id="69857-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69857-150">RELATED LINKS</span></span>
