---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: c531135af3d118a9987a3c328eb4c06847e75fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868259"
---
# <span data-ttu-id="aaf77-101">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="aaf77-101">Grant-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="aaf77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aaf77-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf77-103">Przyznaje dostęp HTTP do klastra.</span><span class="sxs-lookup"><span data-stu-id="aaf77-103">Grants HTTP access to the cluster.</span></span>

## <span data-ttu-id="aaf77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aaf77-104">SYNTAX</span></span>

```
Grant-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaf77-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aaf77-105">DESCRIPTION</span></span>
<span data-ttu-id="aaf77-106">Polecenie cmdlet **Grant-AzHDInsightHttpServicesAccess** udziela dostępu HTTP do klastra usługi Azure HDInsight przy użyciu ODBC, Ambari, Oozie i usług sieci Web.</span><span class="sxs-lookup"><span data-stu-id="aaf77-106">The **Grant-AzHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="aaf77-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aaf77-107">EXAMPLES</span></span>

### <span data-ttu-id="aaf77-108">Przykład 1: udzielenie dostępu HTTP do klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="aaf77-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="aaf77-109">To polecenie udziela dostępu HTTP do klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="aaf77-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="aaf77-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aaf77-110">PARAMETERS</span></span>

### <span data-ttu-id="aaf77-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="aaf77-111">-ClusterName</span></span>
<span data-ttu-id="aaf77-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="aaf77-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf77-113">-DefaultProfile</span></span>
<span data-ttu-id="aaf77-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="aaf77-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaf77-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="aaf77-115">-HttpCredential</span></span>
<span data-ttu-id="aaf77-116">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="aaf77-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf77-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf77-117">-ResourceGroupName</span></span>
<span data-ttu-id="aaf77-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aaf77-118">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf77-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf77-119">CommonParameters</span></span>
<span data-ttu-id="aaf77-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf77-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf77-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaf77-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf77-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aaf77-122">INPUTS</span></span>

### <span data-ttu-id="aaf77-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aaf77-123">None</span></span>

## <span data-ttu-id="aaf77-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aaf77-124">OUTPUTS</span></span>

### <span data-ttu-id="aaf77-125">Microsoft. Azure. Management. HDInsight. MODELES. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="aaf77-125">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="aaf77-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aaf77-126">NOTES</span></span>

## <span data-ttu-id="aaf77-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aaf77-127">RELATED LINKS</span></span>

[<span data-ttu-id="aaf77-128">REVOKE-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="aaf77-128">Revoke-AzHDInsightHttpServicesAccess</span></span>](./Revoke-AzHDInsightHttpServicesAccess.md)


