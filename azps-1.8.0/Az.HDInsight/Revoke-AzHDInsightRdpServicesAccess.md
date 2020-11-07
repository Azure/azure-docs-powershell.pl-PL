---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 7f5fcb8dcfbb325b8bc0381b3c943e550fe27e62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868211"
---
# <span data-ttu-id="41344-101">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="41344-101">Revoke-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="41344-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41344-102">SYNOPSIS</span></span>
<span data-ttu-id="41344-103">Wyłącza dostęp RDP do klastra systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="41344-103">Disables RDP access to a Windows cluster.</span></span>

## <span data-ttu-id="41344-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41344-104">SYNTAX</span></span>

```
Revoke-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41344-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41344-105">DESCRIPTION</span></span>
<span data-ttu-id="41344-106">Polecenie cmdlet **REVOKE-AzHDInsightRdpServicesAccess** wyłącza dostęp do protokołu RDP (Remote Desktop Protocol) do klastra usługi Azure HDInsight opartego na systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="41344-106">The **Revoke-AzHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="41344-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41344-107">EXAMPLES</span></span>

### <span data-ttu-id="41344-108">Przykład 1: wyłączanie dostępu RDP do określonego klastra</span><span class="sxs-lookup"><span data-stu-id="41344-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="41344-109">To polecenie odwołuje dostęp RDP do klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="41344-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="41344-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41344-110">PARAMETERS</span></span>

### <span data-ttu-id="41344-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="41344-111">-ClusterName</span></span>
<span data-ttu-id="41344-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="41344-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="41344-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41344-113">-DefaultProfile</span></span>
<span data-ttu-id="41344-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="41344-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41344-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41344-115">-ResourceGroupName</span></span>
<span data-ttu-id="41344-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="41344-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="41344-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41344-117">CommonParameters</span></span>
<span data-ttu-id="41344-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41344-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41344-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41344-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41344-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41344-120">INPUTS</span></span>

### <span data-ttu-id="41344-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="41344-121">None</span></span>

## <span data-ttu-id="41344-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41344-122">OUTPUTS</span></span>

### <span data-ttu-id="41344-123">System. void</span><span class="sxs-lookup"><span data-stu-id="41344-123">System.Void</span></span>

## <span data-ttu-id="41344-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41344-124">NOTES</span></span>

## <span data-ttu-id="41344-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41344-125">RELATED LINKS</span></span>

[<span data-ttu-id="41344-126">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="41344-126">Grant-AzHDInsightRdpServicesAccess</span></span>](./Grant-AzHDInsightRdpServicesAccess.md)


