---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: ce169dc1cce1552b48aa864885c6877624da0176
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543839"
---
# <span data-ttu-id="0081d-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0081d-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="0081d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0081d-102">SYNOPSIS</span></span>
<span data-ttu-id="0081d-103">Udziela dostępu RDP do klastra systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="0081d-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0081d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0081d-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0081d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0081d-105">DESCRIPTION</span></span>
<span data-ttu-id="0081d-106">Polecenie cmdlet **Grant-AzureRmHDInsightRdpServicesAccess** umożliwia korzystanie z protokołu RDP (Remote Desktop Protocol) w celu uzyskania dostępu do klastra usługi Azure HDInsight opartego na systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="0081d-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="0081d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0081d-107">EXAMPLES</span></span>

### <span data-ttu-id="0081d-108">Przykład 1: udzielanie dostępu RDP do klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="0081d-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="0081d-109">To polecenie udziela dostępu RDP do klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="0081d-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0081d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0081d-110">PARAMETERS</span></span>

### <span data-ttu-id="0081d-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="0081d-111">-ClusterName</span></span>
<span data-ttu-id="0081d-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="0081d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0081d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0081d-113">-DefaultProfile</span></span>
<span data-ttu-id="0081d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0081d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0081d-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="0081d-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="0081d-116">Określa wygaśnięcie jako obiekt **DateTime** , aby uzyskać dostęp do klastra za pomocą protokołu RDP.</span><span class="sxs-lookup"><span data-stu-id="0081d-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0081d-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="0081d-117">-RdpCredential</span></span>
<span data-ttu-id="0081d-118">Określa poświadczenia protokołu RDP dla klastra.</span><span class="sxs-lookup"><span data-stu-id="0081d-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="0081d-119">Dotyczy to tylko klastrów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="0081d-119">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="0081d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0081d-120">-ResourceGroupName</span></span>
<span data-ttu-id="0081d-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0081d-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0081d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0081d-122">CommonParameters</span></span>
<span data-ttu-id="0081d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0081d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0081d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0081d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0081d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0081d-125">INPUTS</span></span>

### <span data-ttu-id="0081d-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0081d-126">None</span></span>

## <span data-ttu-id="0081d-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0081d-127">OUTPUTS</span></span>

### <span data-ttu-id="0081d-128">System. void</span><span class="sxs-lookup"><span data-stu-id="0081d-128">System.Void</span></span>

## <span data-ttu-id="0081d-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0081d-129">NOTES</span></span>

## <span data-ttu-id="0081d-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0081d-130">RELATED LINKS</span></span>

[<span data-ttu-id="0081d-131">REVOKE-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0081d-131">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


