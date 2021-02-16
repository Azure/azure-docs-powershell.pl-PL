---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: ca1e2032b312a7d0805811fb638c95777ba8ae75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199514"
---
# <span data-ttu-id="0cf57-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="0cf57-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="0cf57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cf57-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf57-103">Uzyskaj faktury za subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="0cf57-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="0cf57-104">Uzyskiwanie faktur rozliczeniowych konta rozliczeniowego i profilu rozliczeniowego</span><span class="sxs-lookup"><span data-stu-id="0cf57-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="0cf57-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0cf57-105">SYNTAX</span></span>

### <span data-ttu-id="0cf57-106">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="0cf57-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="0cf57-107">Najnowsze</span><span class="sxs-lookup"><span data-stu-id="0cf57-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="0cf57-108">Single</span><span class="sxs-lookup"><span data-stu-id="0cf57-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cf57-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="0cf57-109">DESCRIPTION</span></span>
<span data-ttu-id="0cf57-110">Polecenie **cmdlet Get-AzBillingInvoice** pobiera faktury za subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="0cf57-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="0cf57-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0cf57-111">EXAMPLES</span></span>

### <span data-ttu-id="0cf57-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0cf57-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="0cf57-113">Pobierz najnowszą fakturę za subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="0cf57-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="0cf57-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0cf57-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="0cf57-115">Pobierz fakturę subskrypcji o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="0cf57-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="0cf57-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0cf57-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="0cf57-117">Pobierz wszystkie dostępne faktury subskrypcji w odwrotnym porządku chronologicznym, począwszy od najnowszej faktury bez pobierania adresu URL.</span><span class="sxs-lookup"><span data-stu-id="0cf57-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="0cf57-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="0cf57-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="0cf57-119">Uzyskaj najnowsze 10 faktur subskrypcji i uwzględnij w wyniku adres URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="0cf57-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="0cf57-120">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="0cf57-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="0cf57-121">Uzyskaj określoną fakturę według nazwy i dołącz adres URL pobierania w wyniku.</span><span class="sxs-lookup"><span data-stu-id="0cf57-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="0cf57-122">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="0cf57-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="0cf57-123">Pobieraj faktury według nazwy konta rozliczeniowego i uwzględnij w wyniku adres URL każdej faktury.</span><span class="sxs-lookup"><span data-stu-id="0cf57-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="0cf57-124">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="0cf57-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="0cf57-125">Uzyskaj określoną fakturę według nazwy faktury i nazwy konta rozliczeniowego oraz dołącz adres URL pobierania każdej faktury w wyniku.</span><span class="sxs-lookup"><span data-stu-id="0cf57-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="0cf57-126">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="0cf57-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="0cf57-127">Uzyskaj najnowszą fakturę według nazwy konta rozliczeniowego i uwzględnij w wyniku adres URL faktury.</span><span class="sxs-lookup"><span data-stu-id="0cf57-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="0cf57-128">Przykład 9</span><span class="sxs-lookup"><span data-stu-id="0cf57-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="0cf57-129">Uzyskaj najnowsze 10 faktur z konkretnego konta rozliczeniowego i określonego profilu rozliczeniowego oraz uwzględnij w wynikach adres URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="0cf57-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="0cf57-130">Przykład 10</span><span class="sxs-lookup"><span data-stu-id="0cf57-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="0cf57-131">Uzyskaj najnowszą fakturę według nazwy konta rozliczeniowego i nazwy profilu rozliczeniowego oraz uwzględnij w wyniku adres URL pobierania faktury.</span><span class="sxs-lookup"><span data-stu-id="0cf57-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="0cf57-132">Przykład 10</span><span class="sxs-lookup"><span data-stu-id="0cf57-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="0cf57-133">Uzyskaj faktury według nazwy konta rozliczeniowego i nazwy profilu rozliczeniowego dla okresu rozliczeniowego określonego przez datę rozpoczęcia i datę zakończenia okresu.</span><span class="sxs-lookup"><span data-stu-id="0cf57-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="0cf57-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cf57-134">PARAMETERS</span></span>

### <span data-ttu-id="0cf57-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf57-135">-DefaultProfile</span></span>
<span data-ttu-id="0cf57-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0cf57-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cf57-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="0cf57-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="0cf57-138">Wygeneruj adres URL pobierania faktur.</span><span class="sxs-lookup"><span data-stu-id="0cf57-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="0cf57-139">— najnowsza wersja</span><span class="sxs-lookup"><span data-stu-id="0cf57-139">-Latest</span></span>
<span data-ttu-id="0cf57-140">Pobierz najnowszą fakturę.</span><span class="sxs-lookup"><span data-stu-id="0cf57-140">Get the latest invoice.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf57-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0cf57-141">-MaxCount</span></span>
<span data-ttu-id="0cf57-142">Określa maksymalną liczbę rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="0cf57-142">Determines the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf57-143">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0cf57-143">-Name</span></span>
<span data-ttu-id="0cf57-144">Nazwa określonej faktury do uzyskania lub najnowsza, jeśli nie jest określona.</span><span class="sxs-lookup"><span data-stu-id="0cf57-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="0cf57-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="0cf57-145">-BillingAccountName</span></span>
<span data-ttu-id="0cf57-146">Nazwa konkretnego konta rozliczeniowego, na które chcesz uzyskać faktury.</span><span class="sxs-lookup"><span data-stu-id="0cf57-146">Name of a specific billing account to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf57-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="0cf57-147">-BillingProfileName</span></span>
<span data-ttu-id="0cf57-148">Nazwa konkretnego profilu rozliczeniowego, za który chcesz uzyskać faktury.</span><span class="sxs-lookup"><span data-stu-id="0cf57-148">Name of a specific billing profile to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf57-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="0cf57-149">-PeriodStartDate</span></span>
<span data-ttu-id="0cf57-150">Data rozpoczęcia faktury.</span><span class="sxs-lookup"><span data-stu-id="0cf57-150">Start date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cf57-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="0cf57-151">-PeriodEndDate</span></span>
<span data-ttu-id="0cf57-152">Data zakończenia faktury.</span><span class="sxs-lookup"><span data-stu-id="0cf57-152">End date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### <span data-ttu-id="0cf57-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf57-153">CommonParameters</span></span>
<span data-ttu-id="0cf57-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf57-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf57-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cf57-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf57-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cf57-156">INPUTS</span></span>

### <span data-ttu-id="0cf57-157">Brak</span><span class="sxs-lookup"><span data-stu-id="0cf57-157">None</span></span>

## <span data-ttu-id="0cf57-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0cf57-158">OUTPUTS</span></span>

### <span data-ttu-id="0cf57-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span><span class="sxs-lookup"><span data-stu-id="0cf57-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="0cf57-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0cf57-160">NOTES</span></span>

## <span data-ttu-id="0cf57-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cf57-161">RELATED LINKS</span></span>
