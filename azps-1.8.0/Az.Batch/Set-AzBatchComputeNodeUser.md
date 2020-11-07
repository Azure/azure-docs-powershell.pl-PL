---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: 95530c75575742e848f39861bed1710be75e318c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710794"
---
# <span data-ttu-id="7aeec-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="7aeec-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="7aeec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7aeec-102">SYNOPSIS</span></span>
<span data-ttu-id="7aeec-103">Modyfikuje właściwości konta w węźle obliczeniowym partii.</span><span class="sxs-lookup"><span data-stu-id="7aeec-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="7aeec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7aeec-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7aeec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7aeec-105">DESCRIPTION</span></span>
<span data-ttu-id="7aeec-106">Polecenie cmdlet **Set-AzBatchComputeNodeUser** modyfikuje właściwości konta użytkownika w węźle obliczeniowym funkcji Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="7aeec-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="7aeec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7aeec-107">EXAMPLES</span></span>

### <span data-ttu-id="7aeec-108">Przykład 1: aktualizowanie konta użytkownika</span><span class="sxs-lookup"><span data-stu-id="7aeec-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="7aeec-109">To polecenie modyfikuje konto użytkownika o nazwie PFuller w węźle obliczeniowym o określonym IDENTYFIKATORze w puli o nazwie ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="7aeec-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="7aeec-110">Polecenie zmienia hasło konta i czas wygaśnięcia.</span><span class="sxs-lookup"><span data-stu-id="7aeec-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="7aeec-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7aeec-111">PARAMETERS</span></span>

### <span data-ttu-id="7aeec-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7aeec-112">-BatchContext</span></span>
<span data-ttu-id="7aeec-113">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="7aeec-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7aeec-114">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="7aeec-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7aeec-115">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="7aeec-115">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7aeec-116">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="7aeec-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7aeec-117">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7aeec-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7aeec-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="7aeec-118">-ComputeNodeId</span></span>
<span data-ttu-id="7aeec-119">Określa identyfikator węzła obliczeniowego, na którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7aeec-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7aeec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aeec-120">-DefaultProfile</span></span>
<span data-ttu-id="7aeec-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7aeec-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aeec-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7aeec-122">-ExpiryTime</span></span>
<span data-ttu-id="7aeec-123">Określa czas wygaśnięcia konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7aeec-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="7aeec-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7aeec-124">-Name</span></span>
<span data-ttu-id="7aeec-125">Określa nazwę konta użytkownika, które jest modyfikowane przez to polecenie.</span><span class="sxs-lookup"><span data-stu-id="7aeec-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7aeec-126">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="7aeec-126">-Password</span></span>
<span data-ttu-id="7aeec-127">Określa hasło dla konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7aeec-127">Specifies the password for the user account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aeec-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="7aeec-128">-PoolId</span></span>
<span data-ttu-id="7aeec-129">Określa identyfikator puli zawierającej węzeł obliczeniowy, na którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7aeec-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7aeec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aeec-130">CommonParameters</span></span>
<span data-ttu-id="7aeec-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aeec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aeec-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aeec-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aeec-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7aeec-133">INPUTS</span></span>

### <span data-ttu-id="7aeec-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7aeec-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7aeec-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7aeec-135">OUTPUTS</span></span>

### <span data-ttu-id="7aeec-136">System. void</span><span class="sxs-lookup"><span data-stu-id="7aeec-136">System.Void</span></span>

## <span data-ttu-id="7aeec-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7aeec-137">NOTES</span></span>

## <span data-ttu-id="7aeec-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7aeec-138">RELATED LINKS</span></span>

[<span data-ttu-id="7aeec-139">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7aeec-139">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7aeec-140">Nowe — AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="7aeec-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="7aeec-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="7aeec-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="7aeec-142">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="7aeec-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

