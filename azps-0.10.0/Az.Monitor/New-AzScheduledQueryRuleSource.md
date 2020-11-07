---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 0679f4281d9528a7124f4a9a5235d47dd8af107c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891102"
---
# <span data-ttu-id="d2b89-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d2b89-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="d2b89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2b89-102">SYNOPSIS</span></span>
<span data-ttu-id="d2b89-103">Tworzy obiekt typu źródło.</span><span class="sxs-lookup"><span data-stu-id="d2b89-103">Creates an object of type Source</span></span>

## <span data-ttu-id="d2b89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2b89-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2b89-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d2b89-105">DESCRIPTION</span></span>
<span data-ttu-id="d2b89-106">Tworzy obiekt typu źródło.</span><span class="sxs-lookup"><span data-stu-id="d2b89-106">Creates an object of type Source.</span></span>
<span data-ttu-id="d2b89-107">Ten obiekt ma zostać przekazany do polecenia, które tworzy regułę alertu dziennika</span><span class="sxs-lookup"><span data-stu-id="d2b89-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="d2b89-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2b89-108">EXAMPLES</span></span>

### <span data-ttu-id="d2b89-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d2b89-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="d2b89-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2b89-110">PARAMETERS</span></span>

### <span data-ttu-id="d2b89-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="d2b89-111">-AuthorizedResource</span></span>
<span data-ttu-id="d2b89-112">Lista autoryzowanych zasobów dla tego alertu</span><span class="sxs-lookup"><span data-stu-id="d2b89-112">The list of authorized resources for this alert</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b89-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="d2b89-113">-DataSourceId</span></span>
<span data-ttu-id="d2b89-114">Źródło danych, w którym jest tworzony ten alert</span><span class="sxs-lookup"><span data-stu-id="d2b89-114">The data source on which this alert is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2b89-115">-DefaultProfile</span></span>
<span data-ttu-id="d2b89-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2b89-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2b89-117">-Query</span><span class="sxs-lookup"><span data-stu-id="d2b89-117">-Query</span></span>
<span data-ttu-id="d2b89-118">Zapytanie alertu</span><span class="sxs-lookup"><span data-stu-id="d2b89-118">The alert query</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b89-119">-Querytype</span><span class="sxs-lookup"><span data-stu-id="d2b89-119">-QueryType</span></span>
<span data-ttu-id="d2b89-120">Typ zapytania — obecnie obsługiwane wartości: ResultCount</span><span class="sxs-lookup"><span data-stu-id="d2b89-120">Type of Query - currently supported values : ResultCount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b89-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2b89-121">CommonParameters</span></span>
<span data-ttu-id="d2b89-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2b89-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2b89-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2b89-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2b89-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2b89-124">INPUTS</span></span>

### <span data-ttu-id="d2b89-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d2b89-125">None</span></span>

## <span data-ttu-id="d2b89-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2b89-126">OUTPUTS</span></span>

### <span data-ttu-id="d2b89-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d2b89-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="d2b89-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2b89-128">NOTES</span></span>

## <span data-ttu-id="d2b89-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2b89-129">RELATED LINKS</span></span>
