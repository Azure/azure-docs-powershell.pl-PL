---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremoteloginsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: 01ded3d4e9d77edac39e7c632f46d6e7ecf9eeb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527098"
---
# <span data-ttu-id="c8051-101">Get-AzureBatchRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="c8051-101">Get-AzureBatchRemoteLoginSettings</span></span>

## <span data-ttu-id="c8051-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8051-102">SYNOPSIS</span></span>
<span data-ttu-id="c8051-103">Pobiera ustawienia logowania zdalnego dla węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="c8051-103">Gets remote logon settings for a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8051-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8051-104">SYNTAX</span></span>

### <span data-ttu-id="c8051-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c8051-105">Id (Default)</span></span>
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8051-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="c8051-106">InputObject</span></span>
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8051-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c8051-107">DESCRIPTION</span></span>
<span data-ttu-id="c8051-108">Polecenie cmdlet **Get-AzureBatchRemoteLoginSettings** pobiera ustawienia logowania zdalnego dla węzła compute w puli opartej na infrastrukturze maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c8051-108">The **Get-AzureBatchRemoteLoginSettings** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="c8051-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8051-109">EXAMPLES</span></span>

### <span data-ttu-id="c8051-110">Przykład 1: Pobieranie ustawień logowania zdalnego dla wszystkich węzłów w puli</span><span class="sxs-lookup"><span data-stu-id="c8051-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="c8051-111">Pierwsze polecenie pobiera kontekst konta wsadowego zawierający klucze dostępu dla subskrypcji przy użyciu polecenia **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="c8051-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="c8051-112">Polecenie zapisuje kontekst w zmiennej $Context do użycia w następnym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="c8051-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="c8051-113">Drugie polecenie pobiera wszystkie węzły obliczeniowe w puli o IDENTYFIKATORze ContosoPool przy użyciu polecenia **Get-AzureBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="c8051-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzureBatchComputeNode**.</span></span>
<span data-ttu-id="c8051-114">Polecenie przekazuje poszczególne węzły komputerów do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="c8051-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c8051-115">Polecenie pobiera ustawienia logowania zdalnego dla każdego węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="c8051-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="c8051-116">Przykład 2: Pobieranie ustawień logowania zdalnego dla węzła</span><span class="sxs-lookup"><span data-stu-id="c8051-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="c8051-117">Pierwsze polecenie pobiera kontekst konta wsadowego zawierający klucze dostępu dla subskrypcji, a następnie zapisuje go w zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="c8051-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>

<span data-ttu-id="c8051-118">Drugie polecenie pobiera ustawienia logowania zdalnego dla węzła obliczeniowego o określonym IDENTYFIKATORze w puli o IDENTYFIKATORze ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="c8051-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="c8051-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8051-119">PARAMETERS</span></span>

### <span data-ttu-id="c8051-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c8051-120">-BatchContext</span></span>
<span data-ttu-id="c8051-121">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c8051-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c8051-122">Aby uzyskać **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="c8051-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8051-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c8051-123">-ComputeNode</span></span>
<span data-ttu-id="c8051-124">Określa węzeł obliczeniowy jako obiekt **PSComputeNode** , dla którego to polecenie cmdlet uzyskuje ustawienia logowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="c8051-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="c8051-125">Aby uzyskać obiekt węzła obliczeniowego, użyj polecenia cmdlet Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="c8051-125">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8051-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c8051-126">-ComputeNodeId</span></span>
<span data-ttu-id="c8051-127">Określa identyfikator węzła obliczeniowego, dla którego mają być uzyskiwane ustawienia logowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="c8051-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="c8051-128">, dla którego to polecenie cmdlet uzyskuje ustawienia logowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="c8051-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8051-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8051-129">-DefaultProfile</span></span>
<span data-ttu-id="c8051-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8051-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8051-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c8051-131">-PoolId</span></span>
<span data-ttu-id="c8051-132">Określa identyfikator puli zawierającej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="c8051-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8051-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8051-133">CommonParameters</span></span>
<span data-ttu-id="c8051-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8051-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8051-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8051-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8051-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8051-136">INPUTS</span></span>

### <span data-ttu-id="c8051-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c8051-137">BatchAccountContext</span></span>
<span data-ttu-id="c8051-138">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c8051-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c8051-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="c8051-139">PSComputeNode</span></span>
<span data-ttu-id="c8051-140">Parametr "ComputeNode" akceptuje wartość typu "PSComputeNode" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c8051-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="c8051-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8051-141">OUTPUTS</span></span>

### <span data-ttu-id="c8051-142">PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="c8051-142">PSRemoteLoginSettings</span></span>

## <span data-ttu-id="c8051-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8051-143">NOTES</span></span>

## <span data-ttu-id="c8051-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8051-144">RELATED LINKS</span></span>

[<span data-ttu-id="c8051-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c8051-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c8051-146">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c8051-146">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="c8051-147">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="c8051-147">Get-AzureBatchRemoteDesktopProtocolFile</span></span>](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="c8051-148">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c8051-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


