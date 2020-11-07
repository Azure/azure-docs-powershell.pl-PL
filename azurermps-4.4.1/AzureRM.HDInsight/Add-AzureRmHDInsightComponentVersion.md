---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 774848C9-47A1-4C43-B6FA-B3C0C3C76470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightComponentVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightComponentVersion.md
ms.openlocfilehash: 300244048ae6855c7c621f9950677c985dcb78cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554366"
---
# <span data-ttu-id="da600-101">Add-AzureRmHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="da600-101">Add-AzureRmHDInsightComponentVersion</span></span>

## <span data-ttu-id="da600-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da600-102">SYNOPSIS</span></span>
<span data-ttu-id="da600-103">Dodaje wersję usługi działającej w klastrze do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="da600-103">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da600-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da600-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightComponentVersion [-Config] <AzureHDInsightConfig> [-ComponentName] <String>
 [-ComponentVersion] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da600-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da600-105">DESCRIPTION</span></span>
<span data-ttu-id="da600-106">Polecenie cmdlet Add-AzureRmHDInsightComponentVersion powoduje dodanie wersji dla usługi uruchomionej w klastrze do obiektu konfiguracji usługi Azure HDInsight utworzonego za pomocą New-AzureRmHDInsightClusterConfig polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da600-106">The Add-AzureRmHDInsightComponentVersion cmdlet adds a version for a service running in a cluster to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="da600-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da600-107">EXAMPLES</span></span>

### <span data-ttu-id="da600-108">--------------------------Przykład 1: Dodaj wersję dla usługi Spark do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="da600-108">--------------------------  Example 1: Add a version for Spark to the cluster configuration object.</span></span>  --------------------------
<span data-ttu-id="da600-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="da600-109">@{paragraph=PS C:\\\>}</span></span>







```
PS C:\> # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
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
        #   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightComponentVersion `
                -ComponentName "Spark" `
                -ComponentVersion "2.0" `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="da600-110">To polecenie powoduje dodanie wersji programu Spark do klastra usługi HDInsight o nazwie "Your-Spark-001".</span><span class="sxs-lookup"><span data-stu-id="da600-110">This command adds the version of Spark to the HDInsight cluster named 'your-spark-001'.</span></span>

## <span data-ttu-id="da600-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da600-111">PARAMETERS</span></span>

### <span data-ttu-id="da600-112">-Składnikname</span><span class="sxs-lookup"><span data-stu-id="da600-112">-ComponentName</span></span>
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

### <span data-ttu-id="da600-113">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="da600-113">-ComponentVersion</span></span>
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

### <span data-ttu-id="da600-114">-Config</span><span class="sxs-lookup"><span data-stu-id="da600-114">-Config</span></span>
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

### <span data-ttu-id="da600-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da600-115">-Confirm</span></span>
<span data-ttu-id="da600-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da600-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da600-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da600-117">-WhatIf</span></span>
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

### <span data-ttu-id="da600-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da600-118">-DefaultProfile</span></span>
<span data-ttu-id="da600-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da600-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da600-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da600-120">CommonParameters</span></span>
<span data-ttu-id="da600-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da600-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da600-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da600-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da600-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da600-123">INPUTS</span></span>

### <span data-ttu-id="da600-124">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="da600-124">AzureHDInsightConfig</span></span>
<span data-ttu-id="da600-125">Parametr "config" akceptuje wartość typu "AzureHDInsightConfig" z procesu</span><span class="sxs-lookup"><span data-stu-id="da600-125">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="da600-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da600-126">OUTPUTS</span></span>

### <span data-ttu-id="da600-127">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="da600-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="da600-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da600-128">NOTES</span></span>

## <span data-ttu-id="da600-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da600-129">RELATED LINKS</span></span>
