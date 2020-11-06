---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 5a6ccf36f8e7aecdca4d6560614e9185a5ca26b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527054"
---
# <span data-ttu-id="5b9dc-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="5b9dc-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="5b9dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="5b9dc-103">Pobierz faktury rozliczeniowe dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5b9dc-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b9dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b9dc-104">SYNTAX</span></span>

### <span data-ttu-id="5b9dc-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="5b9dc-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b9dc-106">Późniejsza</span><span class="sxs-lookup"><span data-stu-id="5b9dc-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b9dc-107">Jedn</span><span class="sxs-lookup"><span data-stu-id="5b9dc-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b9dc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5b9dc-108">DESCRIPTION</span></span>
<span data-ttu-id="5b9dc-109">Polecenie cmdlet **Get-AzureRmBillingInvoice** umożliwia pobieranie faktur rozliczeniowych dotyczących abonamentu.</span><span class="sxs-lookup"><span data-stu-id="5b9dc-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="5b9dc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b9dc-110">EXAMPLES</span></span>

### <span data-ttu-id="5b9dc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5b9dc-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="5b9dc-112">Pobierz najnowszą fakturę z abonamentu.</span><span class="sxs-lookup"><span data-stu-id="5b9dc-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="5b9dc-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5b9dc-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="5b9dc-114">Pobierz fakturę abonamentu o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="5b9dc-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="5b9dc-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5b9dc-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="5b9dc-116">Pobierz wszystkie dostępne faktury subskrypcji w odwrotnym porządku chronologicznym, rozpoczynając od najnowszych faktur bez adresu URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="5b9dc-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="5b9dc-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="5b9dc-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="5b9dc-118">Pobierz najnowsze 10 faktur subskrypcji i Dołącz do wyników adres URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="5b9dc-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="5b9dc-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b9dc-119">PARAMETERS</span></span>

### <span data-ttu-id="5b9dc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b9dc-120">-DefaultProfile</span></span>
<span data-ttu-id="5b9dc-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5b9dc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9dc-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="5b9dc-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="5b9dc-123">Wygeneruj adres URL pobierania faktur.</span><span class="sxs-lookup"><span data-stu-id="5b9dc-123">Generate the download url of the invoices.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9dc-124">-Najnowsze</span><span class="sxs-lookup"><span data-stu-id="5b9dc-124">-Latest</span></span>
<span data-ttu-id="5b9dc-125">Pobierz najnowszą fakturę.</span><span class="sxs-lookup"><span data-stu-id="5b9dc-125">Get the latest invoice.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Latest
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9dc-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5b9dc-126">-MaxCount</span></span>
<span data-ttu-id="5b9dc-127">Określa maksymalną liczbę zwracanych rekordów.</span><span class="sxs-lookup"><span data-stu-id="5b9dc-127">Determines the maximum number of records to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9dc-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5b9dc-128">-Name</span></span>
<span data-ttu-id="5b9dc-129">Nazwa konkretnej faktury do pobrania lub ostatniej, jeśli nie została określona.</span><span class="sxs-lookup"><span data-stu-id="5b9dc-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="5b9dc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b9dc-130">CommonParameters</span></span>
<span data-ttu-id="5b9dc-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b9dc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b9dc-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b9dc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b9dc-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b9dc-133">INPUTS</span></span>

### <span data-ttu-id="5b9dc-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5b9dc-134">None</span></span>

## <span data-ttu-id="5b9dc-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b9dc-135">OUTPUTS</span></span>

### <span data-ttu-id="5b9dc-136">System. Collections. Generic. list "1 [[Microsoft. Azure. Management. rozliczenia. modele. Invoice, Microsoft. Azure. Commands. rozliczenia, wersja = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5b9dc-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Billing.Models.Invoice, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5b9dc-137">Microsoft. Azure. Management. rozliczenia. modele, faktura</span><span class="sxs-lookup"><span data-stu-id="5b9dc-137">Microsoft.Azure.Management.Billing.Models.Invoice</span></span>

## <span data-ttu-id="5b9dc-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b9dc-138">NOTES</span></span>

## <span data-ttu-id="5b9dc-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b9dc-139">RELATED LINKS</span></span>

