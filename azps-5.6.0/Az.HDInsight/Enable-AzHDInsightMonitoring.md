---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: dc9e19c35f43b2420213d21b427d2aff69bb2541
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995541"
---
# <span data-ttu-id="ade88-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="ade88-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="ade88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ade88-102">SYNOPSIS</span></span>
<span data-ttu-id="ade88-103">Umożliwia monitorowanie w klastrze HDInsight, a odpowiednie dzienniki będą wysyłane do obszaru roboczego monitorowania określonego podczas włączania.</span><span class="sxs-lookup"><span data-stu-id="ade88-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="ade88-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ade88-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ade88-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ade88-105">DESCRIPTION</span></span>
<span data-ttu-id="ade88-106">Polecenie **cmdlet Enable-AzHDInsightMonitoring** umożliwia monitorowanie w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ade88-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ade88-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ade88-107">EXAMPLES</span></span>

### <span data-ttu-id="ade88-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ade88-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="ade88-109">Monitorowanie zostanie włączone w klastrze HDInsight, a odpowiednie dzienniki będą wysyłane do obszaru roboczego monitorowania o identyfikatorze 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="ade88-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="ade88-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ade88-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="ade88-111">Monitorowanie zostanie włączone w klastrze HDInsight, a odpowiednie dzienniki będą wysyłane do obszaru roboczego monitorowania o identyfikatorze 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="ade88-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="ade88-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ade88-112">PARAMETERS</span></span>

### <span data-ttu-id="ade88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade88-113">-DefaultProfile</span></span>
<span data-ttu-id="ade88-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ade88-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ade88-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ade88-115">-Name</span></span>
<span data-ttu-id="ade88-116">Nazwa klastra umożliwiającego monitorowanie.</span><span class="sxs-lookup"><span data-stu-id="ade88-116">The name of the cluster to enable monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade88-117">- Klucz Podstawowy</span><span class="sxs-lookup"><span data-stu-id="ade88-117">-PrimaryKey</span></span>
<span data-ttu-id="ade88-118">Klucz podstawowy obszaru roboczego monitorowania.</span><span class="sxs-lookup"><span data-stu-id="ade88-118">The primary key of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade88-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade88-119">-ResourceGroupName</span></span>
<span data-ttu-id="ade88-120">Grupa zasobów klastru.</span><span class="sxs-lookup"><span data-stu-id="ade88-120">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade88-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="ade88-121">-WorkspaceId</span></span>
<span data-ttu-id="ade88-122">Identyfikator obszaru roboczego monitorowania.</span><span class="sxs-lookup"><span data-stu-id="ade88-122">The id of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade88-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ade88-123">-Confirm</span></span>
<span data-ttu-id="ade88-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ade88-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade88-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade88-125">-WhatIf</span></span>
<span data-ttu-id="ade88-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ade88-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ade88-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ade88-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade88-128">CommonParameters</span></span>
<span data-ttu-id="ade88-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade88-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ade88-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade88-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ade88-131">INPUTS</span></span>

### <span data-ttu-id="ade88-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ade88-132">System.String</span></span>

## <span data-ttu-id="ade88-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ade88-133">OUTPUTS</span></span>

### <span data-ttu-id="ade88-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ade88-134">System.Boolean</span></span>

## <span data-ttu-id="ade88-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ade88-135">NOTES</span></span>

## <span data-ttu-id="ade88-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ade88-136">RELATED LINKS</span></span>
