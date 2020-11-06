---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 38b1c4e29ed82ac3bddcff9565a216bd6db23411
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549248"
---
# <span data-ttu-id="798ea-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="798ea-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="798ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="798ea-102">SYNOPSIS</span></span>
<span data-ttu-id="798ea-103">Pobierz faktury rozliczeniowe dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="798ea-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="798ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="798ea-104">SYNTAX</span></span>

### <span data-ttu-id="798ea-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="798ea-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="798ea-106">Późniejsza</span><span class="sxs-lookup"><span data-stu-id="798ea-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="798ea-107">Jedn</span><span class="sxs-lookup"><span data-stu-id="798ea-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="798ea-108">Opis</span><span class="sxs-lookup"><span data-stu-id="798ea-108">DESCRIPTION</span></span>
<span data-ttu-id="798ea-109">Polecenie cmdlet **Get-AzureRmBillingInvoice** umożliwia pobieranie faktur rozliczeniowych dotyczących abonamentu.</span><span class="sxs-lookup"><span data-stu-id="798ea-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="798ea-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="798ea-110">EXAMPLES</span></span>

### <span data-ttu-id="798ea-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="798ea-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="798ea-112">Pobierz najnowszą fakturę z abonamentu.</span><span class="sxs-lookup"><span data-stu-id="798ea-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="798ea-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="798ea-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="798ea-114">Pobierz fakturę abonamentu o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="798ea-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="798ea-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="798ea-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="798ea-116">Pobierz wszystkie dostępne faktury subskrypcji w odwrotnym porządku chronologicznym, rozpoczynając od najnowszych faktur bez adresu URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="798ea-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="798ea-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="798ea-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="798ea-118">Pobierz najnowsze 10 faktur subskrypcji i Dołącz do wyników adres URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="798ea-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="798ea-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="798ea-119">PARAMETERS</span></span>

### <span data-ttu-id="798ea-120">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="798ea-120">-GenerateDownloadUrl</span></span>
<span data-ttu-id="798ea-121">Wygeneruj adres URL pobierania faktur.</span><span class="sxs-lookup"><span data-stu-id="798ea-121">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="798ea-122">-Najnowsze</span><span class="sxs-lookup"><span data-stu-id="798ea-122">-Latest</span></span>
<span data-ttu-id="798ea-123">Pobierz najnowszą fakturę.</span><span class="sxs-lookup"><span data-stu-id="798ea-123">Get the latest invoice.</span></span>

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

### <span data-ttu-id="798ea-124">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="798ea-124">-MaxCount</span></span>
<span data-ttu-id="798ea-125">Określa maksymalną liczbę zwracanych rekordów.</span><span class="sxs-lookup"><span data-stu-id="798ea-125">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="798ea-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="798ea-126">-Name</span></span>
<span data-ttu-id="798ea-127">Nazwa konkretnej faktury do pobrania lub ostatniej, jeśli nie została określona.</span><span class="sxs-lookup"><span data-stu-id="798ea-127">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="798ea-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="798ea-128">-DefaultProfile</span></span>
<span data-ttu-id="798ea-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="798ea-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="798ea-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="798ea-130">CommonParameters</span></span>
<span data-ttu-id="798ea-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="798ea-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="798ea-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="798ea-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="798ea-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="798ea-133">INPUTS</span></span>

### <span data-ttu-id="798ea-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="798ea-134">None</span></span>

## <span data-ttu-id="798ea-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="798ea-135">OUTPUTS</span></span>

### <span data-ttu-id="798ea-136">System. Collections. Generic. list "1 [[Microsoft. Azure. Management. rozliczenia. modele. Invoice, Microsoft. Azure. Commands. rozliczenia, wersja = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="798ea-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Billing.Models.Invoice, Microsoft.Azure.Commands.Billing, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="798ea-137">Microsoft. Azure. Management. rozliczenia. modele, faktura</span><span class="sxs-lookup"><span data-stu-id="798ea-137">Microsoft.Azure.Management.Billing.Models.Invoice</span></span>

## <span data-ttu-id="798ea-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="798ea-138">NOTES</span></span>

## <span data-ttu-id="798ea-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="798ea-139">RELATED LINKS</span></span>

