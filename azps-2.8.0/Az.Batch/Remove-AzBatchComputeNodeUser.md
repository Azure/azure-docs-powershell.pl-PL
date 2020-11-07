---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: a57707b10fc103e860fe579e75d7d4ad09cfd0e3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93896993"
---
# <span data-ttu-id="c9977-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c9977-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="c9977-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9977-102">SYNOPSIS</span></span>
<span data-ttu-id="c9977-103">Usuwa konto użytkownika z węzła obliczeniowego partii.</span><span class="sxs-lookup"><span data-stu-id="c9977-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="c9977-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9977-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9977-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c9977-105">DESCRIPTION</span></span>
<span data-ttu-id="c9977-106">Polecenie cmdlet **Remove-AzBatchComputeNodeUser** usuwa konto użytkownika z węzła obliczeniowego usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="c9977-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="c9977-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9977-107">EXAMPLES</span></span>

### <span data-ttu-id="c9977-108">Przykład 1: Usuwanie użytkownika z węzła obliczeniowego bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="c9977-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="c9977-109">To polecenie usuwa użytkownika o nazwie User14 z węzła compute o nazwie ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="c9977-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="c9977-110">Węzeł obliczeniowy znajduje się w puli o nazwie Pool01.</span><span class="sxs-lookup"><span data-stu-id="c9977-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="c9977-111">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="c9977-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c9977-112">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9977-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c9977-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9977-113">PARAMETERS</span></span>

### <span data-ttu-id="c9977-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c9977-114">-BatchContext</span></span>
<span data-ttu-id="c9977-115">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c9977-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c9977-116">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c9977-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c9977-117">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="c9977-117">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c9977-118">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="c9977-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c9977-119">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c9977-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c9977-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c9977-120">-ComputeNodeId</span></span>
<span data-ttu-id="c9977-121">Określa identyfikator węzła obliczeniowego, na którym to polecenie cmdlet usuwa konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c9977-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="c9977-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9977-122">-DefaultProfile</span></span>
<span data-ttu-id="c9977-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9977-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9977-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9977-124">-Name</span></span>
<span data-ttu-id="c9977-125">Określa nazwę konta użytkownika, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="c9977-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="c9977-126">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="c9977-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="c9977-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c9977-127">-PoolId</span></span>
<span data-ttu-id="c9977-128">Określa identyfikator puli zawierającej węzeł obliczeniowy, na którym ma zostać usunięte konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c9977-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="c9977-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9977-129">-Confirm</span></span>
<span data-ttu-id="c9977-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9977-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9977-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9977-131">-WhatIf</span></span>
<span data-ttu-id="c9977-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9977-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9977-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9977-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9977-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9977-134">CommonParameters</span></span>
<span data-ttu-id="c9977-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9977-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9977-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9977-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9977-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9977-137">INPUTS</span></span>

### <span data-ttu-id="c9977-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c9977-138">System.String</span></span>

### <span data-ttu-id="c9977-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c9977-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c9977-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9977-140">OUTPUTS</span></span>

### <span data-ttu-id="c9977-141">System. void</span><span class="sxs-lookup"><span data-stu-id="c9977-141">System.Void</span></span>

## <span data-ttu-id="c9977-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9977-142">NOTES</span></span>

## <span data-ttu-id="c9977-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9977-143">RELATED LINKS</span></span>

[<span data-ttu-id="c9977-144">Nowe — AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c9977-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="c9977-145">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c9977-145">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c9977-146">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c9977-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


