---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: ec050d4410e50e0838512879856e6534196108af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551099"
---
# <span data-ttu-id="28cad-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="28cad-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="28cad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28cad-102">SYNOPSIS</span></span>
<span data-ttu-id="28cad-103">Usuwa konto użytkownika z węzła obliczeniowego partii.</span><span class="sxs-lookup"><span data-stu-id="28cad-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28cad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28cad-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28cad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="28cad-105">DESCRIPTION</span></span>
<span data-ttu-id="28cad-106">Polecenie cmdlet **Remove-AzureBatchComputeNodeUser** usuwa konto użytkownika z węzła obliczeniowego usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="28cad-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="28cad-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28cad-107">EXAMPLES</span></span>

### <span data-ttu-id="28cad-108">Przykład 1: Usuwanie użytkownika z węzła obliczeniowego bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="28cad-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="28cad-109">To polecenie usuwa użytkownika o nazwie User14 z węzła compute o nazwie ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="28cad-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="28cad-110">Węzeł obliczeniowy znajduje się w puli o nazwie Pool01.</span><span class="sxs-lookup"><span data-stu-id="28cad-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="28cad-111">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="28cad-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="28cad-112">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="28cad-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="28cad-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28cad-113">PARAMETERS</span></span>

### <span data-ttu-id="28cad-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="28cad-114">-BatchContext</span></span>
<span data-ttu-id="28cad-115">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="28cad-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="28cad-116">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="28cad-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="28cad-117">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="28cad-117">-ComputeNodeId</span></span>
<span data-ttu-id="28cad-118">Określa identyfikator węzła obliczeniowego, na którym to polecenie cmdlet usuwa konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="28cad-118">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28cad-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28cad-119">-Name</span></span>
<span data-ttu-id="28cad-120">Określa nazwę konta użytkownika, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="28cad-120">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="28cad-121">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="28cad-121">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28cad-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="28cad-122">-PoolId</span></span>
<span data-ttu-id="28cad-123">Określa identyfikator puli zawierającej węzeł obliczeniowy, na którym ma zostać usunięte konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="28cad-123">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28cad-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28cad-124">-Confirm</span></span>
<span data-ttu-id="28cad-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28cad-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cad-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28cad-126">-WhatIf</span></span>
<span data-ttu-id="28cad-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28cad-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28cad-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28cad-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cad-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cad-129">-DefaultProfile</span></span>
<span data-ttu-id="28cad-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28cad-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28cad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cad-131">CommonParameters</span></span>
<span data-ttu-id="28cad-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28cad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cad-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28cad-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cad-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28cad-134">INPUTS</span></span>

### <span data-ttu-id="28cad-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="28cad-135">BatchAccountContext</span></span>
<span data-ttu-id="28cad-136">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="28cad-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="28cad-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28cad-137">OUTPUTS</span></span>

## <span data-ttu-id="28cad-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28cad-138">NOTES</span></span>

## <span data-ttu-id="28cad-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28cad-139">RELATED LINKS</span></span>

[<span data-ttu-id="28cad-140">Nowe — AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="28cad-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="28cad-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="28cad-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="28cad-142">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="28cad-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


