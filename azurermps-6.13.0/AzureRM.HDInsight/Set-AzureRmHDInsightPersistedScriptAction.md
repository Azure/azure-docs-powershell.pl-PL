---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 07f501be4ac775a9d80c43173e13fccf3057cc26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527950"
---
# <span data-ttu-id="6d2f0-101">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="6d2f0-101">Set-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="6d2f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d2f0-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2f0-103">Ustawia poprzednio wykonaną akcję skryptu, która będzie akcją utrwalonego skryptu.</span><span class="sxs-lookup"><span data-stu-id="6d2f0-103">Sets a previously executed script action to be a persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d2f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d2f0-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d2f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d2f0-105">DESCRIPTION</span></span>
<span data-ttu-id="6d2f0-106">Polecenie cmdlet **Set-AzureRmHDInsightPersistedScriptAction** ustawia uprzednio wykonaną akcję skryptu, która jest akcją utrwaloną na skrypcie.</span><span class="sxs-lookup"><span data-stu-id="6d2f0-106">The **Set-AzureRmHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="6d2f0-107">Określona akcja skryptu musiała już powieść.</span><span class="sxs-lookup"><span data-stu-id="6d2f0-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="6d2f0-108">Akcja skryptu zostanie uruchomiona za każdym razem, gdy klaster usługi Azure HDInsight będzie skalowany.</span><span class="sxs-lookup"><span data-stu-id="6d2f0-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="6d2f0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d2f0-109">EXAMPLES</span></span>

### <span data-ttu-id="6d2f0-110">Przykład 1: Konfigurowanie wcześniej poprawnego skryptu, który ma zostać utrwalony, lub uruchamiania w celu skalowania klastra</span><span class="sxs-lookup"><span data-stu-id="6d2f0-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="6d2f0-111">To polecenie umożliwia ustawienie trwałej akcji skryptu, która została wykonana wcześniej, jako akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="6d2f0-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="6d2f0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d2f0-112">PARAMETERS</span></span>

### <span data-ttu-id="6d2f0-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="6d2f0-113">-ClusterName</span></span>
<span data-ttu-id="6d2f0-114">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="6d2f0-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6d2f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d2f0-115">-DefaultProfile</span></span>
<span data-ttu-id="6d2f0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6d2f0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d2f0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d2f0-117">-ResourceGroupName</span></span>
<span data-ttu-id="6d2f0-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d2f0-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6d2f0-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="6d2f0-119">-ScriptExecutionId</span></span>
<span data-ttu-id="6d2f0-120">Określa identyfikator wykonywania akcji skryptu, który ma zostać podwyższony do utrwalonego.</span><span class="sxs-lookup"><span data-stu-id="6d2f0-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="6d2f0-121">Akcja skryptu musiała się powieść, aby można było ją promować.</span><span class="sxs-lookup"><span data-stu-id="6d2f0-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="6d2f0-122">Identyfikator wykonywania akcji skryptu można znaleźć przy użyciu polecenia Get-AzureRmHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="6d2f0-122">You can find the script action execution ID using Get-AzureRmHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="6d2f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2f0-123">CommonParameters</span></span>
<span data-ttu-id="6d2f0-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d2f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2f0-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d2f0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2f0-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d2f0-126">INPUTS</span></span>

### <span data-ttu-id="6d2f0-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6d2f0-127">None</span></span>

## <span data-ttu-id="6d2f0-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d2f0-128">OUTPUTS</span></span>

### <span data-ttu-id="6d2f0-129">System. void</span><span class="sxs-lookup"><span data-stu-id="6d2f0-129">System.Void</span></span>

## <span data-ttu-id="6d2f0-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d2f0-130">NOTES</span></span>

## <span data-ttu-id="6d2f0-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d2f0-131">RELATED LINKS</span></span>

[<span data-ttu-id="6d2f0-132">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="6d2f0-132">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="6d2f0-133">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="6d2f0-133">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)


