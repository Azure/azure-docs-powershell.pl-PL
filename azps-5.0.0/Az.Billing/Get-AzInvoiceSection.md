---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232887"
---
# <span data-ttu-id="25751-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="25751-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="25751-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25751-102">SYNOPSIS</span></span>
<span data-ttu-id="25751-103">Pobierz sekcje faktury.</span><span class="sxs-lookup"><span data-stu-id="25751-103">Get invoice sections.</span></span>

## <span data-ttu-id="25751-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25751-104">SYNTAX</span></span>

### <span data-ttu-id="25751-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="25751-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25751-106">Jedn</span><span class="sxs-lookup"><span data-stu-id="25751-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25751-107">Opis</span><span class="sxs-lookup"><span data-stu-id="25751-107">DESCRIPTION</span></span>
<span data-ttu-id="25751-108">Polecenie cmdlet **Get-AzInvoiceSection** pobiera sekcje faktury w obszarze określonego profilu rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="25751-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="25751-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25751-109">EXAMPLES</span></span>

### <span data-ttu-id="25751-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25751-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="25751-111">Pobierz wszystkie sekcje faktury w obszarze określonego profilu rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="25751-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="25751-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="25751-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="25751-113">Pobierz sekcję faktury o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="25751-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="25751-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25751-114">PARAMETERS</span></span>

### <span data-ttu-id="25751-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25751-115">-DefaultProfile</span></span>
<span data-ttu-id="25751-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="25751-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25751-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="25751-117">-BillingAccountName</span></span>
<span data-ttu-id="25751-118">Nazwa określonego konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="25751-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="25751-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="25751-119">-BillingProfileName</span></span>
<span data-ttu-id="25751-120">Nazwa określonego profilu rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="25751-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="25751-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25751-121">-Name</span></span>
<span data-ttu-id="25751-122">Nazwa konkretnej sekcji faktury.</span><span class="sxs-lookup"><span data-stu-id="25751-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="25751-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25751-123">CommonParameters</span></span>
<span data-ttu-id="25751-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25751-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25751-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25751-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25751-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25751-126">INPUTS</span></span>

### <span data-ttu-id="25751-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="25751-127">None</span></span>

## <span data-ttu-id="25751-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25751-128">OUTPUTS</span></span>

### <span data-ttu-id="25751-129">Microsoft. Azure. Commands. rozliczenia. modele. PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="25751-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="25751-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25751-130">NOTES</span></span>

## <span data-ttu-id="25751-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25751-131">RELATED LINKS</span></span>
