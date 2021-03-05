---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: 6bf0b5a25772d430695737d70ff68cae5c5aa0d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013994"
---
# <span data-ttu-id="d7dda-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="d7dda-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="d7dda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7dda-102">SYNOPSIS</span></span>
<span data-ttu-id="d7dda-103">Uzyskaj sekcje faktur.</span><span class="sxs-lookup"><span data-stu-id="d7dda-103">Get invoice sections.</span></span>

## <span data-ttu-id="d7dda-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7dda-104">SYNTAX</span></span>

### <span data-ttu-id="d7dda-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d7dda-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7dda-106">Single</span><span class="sxs-lookup"><span data-stu-id="d7dda-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7dda-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7dda-107">DESCRIPTION</span></span>
<span data-ttu-id="d7dda-108">Polecenie **cmdlet Get-AzInvoiceSection** pobiera sekcje faktur w określonym profilu rozliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="d7dda-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="d7dda-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7dda-109">EXAMPLES</span></span>

### <span data-ttu-id="d7dda-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d7dda-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="d7dda-111">Uzyskaj wszystkie sekcje faktur w określonym profilu rozliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="d7dda-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="d7dda-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d7dda-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="d7dda-113">Uzyskaj sekcję z fakturą o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="d7dda-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="d7dda-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7dda-114">PARAMETERS</span></span>

### <span data-ttu-id="d7dda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7dda-115">-DefaultProfile</span></span>
<span data-ttu-id="d7dda-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d7dda-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7dda-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="d7dda-117">-BillingAccountName</span></span>
<span data-ttu-id="d7dda-118">Nazwa konkretnego konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="d7dda-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="d7dda-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="d7dda-119">-BillingProfileName</span></span>
<span data-ttu-id="d7dda-120">Nazwa konkretnego profilu rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="d7dda-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="d7dda-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d7dda-121">-Name</span></span>
<span data-ttu-id="d7dda-122">Nazwa sekcji określonej faktury.</span><span class="sxs-lookup"><span data-stu-id="d7dda-122">Name of a specific invoice section.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dda-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7dda-123">CommonParameters</span></span>
<span data-ttu-id="d7dda-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7dda-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7dda-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7dda-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7dda-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7dda-126">INPUTS</span></span>

### <span data-ttu-id="d7dda-127">Brak</span><span class="sxs-lookup"><span data-stu-id="d7dda-127">None</span></span>

## <span data-ttu-id="d7dda-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7dda-128">OUTPUTS</span></span>

### <span data-ttu-id="d7dda-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="d7dda-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="d7dda-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7dda-130">NOTES</span></span>

## <span data-ttu-id="d7dda-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7dda-131">RELATED LINKS</span></span>
