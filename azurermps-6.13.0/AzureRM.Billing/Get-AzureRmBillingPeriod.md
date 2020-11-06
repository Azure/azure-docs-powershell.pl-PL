---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 66c9a0bb9ba4aa2f17c48ffb737f1c8d72034f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550351"
---
# <span data-ttu-id="7c3b1-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="7c3b1-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="7c3b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7c3b1-103">Uzyskaj okresy rozliczeniowe abonamentu.</span><span class="sxs-lookup"><span data-stu-id="7c3b1-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c3b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c3b1-104">SYNTAX</span></span>

### <span data-ttu-id="7c3b1-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7c3b1-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c3b1-106">Jedn</span><span class="sxs-lookup"><span data-stu-id="7c3b1-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c3b1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7c3b1-107">DESCRIPTION</span></span>
<span data-ttu-id="7c3b1-108">Polecenie cmdlet **Get-AzureRmBillingPeriod** pobiera okresy rozliczeniowe abonamentu.</span><span class="sxs-lookup"><span data-stu-id="7c3b1-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="7c3b1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c3b1-109">EXAMPLES</span></span>

### <span data-ttu-id="7c3b1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7c3b1-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="7c3b1-111">Uzyskaj wszystkie dostępne okresy rozliczeniowe abonamentu.</span><span class="sxs-lookup"><span data-stu-id="7c3b1-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="7c3b1-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7c3b1-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="7c3b1-113">Pobierz okres rozliczeniowy abonamentu o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="7c3b1-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="7c3b1-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7c3b1-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="7c3b1-115">Uzyskaj co najwyżej 2 okresy rozliczeniowe abonamentu.</span><span class="sxs-lookup"><span data-stu-id="7c3b1-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="7c3b1-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c3b1-116">PARAMETERS</span></span>

### <span data-ttu-id="7c3b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c3b1-117">-DefaultProfile</span></span>
<span data-ttu-id="7c3b1-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7c3b1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c3b1-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7c3b1-119">-MaxCount</span></span>
<span data-ttu-id="7c3b1-120">Określ maksymalną liczbę zwracanych rekordów.</span><span class="sxs-lookup"><span data-stu-id="7c3b1-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="7c3b1-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7c3b1-121">-Name</span></span>
<span data-ttu-id="7c3b1-122">Nazwa określonego okresu rozliczeniowego do pobrania.</span><span class="sxs-lookup"><span data-stu-id="7c3b1-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="7c3b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c3b1-123">CommonParameters</span></span>
<span data-ttu-id="7c3b1-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c3b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c3b1-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c3b1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c3b1-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c3b1-126">INPUTS</span></span>

### <span data-ttu-id="7c3b1-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7c3b1-127">None</span></span>

## <span data-ttu-id="7c3b1-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c3b1-128">OUTPUTS</span></span>

### <span data-ttu-id="7c3b1-129">Microsoft. Azure. Commands. rozliczenia. modele. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="7c3b1-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="7c3b1-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c3b1-130">NOTES</span></span>

## <span data-ttu-id="7c3b1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c3b1-131">RELATED LINKS</span></span>
