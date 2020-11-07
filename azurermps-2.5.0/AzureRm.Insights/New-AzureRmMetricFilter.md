---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
ms.openlocfilehash: 42633beddee9e6681e68ce1ba61e71d276abf478
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898478"
---
# <span data-ttu-id="ab9db-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="ab9db-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="ab9db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab9db-102">SYNOPSIS</span></span>
<span data-ttu-id="ab9db-103">Umożliwia utworzenie filtru wymiaru metrycznego, którego można użyć do zbadania metryk.</span><span class="sxs-lookup"><span data-stu-id="ab9db-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab9db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab9db-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab9db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab9db-105">DESCRIPTION</span></span>
<span data-ttu-id="ab9db-106">Polecenie cmdlet **New-AzureRmMetricFilter** umożliwia utworzenie filtru wymiaru metrycznego, którego można użyć do zbadania metryk.</span><span class="sxs-lookup"><span data-stu-id="ab9db-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="ab9db-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab9db-107">EXAMPLES</span></span>

### <span data-ttu-id="ab9db-108">Przykład 1. Tworzenie filtru wymiaru metrycznego</span><span class="sxs-lookup"><span data-stu-id="ab9db-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="ab9db-109">To polecenie tworzy filtr wymiaru metrycznego w formacie "miasto EQ" Warszawa "lub miasto EQ" Nowy Jork "".</span><span class="sxs-lookup"><span data-stu-id="ab9db-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="ab9db-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab9db-110">PARAMETERS</span></span>

### <span data-ttu-id="ab9db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab9db-111">-DefaultProfile</span></span>
<span data-ttu-id="ab9db-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab9db-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab9db-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="ab9db-113">-Dimension</span></span>
<span data-ttu-id="ab9db-114">Nazwa wymiaru metrycznego.</span><span class="sxs-lookup"><span data-stu-id="ab9db-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="ab9db-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="ab9db-115">-Operator</span></span>
<span data-ttu-id="ab9db-116">Umożliwia określenie operatora użytego do wybrania wymiaru metrycznego.</span><span class="sxs-lookup"><span data-stu-id="ab9db-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="ab9db-117">-Value</span><span class="sxs-lookup"><span data-stu-id="ab9db-117">-Value</span></span>
<span data-ttu-id="ab9db-118">Określa tablicę wartości wymiaru metrycznego.</span><span class="sxs-lookup"><span data-stu-id="ab9db-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="ab9db-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab9db-119">CommonParameters</span></span>
<span data-ttu-id="ab9db-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab9db-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab9db-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab9db-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab9db-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab9db-122">INPUTS</span></span>

### <span data-ttu-id="ab9db-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ab9db-123">System.String</span></span>

### <span data-ttu-id="ab9db-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="ab9db-124">System.String[]</span></span>

## <span data-ttu-id="ab9db-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab9db-125">OUTPUTS</span></span>

### <span data-ttu-id="ab9db-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ab9db-126">System.String</span></span>

## <span data-ttu-id="ab9db-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab9db-127">NOTES</span></span>

## <span data-ttu-id="ab9db-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab9db-128">RELATED LINKS</span></span>

<span data-ttu-id="ab9db-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="ab9db-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

