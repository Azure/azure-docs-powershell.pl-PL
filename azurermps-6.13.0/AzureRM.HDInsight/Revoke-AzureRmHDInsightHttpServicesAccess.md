---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 93024e0719687c10ec07daa7269d742db012abe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552847"
---
# <span data-ttu-id="38b1b-101">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="38b1b-101">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="38b1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="38b1b-103">Wyłącza dostęp HTTP do klastra.</span><span class="sxs-lookup"><span data-stu-id="38b1b-103">Disables HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38b1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38b1b-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38b1b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="38b1b-105">DESCRIPTION</span></span>
<span data-ttu-id="38b1b-106">Polecenie cmdlet **REVOKE-AzureRmHDInsightHttpServicesAccess** wyłącza dostęp HTTP do klastra usługi Azure HDInsight dla usług ODBC, Ambari, Oozie i webHCatalog sieci Web.</span><span class="sxs-lookup"><span data-stu-id="38b1b-106">The **Revoke-AzureRmHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="38b1b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38b1b-107">EXAMPLES</span></span>

### <span data-ttu-id="38b1b-108">Przykład 1: wyłączenie dostępu HTTP do klastra</span><span class="sxs-lookup"><span data-stu-id="38b1b-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="38b1b-109">To polecenie odwołuje dostęp HTTP do klastra o nazwie-hadoop_001.</span><span class="sxs-lookup"><span data-stu-id="38b1b-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="38b1b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38b1b-110">PARAMETERS</span></span>

### <span data-ttu-id="38b1b-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="38b1b-111">-ClusterName</span></span>
<span data-ttu-id="38b1b-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="38b1b-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="38b1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b1b-113">-DefaultProfile</span></span>
<span data-ttu-id="38b1b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="38b1b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38b1b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b1b-115">-ResourceGroupName</span></span>
<span data-ttu-id="38b1b-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="38b1b-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="38b1b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b1b-117">CommonParameters</span></span>
<span data-ttu-id="38b1b-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b1b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b1b-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b1b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b1b-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38b1b-120">INPUTS</span></span>

### <span data-ttu-id="38b1b-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="38b1b-121">None</span></span>

## <span data-ttu-id="38b1b-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38b1b-122">OUTPUTS</span></span>

### <span data-ttu-id="38b1b-123">Microsoft. Azure. Management. HDInsight. MODELES. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="38b1b-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="38b1b-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38b1b-124">NOTES</span></span>

## <span data-ttu-id="38b1b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38b1b-125">RELATED LINKS</span></span>

[<span data-ttu-id="38b1b-126">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="38b1b-126">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](./Grant-AzureRmHDInsightHttpServicesAccess.md)


