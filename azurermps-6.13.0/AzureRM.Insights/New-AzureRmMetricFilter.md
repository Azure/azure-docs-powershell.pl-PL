---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
ms.openlocfilehash: 783f5c780b0202ddb78666c2c7446ba07b5434e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719432"
---
# <span data-ttu-id="61b6c-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="61b6c-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="61b6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="61b6c-103">Umożliwia utworzenie filtru wymiaru metrycznego, którego można użyć do zbadania metryk.</span><span class="sxs-lookup"><span data-stu-id="61b6c-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61b6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61b6c-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61b6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="61b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="61b6c-106">Polecenie cmdlet **New-AzureRmMetricFilter** umożliwia utworzenie filtru wymiaru metrycznego, którego można użyć do zbadania metryk.</span><span class="sxs-lookup"><span data-stu-id="61b6c-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="61b6c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61b6c-107">EXAMPLES</span></span>

### <span data-ttu-id="61b6c-108">Przykład 1. Tworzenie filtru wymiaru metrycznego</span><span class="sxs-lookup"><span data-stu-id="61b6c-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="61b6c-109">To polecenie tworzy filtr wymiaru metrycznego w formacie "miasto EQ" Warszawa "lub miasto EQ" Nowy Jork "".</span><span class="sxs-lookup"><span data-stu-id="61b6c-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="61b6c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61b6c-110">PARAMETERS</span></span>

### <span data-ttu-id="61b6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61b6c-111">-DefaultProfile</span></span>
<span data-ttu-id="61b6c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61b6c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61b6c-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="61b6c-113">-Dimension</span></span>
<span data-ttu-id="61b6c-114">Nazwa wymiaru metrycznego.</span><span class="sxs-lookup"><span data-stu-id="61b6c-114">The name of the metric dimension.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61b6c-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="61b6c-115">-Operator</span></span>
<span data-ttu-id="61b6c-116">Umożliwia określenie operatora użytego do wybrania wymiaru metrycznego.</span><span class="sxs-lookup"><span data-stu-id="61b6c-116">Specifies the operator used to select the metric dimension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61b6c-117">-Value</span><span class="sxs-lookup"><span data-stu-id="61b6c-117">-Value</span></span>
<span data-ttu-id="61b6c-118">Określa tablicę wartości wymiaru metrycznego.</span><span class="sxs-lookup"><span data-stu-id="61b6c-118">Specifies the array of metric dimension values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61b6c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b6c-119">CommonParameters</span></span>
<span data-ttu-id="61b6c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61b6c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b6c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61b6c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b6c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61b6c-122">INPUTS</span></span>

### <span data-ttu-id="61b6c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="61b6c-123">System.String</span></span>

### <span data-ttu-id="61b6c-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="61b6c-124">System.String[]</span></span>

## <span data-ttu-id="61b6c-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61b6c-125">OUTPUTS</span></span>

### <span data-ttu-id="61b6c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="61b6c-126">System.String</span></span>

## <span data-ttu-id="61b6c-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61b6c-127">NOTES</span></span>

## <span data-ttu-id="61b6c-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61b6c-128">RELATED LINKS</span></span>

<span data-ttu-id="61b6c-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="61b6c-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

