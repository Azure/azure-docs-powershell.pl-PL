---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232897"
---
# <span data-ttu-id="fe80c-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="fe80c-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="fe80c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe80c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe80c-103">Uzyskaj okresy rozliczeniowe abonamentu.</span><span class="sxs-lookup"><span data-stu-id="fe80c-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="fe80c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe80c-104">SYNTAX</span></span>

### <span data-ttu-id="fe80c-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="fe80c-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe80c-106">Jedn</span><span class="sxs-lookup"><span data-stu-id="fe80c-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe80c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fe80c-107">DESCRIPTION</span></span>
<span data-ttu-id="fe80c-108">Polecenie cmdlet **Get-AzBillingPeriod** pobiera okresy rozliczeniowe abonamentu.</span><span class="sxs-lookup"><span data-stu-id="fe80c-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="fe80c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe80c-109">EXAMPLES</span></span>

### <span data-ttu-id="fe80c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fe80c-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="fe80c-111">Uzyskaj wszystkie dostępne okresy rozliczeniowe abonamentu.</span><span class="sxs-lookup"><span data-stu-id="fe80c-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="fe80c-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fe80c-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="fe80c-113">Pobierz okres rozliczeniowy abonamentu o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="fe80c-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="fe80c-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="fe80c-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="fe80c-115">Uzyskaj co najwyżej 2 okresy rozliczeniowe abonamentu.</span><span class="sxs-lookup"><span data-stu-id="fe80c-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="fe80c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe80c-116">PARAMETERS</span></span>

### <span data-ttu-id="fe80c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe80c-117">-DefaultProfile</span></span>
<span data-ttu-id="fe80c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fe80c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe80c-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fe80c-119">-MaxCount</span></span>
<span data-ttu-id="fe80c-120">Określ maksymalną liczbę zwracanych rekordów.</span><span class="sxs-lookup"><span data-stu-id="fe80c-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="fe80c-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fe80c-121">-Name</span></span>
<span data-ttu-id="fe80c-122">Nazwa określonego okresu rozliczeniowego do pobrania.</span><span class="sxs-lookup"><span data-stu-id="fe80c-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="fe80c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe80c-123">CommonParameters</span></span>
<span data-ttu-id="fe80c-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe80c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe80c-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe80c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe80c-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe80c-126">INPUTS</span></span>

### <span data-ttu-id="fe80c-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fe80c-127">None</span></span>

## <span data-ttu-id="fe80c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe80c-128">OUTPUTS</span></span>

### <span data-ttu-id="fe80c-129">Microsoft. Azure. Commands. rozliczenia. modele. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="fe80c-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="fe80c-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe80c-130">NOTES</span></span>

## <span data-ttu-id="fe80c-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe80c-131">RELATED LINKS</span></span>
