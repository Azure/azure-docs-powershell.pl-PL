---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: c66b3a2c4c151daf0a5d3df62aaaf248a7d2e338
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986217"
---
# <span data-ttu-id="4e3a1-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="4e3a1-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="4e3a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="4e3a1-103">Uzyskaj profile rozliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="4e3a1-103">Get billing profiles.</span></span>

## <span data-ttu-id="4e3a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4e3a1-104">SYNTAX</span></span>

### <span data-ttu-id="4e3a1-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e3a1-106">Single</span><span class="sxs-lookup"><span data-stu-id="4e3a1-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e3a1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4e3a1-107">DESCRIPTION</span></span>
<span data-ttu-id="4e3a1-108">Polecenie **cmdlet Get-AzBillingProfile** pobiera profile rozliczeniowe w ramach określonego konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="4e3a1-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="4e3a1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4e3a1-109">EXAMPLES</span></span>

### <span data-ttu-id="4e3a1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="4e3a1-111">Pobierz wszystkie profile rozliczeniowe w ramach określonego konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="4e3a1-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="4e3a1-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="4e3a1-113">Pobierz profil rozliczeniowy o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="4e3a1-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="4e3a1-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4e3a1-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="4e3a1-115">Pobierz wszystkie profile rozliczeniowe pod określonym kontem rozliczeniowym i uwzględnij w wynikach sekcje faktur.</span><span class="sxs-lookup"><span data-stu-id="4e3a1-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="4e3a1-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="4e3a1-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="4e3a1-117">Uzyskaj profil rozliczeniowy z podaną nazwą i uwzględnij sekcje faktur w wynikach.</span><span class="sxs-lookup"><span data-stu-id="4e3a1-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="4e3a1-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e3a1-118">PARAMETERS</span></span>

### <span data-ttu-id="4e3a1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3a1-119">-DefaultProfile</span></span>
<span data-ttu-id="4e3a1-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4e3a1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e3a1-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="4e3a1-121">-BillingAccountName</span></span>
<span data-ttu-id="4e3a1-122">Nazwa konkretnego konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="4e3a1-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="4e3a1-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="4e3a1-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="4e3a1-124">Uwzględnij sekcje faktur w profilu rozliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="4e3a1-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="4e3a1-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4e3a1-125">-Name</span></span>
<span data-ttu-id="4e3a1-126">Nazwa konkretnego profilu rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="4e3a1-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="4e3a1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3a1-127">CommonParameters</span></span>
<span data-ttu-id="4e3a1-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e3a1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3a1-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e3a1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3a1-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e3a1-130">INPUTS</span></span>

### <span data-ttu-id="4e3a1-131">Brak</span><span class="sxs-lookup"><span data-stu-id="4e3a1-131">None</span></span>

## <span data-ttu-id="4e3a1-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e3a1-132">OUTPUTS</span></span>

### <span data-ttu-id="4e3a1-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="4e3a1-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="4e3a1-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4e3a1-134">NOTES</span></span>

## <span data-ttu-id="4e3a1-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e3a1-135">RELATED LINKS</span></span>
