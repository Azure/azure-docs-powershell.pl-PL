---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 7d3c09385c76fef525535384459d03b0cc65dd9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553032"
---
# <span data-ttu-id="f137a-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="f137a-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="f137a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f137a-102">SYNOPSIS</span></span>
<span data-ttu-id="f137a-103">Uzyskaj okresy rozliczeniowe abonamentu.</span><span class="sxs-lookup"><span data-stu-id="f137a-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f137a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f137a-104">SYNTAX</span></span>

### <span data-ttu-id="f137a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f137a-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f137a-106">Jedn</span><span class="sxs-lookup"><span data-stu-id="f137a-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f137a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f137a-107">DESCRIPTION</span></span>
<span data-ttu-id="f137a-108">Polecenie cmdlet **Get-AzureRmBillingPeriod** pobiera okresy rozliczeniowe abonamentu.</span><span class="sxs-lookup"><span data-stu-id="f137a-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="f137a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f137a-109">EXAMPLES</span></span>

### <span data-ttu-id="f137a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f137a-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="f137a-111">Uzyskaj wszystkie dostępne okresy rozliczeniowe abonamentu.</span><span class="sxs-lookup"><span data-stu-id="f137a-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="f137a-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f137a-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="f137a-113">Pobierz okres rozliczeniowy abonamentu o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="f137a-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="f137a-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f137a-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="f137a-115">Uzyskaj co najwyżej 2 okresy rozliczeniowe abonamentu.</span><span class="sxs-lookup"><span data-stu-id="f137a-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="f137a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f137a-116">PARAMETERS</span></span>

### <span data-ttu-id="f137a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f137a-117">-DefaultProfile</span></span>
<span data-ttu-id="f137a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f137a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f137a-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f137a-119">-MaxCount</span></span>
<span data-ttu-id="f137a-120">Określ maksymalną liczbę zwracanych rekordów.</span><span class="sxs-lookup"><span data-stu-id="f137a-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="f137a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f137a-121">-Name</span></span>
<span data-ttu-id="f137a-122">Nazwa określonego okresu rozliczeniowego do pobrania.</span><span class="sxs-lookup"><span data-stu-id="f137a-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="f137a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f137a-123">CommonParameters</span></span>
<span data-ttu-id="f137a-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f137a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f137a-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f137a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f137a-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f137a-126">INPUTS</span></span>

### <span data-ttu-id="f137a-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f137a-127">None</span></span>

## <span data-ttu-id="f137a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f137a-128">OUTPUTS</span></span>

### <span data-ttu-id="f137a-129">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. rozliczenia. modele. PSBillingPeriod, Microsoft. Azure. Commands. rozliczenia, wersja = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f137a-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f137a-130">Microsoft. Azure. Commands. rozliczenia. modele. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="f137a-130">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="f137a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f137a-131">NOTES</span></span>

## <span data-ttu-id="f137a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f137a-132">RELATED LINKS</span></span>

