---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 7e24fac68efa4392944179d4a0618c0ad487c03f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552848"
---
# <span data-ttu-id="2dda2-101">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="2dda2-101">Remove-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="2dda2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2dda2-102">SYNOPSIS</span></span>
<span data-ttu-id="2dda2-103">Usuwa akcję trwałego skryptu z klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2dda2-103">Removes an persisted script action from an HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dda2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2dda2-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dda2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2dda2-105">DESCRIPTION</span></span>
<span data-ttu-id="2dda2-106">Polecenie cmdlet **Remove-AzureRmHDInsightPersistedScriptAction** powoduje usunięcie akcji skryptu utrwalonego z listy określonych akcji skryptów usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2dda2-106">The **Remove-AzureRmHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="2dda2-107">Usunięty skrypt nie będzie już wykonywany, gdy klaster będzie skalowany.</span><span class="sxs-lookup"><span data-stu-id="2dda2-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="2dda2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2dda2-108">EXAMPLES</span></span>

### <span data-ttu-id="2dda2-109">Przykład 1: usuwanie akcji skryptu z listy akcji skryptów utrwalonych w klastrze</span><span class="sxs-lookup"><span data-stu-id="2dda2-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="2dda2-110">To polecenie powoduje usunięcie akcji skryptu o nazwie ScriptAction z listy akcji trwałego skryptu w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="2dda2-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="2dda2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2dda2-111">PARAMETERS</span></span>

### <span data-ttu-id="2dda2-112">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="2dda2-112">-ClusterName</span></span>
<span data-ttu-id="2dda2-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="2dda2-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2dda2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dda2-114">-DefaultProfile</span></span>
<span data-ttu-id="2dda2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2dda2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dda2-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2dda2-116">-Name</span></span>
<span data-ttu-id="2dda2-117">Określa nazwę akcji skryptu trwałego, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="2dda2-117">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dda2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dda2-118">-ResourceGroupName</span></span>
<span data-ttu-id="2dda2-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2dda2-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2dda2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dda2-120">CommonParameters</span></span>
<span data-ttu-id="2dda2-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dda2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dda2-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dda2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dda2-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dda2-123">INPUTS</span></span>

### <span data-ttu-id="2dda2-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2dda2-124">None</span></span>

## <span data-ttu-id="2dda2-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2dda2-125">OUTPUTS</span></span>

### <span data-ttu-id="2dda2-126">System. void</span><span class="sxs-lookup"><span data-stu-id="2dda2-126">System.Void</span></span>

## <span data-ttu-id="2dda2-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2dda2-127">NOTES</span></span>

## <span data-ttu-id="2dda2-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dda2-128">RELATED LINKS</span></span>

[<span data-ttu-id="2dda2-129">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="2dda2-129">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="2dda2-130">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="2dda2-130">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


