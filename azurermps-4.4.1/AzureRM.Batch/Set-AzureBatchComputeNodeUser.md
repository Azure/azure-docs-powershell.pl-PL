---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: a5e8fd6e6cfba8832365f385cc90357bac59efb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547027"
---
# <span data-ttu-id="88fa6-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88fa6-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="88fa6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="88fa6-103">Modyfikuje właściwości konta w węźle obliczeniowym partii.</span><span class="sxs-lookup"><span data-stu-id="88fa6-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88fa6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88fa6-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <String> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88fa6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88fa6-105">DESCRIPTION</span></span>
<span data-ttu-id="88fa6-106">Polecenie cmdlet **Set-AzureBatchComputeNodeUser** modyfikuje właściwości konta użytkownika w węźle obliczeniowym funkcji Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="88fa6-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="88fa6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88fa6-107">EXAMPLES</span></span>

### <span data-ttu-id="88fa6-108">Przykład 1: aktualizowanie konta użytkownika</span><span class="sxs-lookup"><span data-stu-id="88fa6-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="88fa6-109">To polecenie modyfikuje konto użytkownika o nazwie PFuller w węźle obliczeniowym o określonym IDENTYFIKATORze w puli o nazwie ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="88fa6-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="88fa6-110">Polecenie zmienia hasło konta i czas wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="88fa6-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="88fa6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88fa6-111">PARAMETERS</span></span>

### <span data-ttu-id="88fa6-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="88fa6-112">-BatchContext</span></span>
<span data-ttu-id="88fa6-113">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="88fa6-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="88fa6-114">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="88fa6-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="88fa6-115">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="88fa6-115">-ComputeNodeId</span></span>
<span data-ttu-id="88fa6-116">Określa identyfikator węzła obliczeniowego, na którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88fa6-116">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="88fa6-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="88fa6-117">-ExpiryTime</span></span>
<span data-ttu-id="88fa6-118">Określa czas wygaśnięcia konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="88fa6-118">Specifies the expiry time for the user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fa6-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88fa6-119">-Name</span></span>
<span data-ttu-id="88fa6-120">Określa nazwę konta użytkownika, które jest modyfikowane przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="88fa6-120">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fa6-121">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="88fa6-121">-Password</span></span>
<span data-ttu-id="88fa6-122">Określa hasło dla konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="88fa6-122">Specifies the password for the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88fa6-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="88fa6-123">-PoolId</span></span>
<span data-ttu-id="88fa6-124">Określa identyfikator puli zawierającej węzeł obliczeniowy, na którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88fa6-124">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="88fa6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88fa6-125">-DefaultProfile</span></span>
<span data-ttu-id="88fa6-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88fa6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88fa6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88fa6-127">CommonParameters</span></span>
<span data-ttu-id="88fa6-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88fa6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88fa6-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88fa6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88fa6-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88fa6-130">INPUTS</span></span>

### <span data-ttu-id="88fa6-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="88fa6-131">BatchAccountContext</span></span>
<span data-ttu-id="88fa6-132">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="88fa6-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="88fa6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88fa6-133">OUTPUTS</span></span>

## <span data-ttu-id="88fa6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88fa6-134">NOTES</span></span>

## <span data-ttu-id="88fa6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88fa6-135">RELATED LINKS</span></span>

[<span data-ttu-id="88fa6-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="88fa6-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="88fa6-137">Nowe — AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88fa6-137">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="88fa6-138">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88fa6-138">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="88fa6-139">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="88fa6-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


