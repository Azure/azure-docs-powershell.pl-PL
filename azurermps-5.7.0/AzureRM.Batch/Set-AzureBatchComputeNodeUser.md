---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6fb398e44b2e6de8a0d00e9a8d737916fafa2472
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719191"
---
# <span data-ttu-id="c397a-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c397a-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="c397a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c397a-102">SYNOPSIS</span></span>
<span data-ttu-id="c397a-103">Modyfikuje właściwości konta w węźle obliczeniowym partii.</span><span class="sxs-lookup"><span data-stu-id="c397a-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c397a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c397a-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c397a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c397a-105">DESCRIPTION</span></span>
<span data-ttu-id="c397a-106">Polecenie cmdlet **Set-AzureBatchComputeNodeUser** modyfikuje właściwości konta użytkownika w węźle obliczeniowym funkcji Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="c397a-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="c397a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c397a-107">EXAMPLES</span></span>

### <span data-ttu-id="c397a-108">Przykład 1: aktualizowanie konta użytkownika</span><span class="sxs-lookup"><span data-stu-id="c397a-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="c397a-109">To polecenie modyfikuje konto użytkownika o nazwie PFuller w węźle obliczeniowym o określonym IDENTYFIKATORze w puli o nazwie ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="c397a-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="c397a-110">Polecenie zmienia hasło konta i czas wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="c397a-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="c397a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c397a-111">PARAMETERS</span></span>

### <span data-ttu-id="c397a-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c397a-112">-BatchContext</span></span>
<span data-ttu-id="c397a-113">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c397a-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c397a-114">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c397a-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c397a-115">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="c397a-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c397a-116">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="c397a-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c397a-117">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c397a-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c397a-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c397a-118">-ComputeNodeId</span></span>
<span data-ttu-id="c397a-119">Określa identyfikator węzła obliczeniowego, na którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c397a-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c397a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c397a-120">-DefaultProfile</span></span>
<span data-ttu-id="c397a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c397a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c397a-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c397a-122">-ExpiryTime</span></span>
<span data-ttu-id="c397a-123">Określa czas wygaśnięcia konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c397a-123">Specifies the expiry time for the user account.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c397a-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c397a-124">-Name</span></span>
<span data-ttu-id="c397a-125">Określa nazwę konta użytkownika, które jest modyfikowane przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="c397a-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c397a-126">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="c397a-126">-Password</span></span>
<span data-ttu-id="c397a-127">Określa hasło dla konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c397a-127">Specifies the password for the user account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c397a-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c397a-128">-PoolId</span></span>
<span data-ttu-id="c397a-129">Określa identyfikator puli zawierającej węzeł obliczeniowy, na którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c397a-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c397a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c397a-130">CommonParameters</span></span>
<span data-ttu-id="c397a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c397a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c397a-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c397a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c397a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c397a-133">INPUTS</span></span>

### <span data-ttu-id="c397a-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c397a-134">BatchAccountContext</span></span>
<span data-ttu-id="c397a-135">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c397a-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="c397a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c397a-136">OUTPUTS</span></span>

## <span data-ttu-id="c397a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c397a-137">NOTES</span></span>

## <span data-ttu-id="c397a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c397a-138">RELATED LINKS</span></span>

[<span data-ttu-id="c397a-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c397a-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c397a-140">Nowe — AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c397a-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="c397a-141">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c397a-141">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="c397a-142">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c397a-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


