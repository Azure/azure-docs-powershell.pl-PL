---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: 4e0b5fda29696fb45515c3b478b9dc29ff67263e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237749"
---
# <span data-ttu-id="65d3e-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="65d3e-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="65d3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="65d3e-103">Powoduje ponowne uruchomienie określonych hostów klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="65d3e-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="65d3e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="65d3e-104">SYNTAX</span></span>

### <span data-ttu-id="65d3e-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="65d3e-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d3e-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="65d3e-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65d3e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="65d3e-107">DESCRIPTION</span></span>
<span data-ttu-id="65d3e-108">To **polecenie cmdlet Restart-AzHDInsightHost** powoduje ponowne uruchomienie określonych hostów klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="65d3e-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="65d3e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="65d3e-109">EXAMPLES</span></span>

### <span data-ttu-id="65d3e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65d3e-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="65d3e-111">To polecenie powoduje ponowne uruchomienie dwóch hostów klastra: worknode1 i worknode2.</span><span class="sxs-lookup"><span data-stu-id="65d3e-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="65d3e-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="65d3e-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="65d3e-113">To polecenie pokazuje, jak współpracować przy użyciu polecenia cmdlet "Get-AzHDInsightHost".</span><span class="sxs-lookup"><span data-stu-id="65d3e-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="65d3e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65d3e-114">PARAMETERS</span></span>

### <span data-ttu-id="65d3e-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="65d3e-115">-AsJob</span></span>
<span data-ttu-id="65d3e-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="65d3e-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d3e-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="65d3e-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="65d3e-118">Pobiera lub ustawia nazwę hosta.</span><span class="sxs-lookup"><span data-stu-id="65d3e-118">Gets or sets the name of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]
Parameter Sets: SetByAzureHDInsightHostInfoParameterSet
Aliases: Host

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65d3e-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="65d3e-119">-ClusterName</span></span>
<span data-ttu-id="65d3e-120">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="65d3e-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="65d3e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d3e-121">-DefaultProfile</span></span>
<span data-ttu-id="65d3e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="65d3e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d3e-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="65d3e-123">-Name</span></span>
<span data-ttu-id="65d3e-124">Pobiera lub ustawia nazwę hosta.</span><span class="sxs-lookup"><span data-stu-id="65d3e-124">Gets or sets the name of the host.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByNameParameterSet
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65d3e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65d3e-125">-PassThru</span></span>
<span data-ttu-id="65d3e-126">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="65d3e-126">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d3e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d3e-127">-ResourceGroupName</span></span>
<span data-ttu-id="65d3e-128">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="65d3e-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d3e-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65d3e-129">-Confirm</span></span>
<span data-ttu-id="65d3e-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="65d3e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d3e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d3e-131">-WhatIf</span></span>
<span data-ttu-id="65d3e-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65d3e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d3e-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="65d3e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d3e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d3e-134">CommonParameters</span></span>
<span data-ttu-id="65d3e-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65d3e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d3e-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65d3e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d3e-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65d3e-137">INPUTS</span></span>

### <span data-ttu-id="65d3e-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="65d3e-138">System.String[]</span></span>

### <span data-ttu-id="65d3e-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span><span class="sxs-lookup"><span data-stu-id="65d3e-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span></span>

## <span data-ttu-id="65d3e-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="65d3e-140">OUTPUTS</span></span>

### <span data-ttu-id="65d3e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65d3e-141">System.Boolean</span></span>

## <span data-ttu-id="65d3e-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="65d3e-142">NOTES</span></span>

## <span data-ttu-id="65d3e-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65d3e-143">RELATED LINKS</span></span>
