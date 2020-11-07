---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 28b95833e9221e5ecaa05ab33a6e2518c7cca1a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719187"
---
# <span data-ttu-id="31f34-101">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="31f34-101">Set-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="31f34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31f34-102">SYNOPSIS</span></span>
<span data-ttu-id="31f34-103">Ustawia poprzednio wykonaną akcję skryptu, która będzie akcją utrwalonego skryptu.</span><span class="sxs-lookup"><span data-stu-id="31f34-103">Sets a previously executed script action to be a persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31f34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31f34-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31f34-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31f34-105">DESCRIPTION</span></span>
<span data-ttu-id="31f34-106">Polecenie cmdlet **Set-AzureRmHDInsightPersistedScriptAction** ustawia uprzednio wykonaną akcję skryptu, która jest akcją utrwaloną na skrypcie.</span><span class="sxs-lookup"><span data-stu-id="31f34-106">The **Set-AzureRmHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="31f34-107">Określona akcja skryptu musiała już powieść.</span><span class="sxs-lookup"><span data-stu-id="31f34-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="31f34-108">Akcja skryptu zostanie uruchomiona za każdym razem, gdy klaster usługi Azure HDInsight będzie skalowany.</span><span class="sxs-lookup"><span data-stu-id="31f34-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="31f34-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31f34-109">EXAMPLES</span></span>

### <span data-ttu-id="31f34-110">Przykład 1: Konfigurowanie wcześniej poprawnego skryptu, który ma zostać utrwalony, lub uruchamiania w celu skalowania klastra</span><span class="sxs-lookup"><span data-stu-id="31f34-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="31f34-111">To polecenie umożliwia ustawienie trwałej akcji skryptu, która została wykonana wcześniej, jako akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="31f34-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="31f34-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31f34-112">PARAMETERS</span></span>

### <span data-ttu-id="31f34-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="31f34-113">-ClusterName</span></span>
<span data-ttu-id="31f34-114">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="31f34-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="31f34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f34-115">-DefaultProfile</span></span>
<span data-ttu-id="31f34-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="31f34-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31f34-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f34-117">-ResourceGroupName</span></span>
<span data-ttu-id="31f34-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="31f34-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="31f34-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="31f34-119">-ScriptExecutionId</span></span>
<span data-ttu-id="31f34-120">Określa identyfikator wykonywania akcji skryptu, który ma zostać podwyższony do utrwalonego.</span><span class="sxs-lookup"><span data-stu-id="31f34-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="31f34-121">Akcja skryptu musiała się powieść, aby można było ją promować.</span><span class="sxs-lookup"><span data-stu-id="31f34-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="31f34-122">Identyfikator wykonywania akcji skryptu można znaleźć przy użyciu polecenia Get-AzureRmHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="31f34-122">You can find the script action execution ID using Get-AzureRmHDInsightScriptActionHistory.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f34-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f34-123">CommonParameters</span></span>
<span data-ttu-id="31f34-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f34-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f34-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31f34-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f34-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31f34-126">INPUTS</span></span>

### <span data-ttu-id="31f34-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="31f34-127">None</span></span>
<span data-ttu-id="31f34-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="31f34-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31f34-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31f34-129">OUTPUTS</span></span>

### <span data-ttu-id="31f34-130">System. void</span><span class="sxs-lookup"><span data-stu-id="31f34-130">System.Void</span></span>

## <span data-ttu-id="31f34-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31f34-131">NOTES</span></span>

## <span data-ttu-id="31f34-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31f34-132">RELATED LINKS</span></span>

[<span data-ttu-id="31f34-133">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="31f34-133">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="31f34-134">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="31f34-134">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)


