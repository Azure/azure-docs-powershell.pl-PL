---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: bff21d969a88282f3ba3c1d79d1f717c3c169265
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064088"
---
# <span data-ttu-id="45892-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="45892-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="45892-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45892-102">SYNOPSIS</span></span>
<span data-ttu-id="45892-103">Ustawia poprzednio wykonaną akcję skryptu, która będzie akcją utrwalonego skryptu.</span><span class="sxs-lookup"><span data-stu-id="45892-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="45892-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45892-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45892-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45892-105">DESCRIPTION</span></span>
<span data-ttu-id="45892-106">Polecenie cmdlet **Set-AzHDInsightPersistedScriptAction** ustawia uprzednio wykonaną akcję skryptu, która jest akcją utrwaloną na skrypcie.</span><span class="sxs-lookup"><span data-stu-id="45892-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="45892-107">Określona akcja skryptu musiała już powieść.</span><span class="sxs-lookup"><span data-stu-id="45892-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="45892-108">Akcja skryptu zostanie uruchomiona za każdym razem, gdy klaster usługi Azure HDInsight będzie skalowany.</span><span class="sxs-lookup"><span data-stu-id="45892-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="45892-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45892-109">EXAMPLES</span></span>

### <span data-ttu-id="45892-110">Przykład 1: Konfigurowanie wcześniej poprawnego skryptu, który ma zostać utrwalony, lub uruchamiania w celu skalowania klastra</span><span class="sxs-lookup"><span data-stu-id="45892-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="45892-111">To polecenie umożliwia ustawienie trwałej akcji skryptu, która została wykonana wcześniej, jako akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="45892-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="45892-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45892-112">PARAMETERS</span></span>

### <span data-ttu-id="45892-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="45892-113">-ClusterName</span></span>
<span data-ttu-id="45892-114">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="45892-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="45892-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45892-115">-DefaultProfile</span></span>
<span data-ttu-id="45892-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="45892-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45892-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45892-117">-ResourceGroupName</span></span>
<span data-ttu-id="45892-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="45892-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="45892-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="45892-119">-ScriptExecutionId</span></span>
<span data-ttu-id="45892-120">Określa identyfikator wykonywania akcji skryptu, który ma zostać podwyższony do utrwalonego.</span><span class="sxs-lookup"><span data-stu-id="45892-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="45892-121">Akcja skryptu musiała się powieść, aby można było ją promować.</span><span class="sxs-lookup"><span data-stu-id="45892-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="45892-122">Identyfikator wykonywania akcji skryptu można znaleźć przy użyciu polecenia Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="45892-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45892-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45892-123">CommonParameters</span></span>
<span data-ttu-id="45892-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45892-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45892-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45892-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45892-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45892-126">INPUTS</span></span>

### <span data-ttu-id="45892-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="45892-127">None</span></span>

## <span data-ttu-id="45892-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45892-128">OUTPUTS</span></span>

### <span data-ttu-id="45892-129">System. void</span><span class="sxs-lookup"><span data-stu-id="45892-129">System.Void</span></span>

## <span data-ttu-id="45892-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45892-130">NOTES</span></span>

## <span data-ttu-id="45892-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45892-131">RELATED LINKS</span></span>

[<span data-ttu-id="45892-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="45892-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="45892-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="45892-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


