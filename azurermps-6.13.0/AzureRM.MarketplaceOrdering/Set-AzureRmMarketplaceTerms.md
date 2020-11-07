---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 7932a733fcd672d8ee92e6452765745281ee0a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716714"
---
# <span data-ttu-id="5ec37-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="5ec37-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="5ec37-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ec37-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec37-103">Zaakceptuj lub Odrzuć warunki związane z danym identyfikatorem wydawcy (wydawcy), identyfikatorem oferty (produktu) i identyfikatorem planu (Name).</span><span class="sxs-lookup"><span data-stu-id="5ec37-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="5ec37-104">Skorzystaj z Get-AzureRmMarketplaceTerms, aby uzyskać postanowienia umowy.</span><span class="sxs-lookup"><span data-stu-id="5ec37-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ec37-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ec37-105">SYNTAX</span></span>

### <span data-ttu-id="5ec37-106">AgreementAcceptParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5ec37-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ec37-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ec37-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ec37-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ec37-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ec37-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ec37-109">InputObjectRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ec37-110">Opis</span><span class="sxs-lookup"><span data-stu-id="5ec37-110">DESCRIPTION</span></span>
<span data-ttu-id="5ec37-111">Polecenie cmdlet **Set-AzureRmMarketplaceTerms** zapisuje obiekt terminy dla danego identyfikatora wydawcy (wydawcy), identyfikatora oferty (produktu) i identyfikatora planu (Name).</span><span class="sxs-lookup"><span data-stu-id="5ec37-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="5ec37-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ec37-112">EXAMPLES</span></span>

### <span data-ttu-id="5ec37-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ec37-113">Example 1</span></span>
<span data-ttu-id="5ec37-114">Uzyskiwanie umowy dotyczącej programu Publisher Marketplace</span><span class="sxs-lookup"><span data-stu-id="5ec37-114">Get the marketplace publisher agreement</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

### <span data-ttu-id="5ec37-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5ec37-115">Example 2</span></span>
<span data-ttu-id="5ec37-116">Ustaw umowę o wydawcy na "zaakceptuj".</span><span class="sxs-lookup"><span data-stu-id="5ec37-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="5ec37-117">Pobierz wartość parametru "warunki" z polecenia cmdlet "Get-AzureRmMarketplaceTerms"</span><span class="sxs-lookup"><span data-stu-id="5ec37-117">Get the value for the 'Terms' parameter from the 'Get-AzureRmMarketplaceTerms' cmdlet</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```


## <span data-ttu-id="5ec37-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ec37-118">PARAMETERS</span></span>

### <span data-ttu-id="5ec37-119">-Accept</span><span class="sxs-lookup"><span data-stu-id="5ec37-119">-Accept</span></span>
<span data-ttu-id="5ec37-120">Przekaż to, aby zaakceptować postanowienia prawne.</span><span class="sxs-lookup"><span data-stu-id="5ec37-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ec37-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec37-121">-DefaultProfile</span></span>
<span data-ttu-id="5ec37-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ec37-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ec37-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5ec37-123">-InputObject</span></span>
<span data-ttu-id="5ec37-124">Obiekt terms zwrócony w Get-AzureRmMarketplaceTerms polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ec37-124">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="5ec37-125">Jest to parametr obowiązkowy, jeśli argument akceptowany ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="5ec37-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ec37-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ec37-126">-Name</span></span>
<span data-ttu-id="5ec37-127">Identyfikator planu dla wdrożonego obrazu.</span><span class="sxs-lookup"><span data-stu-id="5ec37-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="5ec37-128">-Product</span><span class="sxs-lookup"><span data-stu-id="5ec37-128">-Product</span></span>
<span data-ttu-id="5ec37-129">Identyfikator oferty z wdrożonym obrazem.</span><span class="sxs-lookup"><span data-stu-id="5ec37-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="5ec37-130">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="5ec37-130">-Publisher</span></span>
<span data-ttu-id="5ec37-131">Ciąg identyfikatora wydawcy wdrażanego obrazu.</span><span class="sxs-lookup"><span data-stu-id="5ec37-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="5ec37-132">-Odrzuć</span><span class="sxs-lookup"><span data-stu-id="5ec37-132">-Reject</span></span>
<span data-ttu-id="5ec37-133">Przekaż to, aby odrzucić postanowienia prawne.</span><span class="sxs-lookup"><span data-stu-id="5ec37-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ec37-134">-Terminy</span><span class="sxs-lookup"><span data-stu-id="5ec37-134">-Terms</span></span>
<span data-ttu-id="5ec37-135">Obiekt terms zwrócony w Get-AzureRmMarketplaceTerms polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ec37-135">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="5ec37-136">Jest to parametr obowiązkowy, jeśli argument akceptowany ma wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="5ec37-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="5ec37-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ec37-137">-Confirm</span></span>
<span data-ttu-id="5ec37-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ec37-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ec37-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ec37-139">-WhatIf</span></span>
<span data-ttu-id="5ec37-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ec37-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ec37-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ec37-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ec37-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec37-142">CommonParameters</span></span>
<span data-ttu-id="5ec37-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ec37-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec37-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ec37-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec37-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ec37-145">INPUTS</span></span>

### <span data-ttu-id="5ec37-146">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="5ec37-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="5ec37-147">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5ec37-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5ec37-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ec37-148">OUTPUTS</span></span>

### <span data-ttu-id="5ec37-149">Microsoft. Azure. Commands. MarketplaceOrdering. models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="5ec37-149">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="5ec37-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ec37-150">NOTES</span></span>

## <span data-ttu-id="5ec37-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ec37-151">RELATED LINKS</span></span>
