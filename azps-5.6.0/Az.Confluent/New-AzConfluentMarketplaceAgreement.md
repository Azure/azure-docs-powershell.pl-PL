---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: f8c293870fa4eeb6f0df8a543473c8a9bda314c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012586"
---
# <span data-ttu-id="44b58-101">New-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="44b58-101">New-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="44b58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44b58-102">SYNOPSIS</span></span>
<span data-ttu-id="44b58-103">Zaakceptuj postanowienia dotyczące witryny marketplace.</span><span class="sxs-lookup"><span data-stu-id="44b58-103">Accept marketplace terms.</span></span>

## <span data-ttu-id="44b58-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="44b58-104">SYNTAX</span></span>

```
New-AzConfluentMarketplaceAgreement [-SubscriptionId <String>] [-Accepted] [-LicenseTextLink <String>]
 [-Plan <String>] [-PrivacyPolicyLink <String>] [-Product <String>] [-Publisher <String>]
 [-RetrieveDatetime <DateTime>] [-Signature <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="44b58-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="44b58-105">DESCRIPTION</span></span>
<span data-ttu-id="44b58-106">Zaakceptuj postanowienia dotyczące witryny marketplace.</span><span class="sxs-lookup"><span data-stu-id="44b58-106">Accept marketplace terms.</span></span>

## <span data-ttu-id="44b58-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="44b58-107">EXAMPLES</span></span>

### <span data-ttu-id="44b58-108">Przykład 1. Tworzenie umowy dotyczącej witryny Confluent Marketplace w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="44b58-108">Example 1: Create confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> New-AzConfluentMarketplaceAgreement -Accepted

Name    Type
----    ----
default Microsoft.Confluent/agreement
```

<span data-ttu-id="44b58-109">To polecenie umożliwia utworzenie umowy dotyczącej witryny Confluent Marketplace w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="44b58-109">This command create confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="44b58-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44b58-110">PARAMETERS</span></span>

### <span data-ttu-id="44b58-111">— Zaakceptowane</span><span class="sxs-lookup"><span data-stu-id="44b58-111">-Accepted</span></span>
<span data-ttu-id="44b58-112">Jeśli którakolwiek wersja warunków została zaakceptowana, w przeciwnym razie fałsz.</span><span class="sxs-lookup"><span data-stu-id="44b58-112">If any version of the terms have been accepted, otherwise false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b58-113">-DefaultProfile</span></span>
<span data-ttu-id="44b58-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="44b58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b58-115">-LicenseTextLink</span><span class="sxs-lookup"><span data-stu-id="44b58-115">-LicenseTextLink</span></span>
<span data-ttu-id="44b58-116">Link do kodu HTML przy użyciu terminów Microsoft i Publisher.</span><span class="sxs-lookup"><span data-stu-id="44b58-116">Link to HTML with Microsoft and Publisher terms.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b58-117">— planowanie</span><span class="sxs-lookup"><span data-stu-id="44b58-117">-Plan</span></span>
<span data-ttu-id="44b58-118">Ciąg identyfikatora planu.</span><span class="sxs-lookup"><span data-stu-id="44b58-118">Plan identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b58-119">-PrivacyPolicyLink</span><span class="sxs-lookup"><span data-stu-id="44b58-119">-PrivacyPolicyLink</span></span>
<span data-ttu-id="44b58-120">Link do zasad zachowania poufności informacji wydawcy.</span><span class="sxs-lookup"><span data-stu-id="44b58-120">Link to the privacy policy of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b58-121">— Produkt</span><span class="sxs-lookup"><span data-stu-id="44b58-121">-Product</span></span>
<span data-ttu-id="44b58-122">Ciąg identyfikatora produktu.</span><span class="sxs-lookup"><span data-stu-id="44b58-122">Product identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b58-123">— Publisher</span><span class="sxs-lookup"><span data-stu-id="44b58-123">-Publisher</span></span>
<span data-ttu-id="44b58-124">Ciąg identyfikatora programu Publisher.</span><span class="sxs-lookup"><span data-stu-id="44b58-124">Publisher identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b58-125">-RetrieveDatetime</span><span class="sxs-lookup"><span data-stu-id="44b58-125">-RetrieveDatetime</span></span>
<span data-ttu-id="44b58-126">Data i godzina w czasie UTC, kiedy warunki zostały zaakceptowane.</span><span class="sxs-lookup"><span data-stu-id="44b58-126">Date and time in UTC of when the terms were accepted.</span></span>
<span data-ttu-id="44b58-127">To pole jest puste, jeśli zaakceptowane ma wartość fałsz.</span><span class="sxs-lookup"><span data-stu-id="44b58-127">This is empty if Accepted is false.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b58-128">— Podpis</span><span class="sxs-lookup"><span data-stu-id="44b58-128">-Signature</span></span>
<span data-ttu-id="44b58-129">Podpis warunków.</span><span class="sxs-lookup"><span data-stu-id="44b58-129">Terms signature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b58-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44b58-130">-SubscriptionId</span></span>
<span data-ttu-id="44b58-131">Identyfikator subskrypcji platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="44b58-131">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44b58-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44b58-132">-Confirm</span></span>
<span data-ttu-id="44b58-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="44b58-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44b58-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44b58-134">-WhatIf</span></span>
<span data-ttu-id="44b58-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44b58-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44b58-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="44b58-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44b58-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b58-137">CommonParameters</span></span>
<span data-ttu-id="44b58-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44b58-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b58-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44b58-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b58-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44b58-140">INPUTS</span></span>

## <span data-ttu-id="44b58-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44b58-141">OUTPUTS</span></span>

### <span data-ttu-id="44b58-142">Microsoft.Azure.PowerShell.Cmdlet.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="44b58-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="44b58-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="44b58-143">NOTES</span></span>

<span data-ttu-id="44b58-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="44b58-144">ALIASES</span></span>

## <span data-ttu-id="44b58-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44b58-145">RELATED LINKS</span></span>

