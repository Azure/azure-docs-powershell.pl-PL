---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241426"
---
# <span data-ttu-id="9cb27-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cb27-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="9cb27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cb27-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb27-103">Pobiera konfigurację automatycznego skalowania klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9cb27-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="9cb27-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9cb27-104">SYNTAX</span></span>

### <span data-ttu-id="9cb27-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9cb27-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cb27-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cb27-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9cb27-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cb27-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cb27-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9cb27-108">DESCRIPTION</span></span>
<span data-ttu-id="9cb27-109">Polecenie **cmdlet Get-AzHDInsightClusterAutoscaleConfiguration** pobiera konfigurację automatycznego skalowania klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9cb27-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="9cb27-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9cb27-110">EXAMPLES</span></span>

### <span data-ttu-id="9cb27-111">Przykład 1. Uzyskaj konfigurację automatycznego skalowania klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9cb27-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="9cb27-112">To polecenie pobiera konfigurację automatycznego skalowania klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9cb27-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="9cb27-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cb27-113">PARAMETERS</span></span>

### <span data-ttu-id="9cb27-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9cb27-114">-ClusterName</span></span>
<span data-ttu-id="9cb27-115">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="9cb27-115">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb27-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb27-116">-DefaultProfile</span></span>
<span data-ttu-id="9cb27-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cb27-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb27-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cb27-118">-InputObject</span></span>
<span data-ttu-id="9cb27-119">Pobiera lub ustawia obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="9cb27-119">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb27-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb27-120">-ResourceGroupName</span></span>
<span data-ttu-id="9cb27-121">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9cb27-121">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb27-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cb27-122">-ResourceId</span></span>
<span data-ttu-id="9cb27-123">Pobiera lub ustawia identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="9cb27-123">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb27-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb27-124">CommonParameters</span></span>
<span data-ttu-id="9cb27-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cb27-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb27-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cb27-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb27-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cb27-127">INPUTS</span></span>

### <span data-ttu-id="9cb27-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9cb27-128">System.String</span></span>

### <span data-ttu-id="9cb27-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9cb27-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="9cb27-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cb27-130">OUTPUTS</span></span>

### <span data-ttu-id="9cb27-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="9cb27-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="9cb27-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9cb27-132">NOTES</span></span>

## <span data-ttu-id="9cb27-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cb27-133">RELATED LINKS</span></span>

<span data-ttu-id="9cb27-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9cb27-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
