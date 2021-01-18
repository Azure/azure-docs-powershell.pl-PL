---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500996"
---
# <span data-ttu-id="354d0-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="354d0-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="354d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="354d0-102">SYNOPSIS</span></span>
<span data-ttu-id="354d0-103">Pobiera konfigurację autoskalowania klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="354d0-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="354d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="354d0-104">SYNTAX</span></span>

### <span data-ttu-id="354d0-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="354d0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="354d0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="354d0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="354d0-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="354d0-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="354d0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="354d0-108">DESCRIPTION</span></span>
<span data-ttu-id="354d0-109">Polecenie cmdlet **Get-AzHDInsightClusterAutoscaleConfiguration** Pobiera konfigurację autoskalowania klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="354d0-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="354d0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="354d0-110">EXAMPLES</span></span>

### <span data-ttu-id="354d0-111">Przykład 1: Uzyskiwanie konfiguracji autoskalowania klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="354d0-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="354d0-112">To polecenie uzyskuje konfigurację autoskalowania klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="354d0-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="354d0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="354d0-113">PARAMETERS</span></span>

### <span data-ttu-id="354d0-114">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="354d0-114">-ClusterName</span></span>
<span data-ttu-id="354d0-115">Pobiera lub ustawia nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="354d0-115">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="354d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354d0-116">-DefaultProfile</span></span>
<span data-ttu-id="354d0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="354d0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="354d0-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="354d0-118">-InputObject</span></span>
<span data-ttu-id="354d0-119">Pobiera lub ustawia obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="354d0-119">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="354d0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="354d0-120">-ResourceGroupName</span></span>
<span data-ttu-id="354d0-121">Pobiera lub ustawia nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="354d0-121">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="354d0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="354d0-122">-ResourceId</span></span>
<span data-ttu-id="354d0-123">Pobiera lub ustawia identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="354d0-123">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="354d0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354d0-124">CommonParameters</span></span>
<span data-ttu-id="354d0-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="354d0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354d0-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="354d0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354d0-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="354d0-127">INPUTS</span></span>

### <span data-ttu-id="354d0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="354d0-128">System.String</span></span>

### <span data-ttu-id="354d0-129">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="354d0-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="354d0-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="354d0-130">OUTPUTS</span></span>

### <span data-ttu-id="354d0-131">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="354d0-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="354d0-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="354d0-132">NOTES</span></span>

## <span data-ttu-id="354d0-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="354d0-133">RELATED LINKS</span></span>

<span data-ttu-id="354d0-134">[Nowe — AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="354d0-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
