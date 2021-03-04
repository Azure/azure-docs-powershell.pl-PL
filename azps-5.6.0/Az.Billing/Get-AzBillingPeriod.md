---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: d2a859740d2e5627eca3ca0748aab8e72c1ee9af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990452"
---
# <span data-ttu-id="d2e22-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="d2e22-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="d2e22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e22-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e22-103">Uzyskaj okresy rozliczeniowe subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d2e22-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="d2e22-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2e22-104">SYNTAX</span></span>

### <span data-ttu-id="d2e22-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d2e22-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e22-106">Single</span><span class="sxs-lookup"><span data-stu-id="d2e22-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2e22-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2e22-107">DESCRIPTION</span></span>
<span data-ttu-id="d2e22-108">Polecenie **cmdlet Get-AzBillingPeriod** pobiera okresy rozliczeniowe subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d2e22-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="d2e22-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2e22-109">EXAMPLES</span></span>

### <span data-ttu-id="d2e22-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d2e22-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="d2e22-111">Uzyskaj wszystkie dostępne okresy rozliczeniowe subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d2e22-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="d2e22-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d2e22-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="d2e22-113">Uzyskaj okres rozliczeniowy subskrypcji pod określoną nazwą.</span><span class="sxs-lookup"><span data-stu-id="d2e22-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="d2e22-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d2e22-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="d2e22-115">Uzyskaj co najwyżej 2 okresy rozliczeniowe subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d2e22-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="d2e22-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2e22-116">PARAMETERS</span></span>

### <span data-ttu-id="d2e22-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e22-117">-DefaultProfile</span></span>
<span data-ttu-id="d2e22-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d2e22-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2e22-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d2e22-119">-MaxCount</span></span>
<span data-ttu-id="d2e22-120">Określ maksymalną liczbę rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="d2e22-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="d2e22-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d2e22-121">-Name</span></span>
<span data-ttu-id="d2e22-122">Nazwa konkretnego okresu rozliczeniowego do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="d2e22-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="d2e22-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e22-123">CommonParameters</span></span>
<span data-ttu-id="d2e22-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2e22-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e22-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e22-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e22-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2e22-126">INPUTS</span></span>

### <span data-ttu-id="d2e22-127">Brak</span><span class="sxs-lookup"><span data-stu-id="d2e22-127">None</span></span>

## <span data-ttu-id="d2e22-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2e22-128">OUTPUTS</span></span>

### <span data-ttu-id="d2e22-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="d2e22-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="d2e22-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2e22-130">NOTES</span></span>

## <span data-ttu-id="d2e22-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2e22-131">RELATED LINKS</span></span>
