---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightcomponentversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightComponentVersion.md
ms.openlocfilehash: 868ab69420cac66e911d772f4362e70ec2c03a1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062729"
---
# <span data-ttu-id="01768-101">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="01768-101">Add-AzHDInsightComponentVersion</span></span>

## <span data-ttu-id="01768-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01768-102">SYNOPSIS</span></span>
<span data-ttu-id="01768-103">Dodaje wersję usługi działającej w klastrze do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="01768-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

## <span data-ttu-id="01768-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01768-104">SYNTAX</span></span>

```
Add-AzHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01768-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01768-105">DESCRIPTION</span></span>
<span data-ttu-id="01768-106">Polecenie cmdlet Add-AzHDInsightComponentVersion powoduje dodanie wersji dla usługi uruchomionej w klastrze do obiektu konfiguracji usługi Azure HDInsight utworzonego za pomocą New-AzHDInsightClusterConfig polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01768-106">The Add-AzHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="01768-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01768-107">EXAMPLES</span></span>

### <span data-ttu-id="01768-108">Przykład 1: dodanie wersji dla usługi Spark do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="01768-108">Example 1: Add a version for Spark to the cluster configuration object.</span></span>
```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container001"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-spark-001"
        $clusterCreds = Get-Credential
        $sshClusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightClusterConfig `
            | Add-AzHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer `
                -SshCredential $sshCredentials `
                -Version "3.5"
```

<span data-ttu-id="01768-109">To polecenie powoduje dodanie wersji programu Spark do klastra usługi HDInsight o nazwie "Your-Spark-001".</span><span class="sxs-lookup"><span data-stu-id="01768-109">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="01768-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01768-110">PARAMETERS</span></span>

### <span data-ttu-id="01768-111">-Składnikname</span><span class="sxs-lookup"><span data-stu-id="01768-111">-ComponentName</span></span>
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

### <span data-ttu-id="01768-112">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="01768-112">-ComponentVersion</span></span>
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

### <span data-ttu-id="01768-113">-Config</span><span class="sxs-lookup"><span data-stu-id="01768-113">-Config</span></span>
```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01768-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01768-114">-DefaultProfile</span></span>
<span data-ttu-id="01768-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="01768-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01768-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01768-116">-Confirm</span></span>
<span data-ttu-id="01768-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01768-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01768-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01768-118">-WhatIf</span></span>
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

### <span data-ttu-id="01768-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01768-119">CommonParameters</span></span>
<span data-ttu-id="01768-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01768-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01768-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01768-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01768-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01768-122">INPUTS</span></span>

### <span data-ttu-id="01768-123">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="01768-123">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="01768-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01768-124">OUTPUTS</span></span>

### <span data-ttu-id="01768-125">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="01768-125">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="01768-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01768-126">NOTES</span></span>

## <span data-ttu-id="01768-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01768-127">RELATED LINKS</span></span>
