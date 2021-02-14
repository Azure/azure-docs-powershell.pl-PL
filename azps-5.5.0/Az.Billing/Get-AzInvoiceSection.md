---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181987"
---
# <span data-ttu-id="84152-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="84152-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="84152-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84152-102">SYNOPSIS</span></span>
<span data-ttu-id="84152-103">Uzyskaj sekcje faktur.</span><span class="sxs-lookup"><span data-stu-id="84152-103">Get invoice sections.</span></span>

## <span data-ttu-id="84152-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="84152-104">SYNTAX</span></span>

### <span data-ttu-id="84152-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="84152-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84152-106">Single</span><span class="sxs-lookup"><span data-stu-id="84152-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84152-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="84152-107">DESCRIPTION</span></span>
<span data-ttu-id="84152-108">Polecenie **cmdlet Get-AzInvoiceSection** pobiera sekcje faktur w określonym profilu rozliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="84152-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="84152-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="84152-109">EXAMPLES</span></span>

### <span data-ttu-id="84152-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84152-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="84152-111">Uzyskaj wszystkie sekcje faktur w określonym profilu rozliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="84152-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="84152-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="84152-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="84152-113">Uzyskaj sekcję z fakturą o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="84152-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="84152-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84152-114">PARAMETERS</span></span>

### <span data-ttu-id="84152-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84152-115">-DefaultProfile</span></span>
<span data-ttu-id="84152-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="84152-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84152-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="84152-117">-BillingAccountName</span></span>
<span data-ttu-id="84152-118">Nazwa konkretnego konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="84152-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="84152-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="84152-119">-BillingProfileName</span></span>
<span data-ttu-id="84152-120">Nazwa konkretnego profilu rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="84152-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="84152-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="84152-121">-Name</span></span>
<span data-ttu-id="84152-122">Nazwa sekcji określonej faktury.</span><span class="sxs-lookup"><span data-stu-id="84152-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="84152-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84152-123">CommonParameters</span></span>
<span data-ttu-id="84152-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84152-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84152-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84152-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84152-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84152-126">INPUTS</span></span>

### <span data-ttu-id="84152-127">Brak</span><span class="sxs-lookup"><span data-stu-id="84152-127">None</span></span>

## <span data-ttu-id="84152-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84152-128">OUTPUTS</span></span>

### <span data-ttu-id="84152-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="84152-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="84152-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="84152-130">NOTES</span></span>

## <span data-ttu-id="84152-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84152-131">RELATED LINKS</span></span>
