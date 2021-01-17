---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 344c6fccd0f6c7db26110a94e2cacc53625df3d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489594"
---
# <span data-ttu-id="d16bd-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="d16bd-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="d16bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d16bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d16bd-103">Usuwa akcję trwałego skryptu z klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d16bd-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="d16bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d16bd-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d16bd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d16bd-105">DESCRIPTION</span></span>
<span data-ttu-id="d16bd-106">Polecenie cmdlet **Remove-AzHDInsightPersistedScriptAction** powoduje usunięcie akcji skryptu utrwalonego z listy określonych akcji skryptów usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d16bd-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="d16bd-107">Usunięty skrypt nie będzie już wykonywany, gdy klaster będzie skalowany.</span><span class="sxs-lookup"><span data-stu-id="d16bd-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="d16bd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d16bd-108">EXAMPLES</span></span>

### <span data-ttu-id="d16bd-109">Przykład 1: usuwanie akcji skryptu z listy akcji skryptów utrwalonych w klastrze</span><span class="sxs-lookup"><span data-stu-id="d16bd-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="d16bd-110">To polecenie powoduje usunięcie akcji skryptu o nazwie ScriptAction z listy akcji trwałego skryptu w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="d16bd-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="d16bd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d16bd-111">PARAMETERS</span></span>

### <span data-ttu-id="d16bd-112">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="d16bd-112">-ClusterName</span></span>
<span data-ttu-id="d16bd-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d16bd-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d16bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d16bd-114">-DefaultProfile</span></span>
<span data-ttu-id="d16bd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d16bd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d16bd-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d16bd-116">-Name</span></span>
<span data-ttu-id="d16bd-117">Określa nazwę akcji skryptu trwałego, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="d16bd-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="d16bd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d16bd-118">-ResourceGroupName</span></span>
<span data-ttu-id="d16bd-119">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d16bd-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d16bd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d16bd-120">CommonParameters</span></span>
<span data-ttu-id="d16bd-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d16bd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d16bd-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d16bd-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d16bd-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d16bd-123">INPUTS</span></span>

### <span data-ttu-id="d16bd-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d16bd-124">None</span></span>

## <span data-ttu-id="d16bd-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d16bd-125">OUTPUTS</span></span>

### <span data-ttu-id="d16bd-126">System. void</span><span class="sxs-lookup"><span data-stu-id="d16bd-126">System.Void</span></span>

## <span data-ttu-id="d16bd-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d16bd-127">NOTES</span></span>

## <span data-ttu-id="d16bd-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d16bd-128">RELATED LINKS</span></span>

[<span data-ttu-id="d16bd-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="d16bd-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="d16bd-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="d16bd-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


