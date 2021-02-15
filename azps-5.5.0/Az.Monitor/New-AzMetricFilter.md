---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190114"
---
# <span data-ttu-id="70588-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="70588-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="70588-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70588-102">SYNOPSIS</span></span>
<span data-ttu-id="70588-103">Tworzy filtr wymiarów metrycznych, który może być używany do tworzenia zapytań dotyczących metryk.</span><span class="sxs-lookup"><span data-stu-id="70588-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="70588-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="70588-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70588-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="70588-105">DESCRIPTION</span></span>
<span data-ttu-id="70588-106">Polecenie **cmdlet New-AzMetricFilter** tworzy filtr wymiarowania metryczne, który może być używany do tworzenia zapytań dotyczących metryk.</span><span class="sxs-lookup"><span data-stu-id="70588-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="70588-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="70588-107">EXAMPLES</span></span>

### <span data-ttu-id="70588-108">Przykład 1. Tworzenie filtru wymiarów metrycznych</span><span class="sxs-lookup"><span data-stu-id="70588-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="70588-109">To polecenie tworzy filtr wymiarów metrycznych w formacie "Miasto eq "Seattle" lub Miasto eq 'Nowy Jork".</span><span class="sxs-lookup"><span data-stu-id="70588-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="70588-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70588-110">PARAMETERS</span></span>

### <span data-ttu-id="70588-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70588-111">-DefaultProfile</span></span>
<span data-ttu-id="70588-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="70588-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70588-113">— Wymiar</span><span class="sxs-lookup"><span data-stu-id="70588-113">-Dimension</span></span>
<span data-ttu-id="70588-114">Nazwa wymiaru metryczne.</span><span class="sxs-lookup"><span data-stu-id="70588-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="70588-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="70588-115">-Operator</span></span>
<span data-ttu-id="70588-116">Określa operator używany do wybierania wymiaru metryczne.</span><span class="sxs-lookup"><span data-stu-id="70588-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="70588-117">— Wartość</span><span class="sxs-lookup"><span data-stu-id="70588-117">-Value</span></span>
<span data-ttu-id="70588-118">Określa tablicę wartości wymiarów metrycznych.</span><span class="sxs-lookup"><span data-stu-id="70588-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="70588-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70588-119">CommonParameters</span></span>
<span data-ttu-id="70588-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70588-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70588-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70588-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70588-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70588-122">INPUTS</span></span>

### <span data-ttu-id="70588-123">System.String</span><span class="sxs-lookup"><span data-stu-id="70588-123">System.String</span></span>

### <span data-ttu-id="70588-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="70588-124">System.String[]</span></span>

## <span data-ttu-id="70588-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70588-125">OUTPUTS</span></span>

### <span data-ttu-id="70588-126">System.String</span><span class="sxs-lookup"><span data-stu-id="70588-126">System.String</span></span>

## <span data-ttu-id="70588-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="70588-127">NOTES</span></span>

## <span data-ttu-id="70588-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70588-128">RELATED LINKS</span></span>

<span data-ttu-id="70588-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="70588-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

