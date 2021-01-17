---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380639"
---
# <span data-ttu-id="0d2ff-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="0d2ff-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="0d2ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d2ff-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2ff-103">Umożliwia utworzenie filtru wymiaru metrycznego, którego można użyć do zbadania metryk.</span><span class="sxs-lookup"><span data-stu-id="0d2ff-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="0d2ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d2ff-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d2ff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0d2ff-105">DESCRIPTION</span></span>
<span data-ttu-id="0d2ff-106">Polecenie cmdlet **New-AzMetricFilter** umożliwia utworzenie filtru wymiaru metrycznego, którego można użyć do zbadania metryk.</span><span class="sxs-lookup"><span data-stu-id="0d2ff-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="0d2ff-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d2ff-107">EXAMPLES</span></span>

### <span data-ttu-id="0d2ff-108">Przykład 1. Tworzenie filtru wymiaru metrycznego</span><span class="sxs-lookup"><span data-stu-id="0d2ff-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="0d2ff-109">To polecenie tworzy filtr wymiaru metrycznego w formacie "miasto EQ" Warszawa "lub miasto EQ" Nowy Jork "".</span><span class="sxs-lookup"><span data-stu-id="0d2ff-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="0d2ff-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d2ff-110">PARAMETERS</span></span>

### <span data-ttu-id="0d2ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d2ff-111">-DefaultProfile</span></span>
<span data-ttu-id="0d2ff-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d2ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d2ff-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="0d2ff-113">-Dimension</span></span>
<span data-ttu-id="0d2ff-114">Nazwa wymiaru metrycznego.</span><span class="sxs-lookup"><span data-stu-id="0d2ff-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="0d2ff-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="0d2ff-115">-Operator</span></span>
<span data-ttu-id="0d2ff-116">Umożliwia określenie operatora użytego do wybrania wymiaru metrycznego.</span><span class="sxs-lookup"><span data-stu-id="0d2ff-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="0d2ff-117">-Value</span><span class="sxs-lookup"><span data-stu-id="0d2ff-117">-Value</span></span>
<span data-ttu-id="0d2ff-118">Określa tablicę wartości wymiaru metrycznego.</span><span class="sxs-lookup"><span data-stu-id="0d2ff-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="0d2ff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2ff-119">CommonParameters</span></span>
<span data-ttu-id="0d2ff-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d2ff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2ff-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d2ff-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2ff-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d2ff-122">INPUTS</span></span>

### <span data-ttu-id="0d2ff-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0d2ff-123">System.String</span></span>

### <span data-ttu-id="0d2ff-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="0d2ff-124">System.String[]</span></span>

## <span data-ttu-id="0d2ff-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d2ff-125">OUTPUTS</span></span>

### <span data-ttu-id="0d2ff-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0d2ff-126">System.String</span></span>

## <span data-ttu-id="0d2ff-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d2ff-127">NOTES</span></span>

## <span data-ttu-id="0d2ff-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d2ff-128">RELATED LINKS</span></span>

<span data-ttu-id="0d2ff-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="0d2ff-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

