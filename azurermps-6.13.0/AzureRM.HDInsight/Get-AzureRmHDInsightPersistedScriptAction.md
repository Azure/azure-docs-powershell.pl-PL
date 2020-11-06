---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 6305e9a312eb5ebb34de56bcef8a8894b1bd7dd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545295"
---
# <span data-ttu-id="e724d-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e724d-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="e724d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e724d-102">SYNOPSIS</span></span>
<span data-ttu-id="e724d-103">Pobiera akcje trwałego skryptu dla klastra i umieszcza je na liście w kolejności chronologicznej lub pobiera szczegóły określonego działania skryptu trwałego.</span><span class="sxs-lookup"><span data-stu-id="e724d-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e724d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e724d-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e724d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e724d-105">DESCRIPTION</span></span>
<span data-ttu-id="e724d-106">Polecenie cmdlet **Get-AzureRmHDInsightPersistedScriptAction** pobiera utrwalone akcje skryptu dla klastra usługi Azure HDInsight i wyświetla je w porządku chronologicznym lub pobiera szczegóły określonego działania skryptu trwałego.</span><span class="sxs-lookup"><span data-stu-id="e724d-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="e724d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e724d-107">EXAMPLES</span></span>

### <span data-ttu-id="e724d-108">Przykład 1: uzyskiwanie akcji trwałego skryptu w klastrze</span><span class="sxs-lookup"><span data-stu-id="e724d-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="e724d-109">To polecenie pobiera akcje trwałego skryptu w klastrze o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="e724d-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e724d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e724d-110">PARAMETERS</span></span>

### <span data-ttu-id="e724d-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="e724d-111">-ClusterName</span></span>
<span data-ttu-id="e724d-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="e724d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e724d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e724d-113">-DefaultProfile</span></span>
<span data-ttu-id="e724d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e724d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e724d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e724d-115">-Name</span></span>
<span data-ttu-id="e724d-116">Określa nazwę akcji skryptu utrwalonego.</span><span class="sxs-lookup"><span data-stu-id="e724d-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e724d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e724d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e724d-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e724d-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e724d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e724d-119">CommonParameters</span></span>
<span data-ttu-id="e724d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e724d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e724d-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e724d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e724d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e724d-122">INPUTS</span></span>

### <span data-ttu-id="e724d-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e724d-123">None</span></span>

## <span data-ttu-id="e724d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e724d-124">OUTPUTS</span></span>

### <span data-ttu-id="e724d-125">Microsoft. Azure. Commands. HDInsight. models. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="e724d-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="e724d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e724d-126">NOTES</span></span>

## <span data-ttu-id="e724d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e724d-127">RELATED LINKS</span></span>

[<span data-ttu-id="e724d-128">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e724d-128">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="e724d-129">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e724d-129">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


