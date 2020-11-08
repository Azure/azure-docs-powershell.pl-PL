---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2392b3275feeb6fa23f8f76dd3e76b6d97c33d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232899"
---
# <span data-ttu-id="b9f2a-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="b9f2a-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="b9f2a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f2a-103">Pobierz faktury rozliczeniowe dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="b9f2a-104">Pobieranie faktur rozliczeniowych dotyczących konta rozliczeniowego i profilu rozliczeń</span><span class="sxs-lookup"><span data-stu-id="b9f2a-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="b9f2a-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9f2a-105">SYNTAX</span></span>

### <span data-ttu-id="b9f2a-106">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b9f2a-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="b9f2a-107">Późniejsza</span><span class="sxs-lookup"><span data-stu-id="b9f2a-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="b9f2a-108">Jedn</span><span class="sxs-lookup"><span data-stu-id="b9f2a-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9f2a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b9f2a-109">DESCRIPTION</span></span>
<span data-ttu-id="b9f2a-110">Polecenie cmdlet **Get-AzBillingInvoice** umożliwia pobieranie faktur rozliczeniowych dotyczących abonamentu.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="b9f2a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9f2a-111">EXAMPLES</span></span>

### <span data-ttu-id="b9f2a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b9f2a-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="b9f2a-113">Pobierz najnowszą fakturę z abonamentu.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="b9f2a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b9f2a-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="b9f2a-115">Pobierz fakturę abonamentu o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="b9f2a-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b9f2a-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="b9f2a-117">Pobierz wszystkie dostępne faktury subskrypcji w odwrotnym porządku chronologicznym, rozpoczynając od najnowszych faktur bez adresu URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="b9f2a-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="b9f2a-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="b9f2a-119">Pobierz najnowsze 10 faktur subskrypcji i Dołącz do wyników adres URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="b9f2a-120">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="b9f2a-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="b9f2a-121">Pobierz określoną fakturę według nazwy i Dołącz adres URL pobierania w wyniku.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="b9f2a-122">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="b9f2a-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="b9f2a-123">Pobierz faktury według nazwy konta rozliczeniowego i Dołącz adres URL pobierania dla każdej faktury w wyniku.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="b9f2a-124">Przykład 7</span><span class="sxs-lookup"><span data-stu-id="b9f2a-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="b9f2a-125">Pobierz określoną fakturę według nazwy faktury i nazwy konta rozliczeniowego i Dołącz adres URL pobierania dla każdej faktury w wyniku.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="b9f2a-126">Przykład 8</span><span class="sxs-lookup"><span data-stu-id="b9f2a-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="b9f2a-127">Pobierz najnowszą fakturę według nazwy konta rozliczeniowego i Dołącz adres URL pobierania dla faktury w wyniku.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="b9f2a-128">Przykład 9</span><span class="sxs-lookup"><span data-stu-id="b9f2a-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="b9f2a-129">Pobierz najnowsze 10 faktur z określonego konta rozliczeniowego i konkretnego profilu rozliczeń i Dołącz do wyników adres URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="b9f2a-130">Przykład 10</span><span class="sxs-lookup"><span data-stu-id="b9f2a-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="b9f2a-131">Pobierz najnowszą fakturę według nazwy konta rozliczeniowego oraz nazwy profilu rozliczeń i Dołącz adres URL pobierania dla faktury w wyniku.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="b9f2a-132">Przykład 10</span><span class="sxs-lookup"><span data-stu-id="b9f2a-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="b9f2a-133">Pobierz faktury według nazwy konta rozliczeniowego i nazwy profilu rozliczeń dla okresu rozliczeniowego określonego przez datę perioStart i datę periodEnd.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="b9f2a-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9f2a-134">PARAMETERS</span></span>

### <span data-ttu-id="b9f2a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f2a-135">-DefaultProfile</span></span>
<span data-ttu-id="b9f2a-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b9f2a-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9f2a-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="b9f2a-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="b9f2a-138">Wygeneruj adres URL pobierania faktur.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="b9f2a-139">-Najnowsze</span><span class="sxs-lookup"><span data-stu-id="b9f2a-139">-Latest</span></span>
<span data-ttu-id="b9f2a-140">Pobierz najnowszą fakturę.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="b9f2a-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b9f2a-141">-MaxCount</span></span>
<span data-ttu-id="b9f2a-142">Określa maksymalną liczbę zwracanych rekordów.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="b9f2a-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b9f2a-143">-Name</span></span>
<span data-ttu-id="b9f2a-144">Nazwa konkretnej faktury do pobrania lub ostatniej, jeśli nie została określona.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="b9f2a-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="b9f2a-145">-BillingAccountName</span></span>
<span data-ttu-id="b9f2a-146">Nazwa określonego konta rozliczeniowego, za pomocą którego można uzyskać faktury.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-146">Name of a specific billing account to get invoices for.</span></span>

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

### <span data-ttu-id="b9f2a-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="b9f2a-147">-BillingProfileName</span></span>
<span data-ttu-id="b9f2a-148">Nazwa określonego profilu rozliczeń, za pomocą którego można uzyskać faktury.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-148">Name of a specific billing profile to get invoices for.</span></span>

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

### <span data-ttu-id="b9f2a-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="b9f2a-149">-PeriodStartDate</span></span>
<span data-ttu-id="b9f2a-150">Data rozpoczęcia faktury.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-150">Start date for invoice.</span></span>

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

### <span data-ttu-id="b9f2a-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="b9f2a-151">-PeriodEndDate</span></span>
<span data-ttu-id="b9f2a-152">Data zakończenia fakturowania.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-152">End date for invoice.</span></span>

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



### <span data-ttu-id="b9f2a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f2a-153">CommonParameters</span></span>
<span data-ttu-id="b9f2a-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9f2a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f2a-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9f2a-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f2a-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9f2a-156">INPUTS</span></span>

### <span data-ttu-id="b9f2a-157">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b9f2a-157">None</span></span>

## <span data-ttu-id="b9f2a-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9f2a-158">OUTPUTS</span></span>

### <span data-ttu-id="b9f2a-159">Microsoft. Azure. Commands. rozliczenia. modele. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="b9f2a-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="b9f2a-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9f2a-160">NOTES</span></span>

## <span data-ttu-id="b9f2a-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9f2a-161">RELATED LINKS</span></span>
