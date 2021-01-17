---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339766"
---
# <span data-ttu-id="e4cf4-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="e4cf4-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="e4cf4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="e4cf4-103">Uzyskaj profile rozliczeń.</span><span class="sxs-lookup"><span data-stu-id="e4cf4-103">Get billing profiles.</span></span>

## <span data-ttu-id="e4cf4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4cf4-104">SYNTAX</span></span>

### <span data-ttu-id="e4cf4-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e4cf4-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4cf4-106">Jedn</span><span class="sxs-lookup"><span data-stu-id="e4cf4-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4cf4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e4cf4-107">DESCRIPTION</span></span>
<span data-ttu-id="e4cf4-108">Polecenie cmdlet **Get-AzBillingProfile** pobiera profile rozliczeń w ramach określonego konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="e4cf4-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="e4cf4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4cf4-109">EXAMPLES</span></span>

### <span data-ttu-id="e4cf4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e4cf4-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="e4cf4-111">Pobierz wszystkie profile rozliczeń w ramach określonego konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="e4cf4-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="e4cf4-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e4cf4-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="e4cf4-113">Pobierz profil rozliczeń o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="e4cf4-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="e4cf4-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e4cf4-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="e4cf4-115">Pobierz wszystkie profile rozliczeń w obszarze określone konto rozliczeniowe i Uwzględnij w wynikach sekcje faktur.</span><span class="sxs-lookup"><span data-stu-id="e4cf4-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="e4cf4-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="e4cf4-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="e4cf4-117">Pobierz profil rozliczeń o określonej nazwie i Dołącz sekcje faktury w wynikach.</span><span class="sxs-lookup"><span data-stu-id="e4cf4-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="e4cf4-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4cf4-118">PARAMETERS</span></span>

### <span data-ttu-id="e4cf4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4cf4-119">-DefaultProfile</span></span>
<span data-ttu-id="e4cf4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e4cf4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4cf4-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="e4cf4-121">-BillingAccountName</span></span>
<span data-ttu-id="e4cf4-122">Nazwa określonego konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="e4cf4-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="e4cf4-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="e4cf4-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="e4cf4-124">Uwzględnij sekcje faktur w obszarze Profil rozliczeń.</span><span class="sxs-lookup"><span data-stu-id="e4cf4-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="e4cf4-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4cf4-125">-Name</span></span>
<span data-ttu-id="e4cf4-126">Nazwa określonego profilu rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="e4cf4-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="e4cf4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4cf4-127">CommonParameters</span></span>
<span data-ttu-id="e4cf4-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4cf4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4cf4-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4cf4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4cf4-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4cf4-130">INPUTS</span></span>

### <span data-ttu-id="e4cf4-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e4cf4-131">None</span></span>

## <span data-ttu-id="e4cf4-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4cf4-132">OUTPUTS</span></span>

### <span data-ttu-id="e4cf4-133">Microsoft. Azure. Commands. rozliczenia. modele. PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="e4cf4-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="e4cf4-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4cf4-134">NOTES</span></span>

## <span data-ttu-id="e4cf4-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4cf4-135">RELATED LINKS</span></span>
