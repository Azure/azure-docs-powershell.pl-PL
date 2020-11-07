---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 6cbe18311f4a14b31bc50f7c0b95266bf99d4a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868255"
---
# <span data-ttu-id="13526-101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="13526-101">Grant-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="13526-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13526-102">SYNOPSIS</span></span>
<span data-ttu-id="13526-103">Udziela dostępu RDP do klastra systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="13526-103">Grants RDP access to the Windows cluster.</span></span>

## <span data-ttu-id="13526-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13526-104">SYNTAX</span></span>

```
Grant-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13526-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13526-105">DESCRIPTION</span></span>
<span data-ttu-id="13526-106">Polecenie cmdlet **Grant-AzHDInsightRdpServicesAccess** umożliwia korzystanie z protokołu RDP (Remote Desktop Protocol) w celu uzyskania dostępu do klastra usługi Azure HDInsight opartego na systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="13526-106">The **Grant-AzHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="13526-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13526-107">EXAMPLES</span></span>

### <span data-ttu-id="13526-108">Przykład 1: udzielanie dostępu RDP do klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="13526-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="13526-109">To polecenie udziela dostępu RDP do klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="13526-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="13526-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13526-110">PARAMETERS</span></span>

### <span data-ttu-id="13526-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="13526-111">-ClusterName</span></span>
<span data-ttu-id="13526-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="13526-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="13526-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13526-113">-DefaultProfile</span></span>
<span data-ttu-id="13526-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="13526-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13526-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="13526-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="13526-116">Określa wygaśnięcie jako obiekt **DateTime** , aby uzyskać dostęp do klastra za pomocą protokołu RDP.</span><span class="sxs-lookup"><span data-stu-id="13526-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="13526-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="13526-117">-RdpCredential</span></span>
<span data-ttu-id="13526-118">Określa poświadczenia protokołu RDP dla klastra.</span><span class="sxs-lookup"><span data-stu-id="13526-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="13526-119">Dotyczy to tylko klastrów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="13526-119">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="13526-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13526-120">-ResourceGroupName</span></span>
<span data-ttu-id="13526-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13526-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="13526-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13526-122">CommonParameters</span></span>
<span data-ttu-id="13526-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13526-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13526-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13526-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13526-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13526-125">INPUTS</span></span>

### <span data-ttu-id="13526-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="13526-126">None</span></span>

## <span data-ttu-id="13526-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13526-127">OUTPUTS</span></span>

### <span data-ttu-id="13526-128">System. void</span><span class="sxs-lookup"><span data-stu-id="13526-128">System.Void</span></span>

## <span data-ttu-id="13526-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13526-129">NOTES</span></span>

## <span data-ttu-id="13526-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13526-130">RELATED LINKS</span></span>

[<span data-ttu-id="13526-131">REVOKE-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="13526-131">Revoke-AzHDInsightRdpServicesAccess</span></span>](./Revoke-AzHDInsightRdpServicesAccess.md)


