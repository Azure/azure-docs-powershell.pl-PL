---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: ddc269d342a6119187ec578e236a30c928d9ea3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868212"
---
# <span data-ttu-id="2e260-101">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2e260-101">Revoke-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="2e260-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e260-102">SYNOPSIS</span></span>
<span data-ttu-id="2e260-103">Wyłącza dostęp HTTP do klastra.</span><span class="sxs-lookup"><span data-stu-id="2e260-103">Disables HTTP access to the cluster.</span></span>

## <span data-ttu-id="2e260-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e260-104">SYNTAX</span></span>

```
Revoke-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e260-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e260-105">DESCRIPTION</span></span>
<span data-ttu-id="2e260-106">Polecenie cmdlet **REVOKE-AzHDInsightHttpServicesAccess** wyłącza dostęp HTTP do klastra usługi Azure HDInsight dla usług ODBC, Ambari, Oozie i webHCatalog sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2e260-106">The **Revoke-AzHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="2e260-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e260-107">EXAMPLES</span></span>

### <span data-ttu-id="2e260-108">Przykład 1: wyłączenie dostępu HTTP do klastra</span><span class="sxs-lookup"><span data-stu-id="2e260-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="2e260-109">To polecenie odwołuje dostęp HTTP do klastra o nazwie-hadoop_001.</span><span class="sxs-lookup"><span data-stu-id="2e260-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="2e260-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e260-110">PARAMETERS</span></span>

### <span data-ttu-id="2e260-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="2e260-111">-ClusterName</span></span>
<span data-ttu-id="2e260-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="2e260-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2e260-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e260-113">-DefaultProfile</span></span>
<span data-ttu-id="2e260-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2e260-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e260-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e260-115">-ResourceGroupName</span></span>
<span data-ttu-id="2e260-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e260-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2e260-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e260-117">CommonParameters</span></span>
<span data-ttu-id="2e260-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e260-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e260-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e260-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e260-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e260-120">INPUTS</span></span>

### <span data-ttu-id="2e260-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2e260-121">None</span></span>

## <span data-ttu-id="2e260-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e260-122">OUTPUTS</span></span>

### <span data-ttu-id="2e260-123">Microsoft. Azure. Management. HDInsight. MODELES. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="2e260-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="2e260-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e260-124">NOTES</span></span>

## <span data-ttu-id="2e260-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e260-125">RELATED LINKS</span></span>

[<span data-ttu-id="2e260-126">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2e260-126">Grant-AzHDInsightHttpServicesAccess</span></span>](./Grant-AzHDInsightHttpServicesAccess.md)


