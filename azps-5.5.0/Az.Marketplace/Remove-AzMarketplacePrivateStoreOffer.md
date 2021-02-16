---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187419"
---
# <span data-ttu-id="53c88-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="53c88-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="53c88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53c88-102">SYNOPSIS</span></span>
<span data-ttu-id="53c88-103">Usuń ofertę ze sklepu prywatnego.</span><span class="sxs-lookup"><span data-stu-id="53c88-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="53c88-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="53c88-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53c88-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="53c88-105">DESCRIPTION</span></span>
<span data-ttu-id="53c88-106">Usuń ofertę ze sklepu prywatnego, który został utworzony w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="53c88-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="53c88-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="53c88-107">EXAMPLES</span></span>

### <span data-ttu-id="53c88-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="53c88-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="53c88-109">Usuń ofertę ze sklepu prywatnego, który został utworzony w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="53c88-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="53c88-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53c88-110">PARAMETERS</span></span>

### <span data-ttu-id="53c88-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c88-111">-DefaultProfile</span></span>
<span data-ttu-id="53c88-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="53c88-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53c88-113">- OfferId</span><span class="sxs-lookup"><span data-stu-id="53c88-113">-OfferId</span></span>
<span data-ttu-id="53c88-114">Wymagana oferta z witryny Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="53c88-114">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c88-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53c88-115">-PassThru</span></span>
<span data-ttu-id="53c88-116">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="53c88-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="53c88-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="53c88-117">-PrivateStoreId</span></span>
<span data-ttu-id="53c88-118">Wymagana prywatna usługa Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="53c88-118">Required Azure Marketplace privateStore</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c88-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53c88-119">-Confirm</span></span>
<span data-ttu-id="53c88-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="53c88-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c88-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c88-121">-WhatIf</span></span>
<span data-ttu-id="53c88-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53c88-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c88-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="53c88-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c88-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c88-124">CommonParameters</span></span>
<span data-ttu-id="53c88-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c88-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c88-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53c88-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c88-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53c88-127">INPUTS</span></span>

### <span data-ttu-id="53c88-128">Brak</span><span class="sxs-lookup"><span data-stu-id="53c88-128">None</span></span>

## <span data-ttu-id="53c88-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53c88-129">OUTPUTS</span></span>

### <span data-ttu-id="53c88-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="53c88-130">System.Boolean</span></span>

## <span data-ttu-id="53c88-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="53c88-131">NOTES</span></span>

## <span data-ttu-id="53c88-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53c88-132">RELATED LINKS</span></span>
