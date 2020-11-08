---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221727"
---
# <span data-ttu-id="62557-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="62557-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="62557-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62557-102">SYNOPSIS</span></span>
<span data-ttu-id="62557-103">Umożliwia monitorowanie w klastrze usługi HDInsight i odpowiednie dzienniki zostaną wysłane do obszaru roboczego monitorowania określonego podczas włączania.</span><span class="sxs-lookup"><span data-stu-id="62557-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="62557-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62557-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62557-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62557-105">DESCRIPTION</span></span>
<span data-ttu-id="62557-106">Polecenie cmdlet **enable-AzHDInsightMonitoring** umożliwia monitorowanie w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="62557-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="62557-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62557-107">EXAMPLES</span></span>

### <span data-ttu-id="62557-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="62557-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="62557-109">Monitorowanie zostanie włączone w klastrze usługi HDInsight, a odpowiednie dzienniki zostaną wysłane do obszaru roboczego Monitorowanie o identyfikatorze 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="62557-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="62557-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="62557-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="62557-111">Monitorowanie zostanie włączone w klastrze usługi HDInsight, a odpowiednie dzienniki zostaną wysłane do obszaru roboczego Monitorowanie o identyfikatorze 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="62557-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="62557-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62557-112">PARAMETERS</span></span>

### <span data-ttu-id="62557-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62557-113">-DefaultProfile</span></span>
<span data-ttu-id="62557-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="62557-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62557-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62557-115">-Name</span></span>
<span data-ttu-id="62557-116">Nazwa klastra do włączenia monitorowania.</span><span class="sxs-lookup"><span data-stu-id="62557-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="62557-117">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="62557-117">-PrimaryKey</span></span>
<span data-ttu-id="62557-118">Klucz podstawowy obszaru roboczego Monitorowanie.</span><span class="sxs-lookup"><span data-stu-id="62557-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="62557-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62557-119">-ResourceGroupName</span></span>
<span data-ttu-id="62557-120">Grupa zasobów klastra.</span><span class="sxs-lookup"><span data-stu-id="62557-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="62557-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="62557-121">-WorkspaceId</span></span>
<span data-ttu-id="62557-122">Identyfikator obszaru roboczego monitorowania.</span><span class="sxs-lookup"><span data-stu-id="62557-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="62557-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62557-123">-Confirm</span></span>
<span data-ttu-id="62557-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62557-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62557-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62557-125">-WhatIf</span></span>
<span data-ttu-id="62557-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62557-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62557-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="62557-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62557-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62557-128">CommonParameters</span></span>
<span data-ttu-id="62557-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62557-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62557-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62557-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62557-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62557-131">INPUTS</span></span>

### <span data-ttu-id="62557-132">System. String</span><span class="sxs-lookup"><span data-stu-id="62557-132">System.String</span></span>

## <span data-ttu-id="62557-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62557-133">OUTPUTS</span></span>

### <span data-ttu-id="62557-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62557-134">System.Boolean</span></span>

## <span data-ttu-id="62557-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62557-135">NOTES</span></span>

## <span data-ttu-id="62557-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62557-136">RELATED LINKS</span></span>
