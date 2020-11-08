---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224345"
---
# <span data-ttu-id="51f85-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="51f85-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="51f85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51f85-102">SYNOPSIS</span></span>
<span data-ttu-id="51f85-103">Umożliwia monitorowanie w klastrze usługi HDInsight i odpowiednie dzienniki zostaną wysłane do obszaru roboczego monitorowania określonego podczas włączania.</span><span class="sxs-lookup"><span data-stu-id="51f85-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="51f85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51f85-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51f85-105">Opis</span><span class="sxs-lookup"><span data-stu-id="51f85-105">DESCRIPTION</span></span>
<span data-ttu-id="51f85-106">Polecenie cmdlet **enable-AzHDInsightMonitoring** umożliwia monitorowanie w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="51f85-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="51f85-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51f85-107">EXAMPLES</span></span>

### <span data-ttu-id="51f85-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51f85-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="51f85-109">Monitorowanie zostanie włączone w klastrze usługi HDInsight, a odpowiednie dzienniki zostaną wysłane do obszaru roboczego Monitorowanie o identyfikatorze 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="51f85-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="51f85-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="51f85-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="51f85-111">Monitorowanie zostanie włączone w klastrze usługi HDInsight, a odpowiednie dzienniki zostaną wysłane do obszaru roboczego Monitorowanie o identyfikatorze 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="51f85-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="51f85-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51f85-112">PARAMETERS</span></span>

### <span data-ttu-id="51f85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f85-113">-DefaultProfile</span></span>
<span data-ttu-id="51f85-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="51f85-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51f85-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51f85-115">-Name</span></span>
<span data-ttu-id="51f85-116">Nazwa klastra do włączenia monitorowania.</span><span class="sxs-lookup"><span data-stu-id="51f85-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="51f85-117">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="51f85-117">-PrimaryKey</span></span>
<span data-ttu-id="51f85-118">Klucz podstawowy obszaru roboczego Monitorowanie.</span><span class="sxs-lookup"><span data-stu-id="51f85-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="51f85-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51f85-119">-ResourceGroupName</span></span>
<span data-ttu-id="51f85-120">Grupa zasobów klastra.</span><span class="sxs-lookup"><span data-stu-id="51f85-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="51f85-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="51f85-121">-WorkspaceId</span></span>
<span data-ttu-id="51f85-122">Identyfikator obszaru roboczego monitorowania.</span><span class="sxs-lookup"><span data-stu-id="51f85-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="51f85-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51f85-123">-Confirm</span></span>
<span data-ttu-id="51f85-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51f85-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51f85-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51f85-125">-WhatIf</span></span>
<span data-ttu-id="51f85-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51f85-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51f85-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="51f85-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51f85-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f85-128">CommonParameters</span></span>
<span data-ttu-id="51f85-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51f85-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f85-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51f85-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f85-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51f85-131">INPUTS</span></span>

### <span data-ttu-id="51f85-132">System. String</span><span class="sxs-lookup"><span data-stu-id="51f85-132">System.String</span></span>

## <span data-ttu-id="51f85-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51f85-133">OUTPUTS</span></span>

### <span data-ttu-id="51f85-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51f85-134">System.Boolean</span></span>

## <span data-ttu-id="51f85-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51f85-135">NOTES</span></span>

## <span data-ttu-id="51f85-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51f85-136">RELATED LINKS</span></span>
