---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2b1906d07b3e08b1761469b4a9d6d8d565e0fd8c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051406"
---
# <span data-ttu-id="41abe-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="41abe-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="41abe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41abe-102">SYNOPSIS</span></span>
<span data-ttu-id="41abe-103">Pobierz faktury rozliczeniowe dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="41abe-103">Get billing invoices of the subscription.</span></span>

## <span data-ttu-id="41abe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41abe-104">SYNTAX</span></span>

### <span data-ttu-id="41abe-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="41abe-105">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41abe-106">Późniejsza</span><span class="sxs-lookup"><span data-stu-id="41abe-106">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41abe-107">Jedn</span><span class="sxs-lookup"><span data-stu-id="41abe-107">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41abe-108">Opis</span><span class="sxs-lookup"><span data-stu-id="41abe-108">DESCRIPTION</span></span>
<span data-ttu-id="41abe-109">Polecenie cmdlet **Get-AzBillingInvoice** umożliwia pobieranie faktur rozliczeniowych dotyczących abonamentu.</span><span class="sxs-lookup"><span data-stu-id="41abe-109">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="41abe-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41abe-110">EXAMPLES</span></span>

### <span data-ttu-id="41abe-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="41abe-111">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="41abe-112">Pobierz najnowszą fakturę z abonamentu.</span><span class="sxs-lookup"><span data-stu-id="41abe-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="41abe-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="41abe-113">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="41abe-114">Pobierz fakturę abonamentu o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="41abe-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="41abe-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="41abe-115">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="41abe-116">Pobierz wszystkie dostępne faktury subskrypcji w odwrotnym porządku chronologicznym, rozpoczynając od najnowszych faktur bez adresu URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="41abe-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="41abe-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="41abe-117">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="41abe-118">Pobierz najnowsze 10 faktur subskrypcji i Dołącz do wyników adres URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="41abe-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="41abe-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41abe-119">PARAMETERS</span></span>

### <span data-ttu-id="41abe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41abe-120">-DefaultProfile</span></span>
<span data-ttu-id="41abe-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="41abe-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41abe-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="41abe-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="41abe-123">Wygeneruj adres URL pobierania faktur.</span><span class="sxs-lookup"><span data-stu-id="41abe-123">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41abe-124">-Najnowsze</span><span class="sxs-lookup"><span data-stu-id="41abe-124">-Latest</span></span>
<span data-ttu-id="41abe-125">Pobierz najnowszą fakturę.</span><span class="sxs-lookup"><span data-stu-id="41abe-125">Get the latest invoice.</span></span>

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

### <span data-ttu-id="41abe-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="41abe-126">-MaxCount</span></span>
<span data-ttu-id="41abe-127">Określa maksymalną liczbę zwracanych rekordów.</span><span class="sxs-lookup"><span data-stu-id="41abe-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="41abe-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41abe-128">-Name</span></span>
<span data-ttu-id="41abe-129">Nazwa konkretnej faktury do pobrania lub ostatniej, jeśli nie została określona.</span><span class="sxs-lookup"><span data-stu-id="41abe-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="41abe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41abe-130">CommonParameters</span></span>
<span data-ttu-id="41abe-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41abe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41abe-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41abe-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41abe-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41abe-133">INPUTS</span></span>

### <span data-ttu-id="41abe-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="41abe-134">None</span></span>

## <span data-ttu-id="41abe-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41abe-135">OUTPUTS</span></span>

### <span data-ttu-id="41abe-136">Microsoft. Azure. Commands. rozliczenia. modele. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="41abe-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="41abe-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41abe-137">NOTES</span></span>

## <span data-ttu-id="41abe-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41abe-138">RELATED LINKS</span></span>
