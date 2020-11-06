---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 529eedf9cd8ae782d08af7d349d4e11885a8a564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528137"
---
# <span data-ttu-id="d833b-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d833b-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="d833b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d833b-102">SYNOPSIS</span></span>
<span data-ttu-id="d833b-103">Przyznaje dostęp HTTP do klastra.</span><span class="sxs-lookup"><span data-stu-id="d833b-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d833b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d833b-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d833b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d833b-105">DESCRIPTION</span></span>
<span data-ttu-id="d833b-106">Polecenie cmdlet **Grant-AzureRmHDInsightHttpServicesAccess** udziela dostępu HTTP do klastra usługi Azure HDInsight przy użyciu ODBC, Ambari, Oozie i usług sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d833b-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="d833b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d833b-107">EXAMPLES</span></span>

### <span data-ttu-id="d833b-108">Przykład 1: udzielenie dostępu HTTP do klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="d833b-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="d833b-109">To polecenie udziela dostępu HTTP do klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="d833b-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d833b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d833b-110">PARAMETERS</span></span>

### <span data-ttu-id="d833b-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="d833b-111">-ClusterName</span></span>
<span data-ttu-id="d833b-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d833b-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d833b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d833b-113">-DefaultProfile</span></span>
<span data-ttu-id="d833b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d833b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d833b-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d833b-115">-HttpCredential</span></span>
<span data-ttu-id="d833b-116">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="d833b-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d833b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d833b-117">-ResourceGroupName</span></span>
<span data-ttu-id="d833b-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d833b-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d833b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d833b-119">CommonParameters</span></span>
<span data-ttu-id="d833b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d833b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d833b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d833b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d833b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d833b-122">INPUTS</span></span>

### <span data-ttu-id="d833b-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d833b-123">None</span></span>
<span data-ttu-id="d833b-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d833b-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d833b-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d833b-125">OUTPUTS</span></span>

### <span data-ttu-id="d833b-126">Microsoft. Azure. Management. HDInsight. MODELES. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="d833b-126">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="d833b-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d833b-127">NOTES</span></span>

## <span data-ttu-id="d833b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d833b-128">RELATED LINKS</span></span>

[<span data-ttu-id="d833b-129">REVOKE-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d833b-129">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)


