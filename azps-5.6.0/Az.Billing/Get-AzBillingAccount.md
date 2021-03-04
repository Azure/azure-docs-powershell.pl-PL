---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 8c934adfd0bea950f97fbe8e8226568f9eaf57dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959786"
---
# <span data-ttu-id="357de-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="357de-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="357de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="357de-102">SYNOPSIS</span></span>
<span data-ttu-id="357de-103">Uzyskaj konta rozliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="357de-103">Get billing accounts.</span></span>

## <span data-ttu-id="357de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="357de-104">SYNTAX</span></span>

### <span data-ttu-id="357de-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="357de-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="357de-106">Single</span><span class="sxs-lookup"><span data-stu-id="357de-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="357de-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="357de-107">DESCRIPTION</span></span>
<span data-ttu-id="357de-108">Polecenie **cmdlet Get-AzBillingAccount** pobiera konta rozliczeniowe, użytkownik ma do nich dostęp.</span><span class="sxs-lookup"><span data-stu-id="357de-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="357de-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="357de-109">EXAMPLES</span></span>

### <span data-ttu-id="357de-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="357de-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="357de-111">Uzyskaj dostęp do wszystkich kont rozliczeniowych, do których ma dostęp użytkownik.</span><span class="sxs-lookup"><span data-stu-id="357de-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="357de-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="357de-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="357de-113">Pobierz konto rozliczeniowe o podanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="357de-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="357de-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="357de-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="357de-115">Pobierz wszystkie konta rozliczeniowe, do których użytkownik ma dostęp, i uwzględnij adres w wynikach.</span><span class="sxs-lookup"><span data-stu-id="357de-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="357de-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="357de-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="357de-117">Uzyskaj dostęp do wszystkich kont rozliczeniowych i uwzględnij profile rozliczeniowe w wynikach.</span><span class="sxs-lookup"><span data-stu-id="357de-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="357de-118">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="357de-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="357de-119">Uzyskaj dostęp do wszystkich kont rozliczeniowych, do których ma dostęp użytkownik, oraz uwzględnij w wynikach sekcje dotyczące faktur i profile rozliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="357de-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="357de-120">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="357de-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="357de-121">Uzyskaj konto rozliczeniowe o podanej nazwie i uwzględnij w wynikach sekcje adresu, profilów rozliczeń i faktur.</span><span class="sxs-lookup"><span data-stu-id="357de-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="357de-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="357de-122">PARAMETERS</span></span>

### <span data-ttu-id="357de-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357de-123">-DefaultProfile</span></span>
<span data-ttu-id="357de-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="357de-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="357de-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="357de-125">-IncludeAddress</span></span>
<span data-ttu-id="357de-126">Uwzględnij adres konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="357de-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="357de-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="357de-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="357de-128">Uwzględnij profile rozliczeniowe w obszarze konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="357de-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="357de-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="357de-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="357de-130">Uwzględnij profile rozliczeniowe w sekcjach konta rozliczeniowego i faktur pod nimi.</span><span class="sxs-lookup"><span data-stu-id="357de-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="357de-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="357de-131">-Name</span></span>
<span data-ttu-id="357de-132">Nazwa konkretnego konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="357de-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="357de-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="357de-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="357de-134">Utwórz listę jednostek rozliczeniowych w obszarze konta rozliczeniowego, których można użyć jako danych wejściowych do utworzenia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="357de-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="357de-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357de-135">CommonParameters</span></span>
<span data-ttu-id="357de-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="357de-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357de-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="357de-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357de-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="357de-138">INPUTS</span></span>

### <span data-ttu-id="357de-139">Brak</span><span class="sxs-lookup"><span data-stu-id="357de-139">None</span></span>

## <span data-ttu-id="357de-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="357de-140">OUTPUTS</span></span>

### <span data-ttu-id="357de-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="357de-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="357de-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="357de-142">NOTES</span></span>

## <span data-ttu-id="357de-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="357de-143">RELATED LINKS</span></span>
