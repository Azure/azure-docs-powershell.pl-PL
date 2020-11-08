---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233106"
---
# <span data-ttu-id="70498-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="70498-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="70498-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70498-102">SYNOPSIS</span></span>
<span data-ttu-id="70498-103">Usuwanie oferty ze sklepu prywatnego.</span><span class="sxs-lookup"><span data-stu-id="70498-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="70498-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70498-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70498-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70498-105">DESCRIPTION</span></span>
<span data-ttu-id="70498-106">Usuń ofertę ze sklepu prywatnego, która została utworzona w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="70498-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="70498-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70498-107">EXAMPLES</span></span>

### <span data-ttu-id="70498-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="70498-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="70498-109">Usuń ofertę ze sklepu prywatnego, która została utworzona w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="70498-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="70498-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70498-110">PARAMETERS</span></span>

### <span data-ttu-id="70498-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70498-111">-DefaultProfile</span></span>
<span data-ttu-id="70498-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70498-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70498-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="70498-113">-OfferId</span></span>
<span data-ttu-id="70498-114">Wymagana oferta usługi Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="70498-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="70498-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70498-115">-PassThru</span></span>
<span data-ttu-id="70498-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="70498-116">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="70498-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="70498-117">-PrivateStoreId</span></span>
<span data-ttu-id="70498-118">Wymagany privateStore Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="70498-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="70498-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70498-119">-Confirm</span></span>
<span data-ttu-id="70498-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70498-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70498-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70498-121">-WhatIf</span></span>
<span data-ttu-id="70498-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70498-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70498-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70498-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70498-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70498-124">CommonParameters</span></span>
<span data-ttu-id="70498-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70498-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70498-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70498-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70498-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70498-127">INPUTS</span></span>

### <span data-ttu-id="70498-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="70498-128">None</span></span>

## <span data-ttu-id="70498-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70498-129">OUTPUTS</span></span>

### <span data-ttu-id="70498-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70498-130">System.Boolean</span></span>

## <span data-ttu-id="70498-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70498-131">NOTES</span></span>

## <span data-ttu-id="70498-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70498-132">RELATED LINKS</span></span>
