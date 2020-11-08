---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232301"
---
# <span data-ttu-id="6b2e2-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b2e2-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="6b2e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b2e2-102">SYNOPSIS</span></span>
<span data-ttu-id="6b2e2-103">Usuwa konfigurację autoskalowania klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="6b2e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b2e2-104">SYNTAX</span></span>

### <span data-ttu-id="6b2e2-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6b2e2-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b2e2-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b2e2-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b2e2-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b2e2-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b2e2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6b2e2-108">DESCRIPTION</span></span>
<span data-ttu-id="6b2e2-109">Polecenie cmdlet **Remove-AzHDInsightClusterAutoscaleConfiguration** usuwa konfigurację autoskalowania klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="6b2e2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b2e2-110">EXAMPLES</span></span>

### <span data-ttu-id="6b2e2-111">Przykład 1: Usunięcie konfiguracji autoskalowania klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="6b2e2-112">To polecenie powoduje usunięcie konfiguracji autoskalowania klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="6b2e2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b2e2-113">PARAMETERS</span></span>

### <span data-ttu-id="6b2e2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b2e2-114">-AsJob</span></span>
<span data-ttu-id="6b2e2-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6b2e2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b2e2-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="6b2e2-116">-ClusterName</span></span>
<span data-ttu-id="6b2e2-117">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b2e2-118">-DefaultProfile</span></span>
<span data-ttu-id="6b2e2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b2e2-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6b2e2-120">-InputObject</span></span>
<span data-ttu-id="6b2e2-121">Pobiera lub ustawia obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b2e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="6b2e2-123">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2e2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b2e2-124">-ResourceId</span></span>
<span data-ttu-id="6b2e2-125">Pobiera lub ustawia identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2e2-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b2e2-126">-Confirm</span></span>
<span data-ttu-id="6b2e2-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b2e2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b2e2-128">-WhatIf</span></span>
<span data-ttu-id="6b2e2-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b2e2-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b2e2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b2e2-131">CommonParameters</span></span>
<span data-ttu-id="6b2e2-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b2e2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b2e2-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b2e2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b2e2-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b2e2-134">INPUTS</span></span>

### <span data-ttu-id="6b2e2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6b2e2-135">System.String</span></span>

### <span data-ttu-id="6b2e2-136">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6b2e2-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="6b2e2-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b2e2-137">OUTPUTS</span></span>

### <span data-ttu-id="6b2e2-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b2e2-138">System.Boolean</span></span>

## <span data-ttu-id="6b2e2-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b2e2-139">NOTES</span></span>

## <span data-ttu-id="6b2e2-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b2e2-140">RELATED LINKS</span></span>

<span data-ttu-id="6b2e2-141">[Nowe — AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6b2e2-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
