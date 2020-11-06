---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 1f21022294b1bcf5c75a7cf49dcc009600dc4cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550348"
---
# <span data-ttu-id="12857-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="12857-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="12857-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12857-102">SYNOPSIS</span></span>
<span data-ttu-id="12857-103">Pobierz faktury rozliczeniowe dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="12857-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12857-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12857-104">SYNTAX</span></span>

### <span data-ttu-id="12857-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="12857-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12857-106">Późniejsza</span><span class="sxs-lookup"><span data-stu-id="12857-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12857-107">Jedn</span><span class="sxs-lookup"><span data-stu-id="12857-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12857-108">Opis</span><span class="sxs-lookup"><span data-stu-id="12857-108">DESCRIPTION</span></span>
<span data-ttu-id="12857-109">Polecenie cmdlet **Get-AzureRmBillingInvoice** umożliwia pobieranie faktur rozliczeniowych dotyczących abonamentu.</span><span class="sxs-lookup"><span data-stu-id="12857-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="12857-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12857-110">EXAMPLES</span></span>

### <span data-ttu-id="12857-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="12857-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="12857-112">Pobierz najnowszą fakturę z abonamentu.</span><span class="sxs-lookup"><span data-stu-id="12857-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="12857-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="12857-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="12857-114">Pobierz fakturę abonamentu o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="12857-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="12857-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="12857-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="12857-116">Pobierz wszystkie dostępne faktury subskrypcji w odwrotnym porządku chronologicznym, rozpoczynając od najnowszych faktur bez adresu URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="12857-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="12857-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="12857-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="12857-118">Pobierz najnowsze 10 faktur subskrypcji i Dołącz do wyników adres URL pobierania.</span><span class="sxs-lookup"><span data-stu-id="12857-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="12857-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12857-119">PARAMETERS</span></span>

### <span data-ttu-id="12857-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12857-120">-DefaultProfile</span></span>
<span data-ttu-id="12857-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="12857-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12857-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="12857-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="12857-123">Wygeneruj adres URL pobierania faktur.</span><span class="sxs-lookup"><span data-stu-id="12857-123">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="12857-124">-Najnowsze</span><span class="sxs-lookup"><span data-stu-id="12857-124">-Latest</span></span>
<span data-ttu-id="12857-125">Pobierz najnowszą fakturę.</span><span class="sxs-lookup"><span data-stu-id="12857-125">Get the latest invoice.</span></span>

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

### <span data-ttu-id="12857-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="12857-126">-MaxCount</span></span>
<span data-ttu-id="12857-127">Określa maksymalną liczbę zwracanych rekordów.</span><span class="sxs-lookup"><span data-stu-id="12857-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="12857-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="12857-128">-Name</span></span>
<span data-ttu-id="12857-129">Nazwa konkretnej faktury do pobrania lub ostatniej, jeśli nie została określona.</span><span class="sxs-lookup"><span data-stu-id="12857-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="12857-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12857-130">CommonParameters</span></span>
<span data-ttu-id="12857-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12857-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12857-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12857-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12857-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12857-133">INPUTS</span></span>

### <span data-ttu-id="12857-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="12857-134">None</span></span>

## <span data-ttu-id="12857-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12857-135">OUTPUTS</span></span>

### <span data-ttu-id="12857-136">Microsoft. Azure. Commands. rozliczenia. modele. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="12857-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="12857-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12857-137">NOTES</span></span>

## <span data-ttu-id="12857-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12857-138">RELATED LINKS</span></span>
