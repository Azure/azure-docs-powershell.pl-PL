---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 32664beb1ffe7600756953294b1ec33f7d1d54ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549759"
---
# <span data-ttu-id="7c621-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7c621-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="7c621-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c621-102">SYNOPSIS</span></span>
<span data-ttu-id="7c621-103">Wyłącza dostęp RDP do klastra systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="7c621-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c621-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c621-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c621-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7c621-105">DESCRIPTION</span></span>
<span data-ttu-id="7c621-106">Polecenie cmdlet **REVOKE-AzureRmHDInsightRdpServicesAccess** wyłącza dostęp do protokołu RDP (Remote Desktop Protocol) do klastra usługi Azure HDInsight opartego na systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="7c621-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7c621-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c621-107">EXAMPLES</span></span>

### <span data-ttu-id="7c621-108">Przykład 1: wyłączanie dostępu RDP do określonego klastra</span><span class="sxs-lookup"><span data-stu-id="7c621-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="7c621-109">To polecenie odwołuje dostęp RDP do klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="7c621-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="7c621-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c621-110">PARAMETERS</span></span>

### <span data-ttu-id="7c621-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="7c621-111">-ClusterName</span></span>
<span data-ttu-id="7c621-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="7c621-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="7c621-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c621-113">-DefaultProfile</span></span>
<span data-ttu-id="7c621-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7c621-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c621-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c621-115">-ResourceGroupName</span></span>
<span data-ttu-id="7c621-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7c621-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7c621-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c621-117">CommonParameters</span></span>
<span data-ttu-id="7c621-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c621-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c621-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c621-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c621-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c621-120">INPUTS</span></span>

### <span data-ttu-id="7c621-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7c621-121">None</span></span>
<span data-ttu-id="7c621-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7c621-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c621-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c621-123">OUTPUTS</span></span>

### <span data-ttu-id="7c621-124">System. void</span><span class="sxs-lookup"><span data-stu-id="7c621-124">System.Void</span></span>

## <span data-ttu-id="7c621-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c621-125">NOTES</span></span>

## <span data-ttu-id="7c621-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c621-126">RELATED LINKS</span></span>

[<span data-ttu-id="7c621-127">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7c621-127">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)


