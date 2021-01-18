---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502171"
---
# <span data-ttu-id="47738-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="47738-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="47738-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47738-102">SYNOPSIS</span></span>
<span data-ttu-id="47738-103">Pobiera ustawienia logowania zdalnego dla węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="47738-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="47738-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47738-104">SYNTAX</span></span>

### <span data-ttu-id="47738-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="47738-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47738-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="47738-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47738-107">Opis</span><span class="sxs-lookup"><span data-stu-id="47738-107">DESCRIPTION</span></span>
<span data-ttu-id="47738-108">Polecenie cmdlet **Get-AzBatchRemoteLoginSetting** pobiera ustawienia logowania zdalnego dla węzła compute w puli opartej na infrastrukturze maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="47738-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="47738-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47738-109">EXAMPLES</span></span>

### <span data-ttu-id="47738-110">Przykład 1: Pobieranie ustawień logowania zdalnego dla wszystkich węzłów w puli</span><span class="sxs-lookup"><span data-stu-id="47738-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="47738-111">Pierwsze polecenie pobiera kontekst konta wsadowego zawierający klucze dostępu dla subskrypcji przy użyciu polecenia **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="47738-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="47738-112">Polecenie zapisuje kontekst w zmiennej $Context do użycia w następnym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="47738-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="47738-113">Drugie polecenie pobiera wszystkie węzły obliczeniowe w puli o IDENTYFIKATORze ContosoPool przy użyciu polecenia **Get-AzBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="47738-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="47738-114">Polecenie przekazuje poszczególne węzły komputerów do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="47738-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="47738-115">Polecenie pobiera ustawienia logowania zdalnego dla każdego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="47738-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="47738-116">Przykład 2: Pobieranie ustawień logowania zdalnego dla węzła</span><span class="sxs-lookup"><span data-stu-id="47738-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="47738-117">Pierwsze polecenie pobiera kontekst konta wsadowego zawierający klucze dostępu dla subskrypcji, a następnie zapisuje go w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="47738-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="47738-118">Drugie polecenie pobiera ustawienia logowania zdalnego dla węzła obliczeniowego o określonym IDENTYFIKATORze w puli o IDENTYFIKATORze ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="47738-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="47738-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47738-119">PARAMETERS</span></span>

### <span data-ttu-id="47738-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="47738-120">-BatchContext</span></span>
<span data-ttu-id="47738-121">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="47738-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="47738-122">Aby uzyskać **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzBatchAccountKey.</span><span class="sxs-lookup"><span data-stu-id="47738-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47738-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="47738-123">-ComputeNode</span></span>
<span data-ttu-id="47738-124">Określa węzeł obliczeniowy jako obiekt **PSComputeNode** , dla którego to polecenie cmdlet uzyskuje ustawienia logowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="47738-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="47738-125">Aby uzyskać obiekt węzła obliczeniowego, użyj polecenia cmdlet Get-AzBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="47738-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47738-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="47738-126">-ComputeNodeId</span></span>
<span data-ttu-id="47738-127">Określa identyfikator węzła obliczeniowego, dla którego mają być uzyskiwane ustawienia logowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="47738-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="47738-128">, dla którego to polecenie cmdlet uzyskuje ustawienia logowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="47738-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47738-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47738-129">-DefaultProfile</span></span>
<span data-ttu-id="47738-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47738-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47738-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="47738-131">-PoolId</span></span>
<span data-ttu-id="47738-132">Określa identyfikator puli zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="47738-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47738-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47738-133">CommonParameters</span></span>
<span data-ttu-id="47738-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47738-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47738-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47738-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47738-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47738-136">INPUTS</span></span>

### <span data-ttu-id="47738-137">Microsoft.Azure.Commands.Batch. Modele. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="47738-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="47738-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="47738-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="47738-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47738-139">OUTPUTS</span></span>

### <span data-ttu-id="47738-140">Microsoft.Azure.Commands.Batch. Modele. PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="47738-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="47738-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47738-141">NOTES</span></span>

## <span data-ttu-id="47738-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47738-142">RELATED LINKS</span></span>

[<span data-ttu-id="47738-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="47738-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="47738-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="47738-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="47738-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="47738-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="47738-146">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="47738-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
