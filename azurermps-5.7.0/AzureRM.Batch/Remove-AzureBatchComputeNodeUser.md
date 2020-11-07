---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 668abe661eebfe600625ea85d5694838ef0e12f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718505"
---
# <span data-ttu-id="36e8b-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="36e8b-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="36e8b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="36e8b-103">Usuwa konto użytkownika z węzła obliczeniowego partii.</span><span class="sxs-lookup"><span data-stu-id="36e8b-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36e8b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36e8b-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36e8b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36e8b-105">DESCRIPTION</span></span>
<span data-ttu-id="36e8b-106">Polecenie cmdlet **Remove-AzureBatchComputeNodeUser** usuwa konto użytkownika z węzła obliczeniowego usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="36e8b-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="36e8b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36e8b-107">EXAMPLES</span></span>

### <span data-ttu-id="36e8b-108">Przykład 1: Usuwanie użytkownika z węzła obliczeniowego bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="36e8b-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="36e8b-109">To polecenie usuwa użytkownika o nazwie User14 z węzła compute o nazwie ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="36e8b-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="36e8b-110">Węzeł obliczeniowy znajduje się w puli o nazwie Pool01.</span><span class="sxs-lookup"><span data-stu-id="36e8b-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="36e8b-111">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="36e8b-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="36e8b-112">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36e8b-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="36e8b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36e8b-113">PARAMETERS</span></span>

### <span data-ttu-id="36e8b-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="36e8b-114">-BatchContext</span></span>
<span data-ttu-id="36e8b-115">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="36e8b-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="36e8b-116">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="36e8b-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="36e8b-117">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="36e8b-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="36e8b-118">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="36e8b-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="36e8b-119">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="36e8b-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="36e8b-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="36e8b-120">-ComputeNodeId</span></span>
<span data-ttu-id="36e8b-121">Określa identyfikator węzła obliczeniowego, na którym to polecenie cmdlet usuwa konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="36e8b-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36e8b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e8b-122">-DefaultProfile</span></span>
<span data-ttu-id="36e8b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36e8b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36e8b-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36e8b-124">-Name</span></span>
<span data-ttu-id="36e8b-125">Określa nazwę konta użytkownika, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="36e8b-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="36e8b-126">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="36e8b-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36e8b-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="36e8b-127">-PoolId</span></span>
<span data-ttu-id="36e8b-128">Określa identyfikator puli zawierającej węzeł obliczeniowy, na którym ma zostać usunięte konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="36e8b-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36e8b-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36e8b-129">-Confirm</span></span>
<span data-ttu-id="36e8b-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36e8b-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e8b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e8b-131">-WhatIf</span></span>
<span data-ttu-id="36e8b-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36e8b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36e8b-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36e8b-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e8b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e8b-134">CommonParameters</span></span>
<span data-ttu-id="36e8b-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e8b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e8b-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36e8b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e8b-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36e8b-137">INPUTS</span></span>

### <span data-ttu-id="36e8b-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="36e8b-138">BatchAccountContext</span></span>
<span data-ttu-id="36e8b-139">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="36e8b-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="36e8b-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36e8b-140">OUTPUTS</span></span>

## <span data-ttu-id="36e8b-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36e8b-141">NOTES</span></span>

## <span data-ttu-id="36e8b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36e8b-142">RELATED LINKS</span></span>

[<span data-ttu-id="36e8b-143">Nowe — AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="36e8b-143">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="36e8b-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="36e8b-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="36e8b-145">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="36e8b-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


