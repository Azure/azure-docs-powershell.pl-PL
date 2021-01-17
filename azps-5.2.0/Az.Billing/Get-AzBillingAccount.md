---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351238"
---
# <span data-ttu-id="e1aa7-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="e1aa7-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="e1aa7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="e1aa7-103">Pobierz konta rozliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-103">Get billing accounts.</span></span>

## <span data-ttu-id="e1aa7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1aa7-104">SYNTAX</span></span>

### <span data-ttu-id="e1aa7-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e1aa7-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1aa7-106">Jedn</span><span class="sxs-lookup"><span data-stu-id="e1aa7-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1aa7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e1aa7-107">DESCRIPTION</span></span>
<span data-ttu-id="e1aa7-108">Polecenie cmdlet **Get-AzBillingAccount** pobiera konta rozliczeniowe, do których użytkownik ma dostęp.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="e1aa7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1aa7-109">EXAMPLES</span></span>

### <span data-ttu-id="e1aa7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e1aa7-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="e1aa7-111">Pobierz wszystkie konta rozliczeniowe, do których ma dostęp użytkownik.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="e1aa7-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e1aa7-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="e1aa7-113">Pobierz konto rozliczeniowe o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="e1aa7-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e1aa7-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="e1aa7-115">Pobierz wszystkie konta rozliczeniowe, do których użytkownik ma dostęp, i Dołącz ten adres do wyniku.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="e1aa7-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="e1aa7-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="e1aa7-117">Pobierz wszystkie konta rozliczeniowe, do których jest dostęp, i Dołącz do nich profile rozliczeń.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="e1aa7-118">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="e1aa7-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="e1aa7-119">Pobierz wszystkie konta rozliczeniowe, do których masz dostęp, i Dołącz do nich sekcje Profile rozliczeń i faktury.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="e1aa7-120">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="e1aa7-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="e1aa7-121">Pobierz konto rozliczeniowe o określonej nazwie, a następnie w wynikach Uwzględnij adres, profile rozliczeń i faktury.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="e1aa7-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1aa7-122">PARAMETERS</span></span>

### <span data-ttu-id="e1aa7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1aa7-123">-DefaultProfile</span></span>
<span data-ttu-id="e1aa7-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e1aa7-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1aa7-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="e1aa7-125">-IncludeAddress</span></span>
<span data-ttu-id="e1aa7-126">Uwzględnij adres konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="e1aa7-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="e1aa7-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="e1aa7-128">Uwzględnij profile rozliczeń w obszarze konto rozliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="e1aa7-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="e1aa7-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="e1aa7-130">Uwzględnij profile rozliczeń w sekcji konto rozliczeniowe i faktury pod nimi.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="e1aa7-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1aa7-131">-Name</span></span>
<span data-ttu-id="e1aa7-132">Nazwa określonego konta rozliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="e1aa7-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="e1aa7-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="e1aa7-134">Wystaw jednostki rozliczeniowe w obszarze konto rozliczeniowe, których można użyć jako danych wejściowych w celu utworzenia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

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

### <span data-ttu-id="e1aa7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1aa7-135">CommonParameters</span></span>
<span data-ttu-id="e1aa7-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1aa7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1aa7-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1aa7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1aa7-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1aa7-138">INPUTS</span></span>

### <span data-ttu-id="e1aa7-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e1aa7-139">None</span></span>

## <span data-ttu-id="e1aa7-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1aa7-140">OUTPUTS</span></span>

### <span data-ttu-id="e1aa7-141">Microsoft. Azure. Commands. rozliczenia. modele. PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="e1aa7-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="e1aa7-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1aa7-142">NOTES</span></span>

## <span data-ttu-id="e1aa7-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1aa7-143">RELATED LINKS</span></span>
