---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: aaf020d61941057dd0dabac849adb37197e02882
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987008"
---
# <span data-ttu-id="35340-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="35340-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="35340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35340-102">SYNOPSIS</span></span>
<span data-ttu-id="35340-103">Tworzy konto użytkownika w węźle obliczania partii.</span><span class="sxs-lookup"><span data-stu-id="35340-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="35340-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35340-104">SYNTAX</span></span>

### <span data-ttu-id="35340-105">Identyfikator</span><span class="sxs-lookup"><span data-stu-id="35340-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35340-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="35340-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35340-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="35340-107">DESCRIPTION</span></span>
<span data-ttu-id="35340-108">Polecenie **cmdlet New-AzBatchComputeNodeUser** tworzy konto użytkownika w węźle obliczeniowym partii platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="35340-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="35340-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35340-109">EXAMPLES</span></span>

### <span data-ttu-id="35340-110">Przykład 1. Tworzenie konta użytkownika z poświadczeniami administracyjnymi</span><span class="sxs-lookup"><span data-stu-id="35340-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="35340-111">To polecenie tworzy konto użytkownika w węźle obliczeniowym o identyfikatorze ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="35340-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="35340-112">Węzeł znajduje się w puli o identyfikatorze MyPool01.</span><span class="sxs-lookup"><span data-stu-id="35340-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="35340-113">Nazwa użytkownika to TestUser, hasło to Hasło, konto wygasa za siedem dni, a konto ma poświadczenia administracyjne.</span><span class="sxs-lookup"><span data-stu-id="35340-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="35340-114">Przykład 2. Tworzenie konta użytkownika w węźle obliczeniowym przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="35340-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="35340-115">To polecenie pobiera węzeł obliczeniowy o nazwie ComputeNode01 przy użyciu polecenia cmdlet **Get-AzBatchComputeNode.**</span><span class="sxs-lookup"><span data-stu-id="35340-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="35340-116">Ten węzeł znajduje się w puli o identyfikatorze MyPool01.</span><span class="sxs-lookup"><span data-stu-id="35340-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="35340-117">Polecenie przekazuje węzeł obliczeniowy do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="35340-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="35340-118">To polecenie tworzy konto użytkownika, które ma nazwę użytkownika TestUser i hasło hasło.</span><span class="sxs-lookup"><span data-stu-id="35340-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="35340-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35340-119">PARAMETERS</span></span>

### <span data-ttu-id="35340-120">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="35340-120">-BatchContext</span></span>
<span data-ttu-id="35340-121">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="35340-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="35340-122">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="35340-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="35340-123">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="35340-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="35340-124">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="35340-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="35340-125">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="35340-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="35340-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="35340-126">-ComputeNode</span></span>
<span data-ttu-id="35340-127">Określa węzeł obliczeniowy jako **obiekt PSComputeNode,** na którym to polecenie cmdlet tworzy konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="35340-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35340-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="35340-128">-ComputeNodeId</span></span>
<span data-ttu-id="35340-129">Określa identyfikator węzła obliczeniowego, w którym to polecenie cmdlet tworzy konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="35340-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="35340-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35340-130">-DefaultProfile</span></span>
<span data-ttu-id="35340-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="35340-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35340-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="35340-132">-ExpiryTime</span></span>
<span data-ttu-id="35340-133">Określa czas wygaśnięcia nowego konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="35340-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="35340-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="35340-134">-IsAdmin</span></span>
<span data-ttu-id="35340-135">Wskazuje, że polecenie cmdlet tworzy konto użytkownika z poświadczeniami administracyjnymi.</span><span class="sxs-lookup"><span data-stu-id="35340-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35340-136">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="35340-136">-Name</span></span>
<span data-ttu-id="35340-137">Określa nazwę nowego lokalnego konta systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="35340-137">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35340-138">— Hasło</span><span class="sxs-lookup"><span data-stu-id="35340-138">-Password</span></span>
<span data-ttu-id="35340-139">Określa hasło do konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="35340-139">Specifies the user account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35340-140">- PoolId</span><span class="sxs-lookup"><span data-stu-id="35340-140">-PoolId</span></span>
<span data-ttu-id="35340-141">Określa identyfikator puli zawierającej węzeł obliczeniowy, w którym należy utworzyć konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="35340-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="35340-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35340-142">CommonParameters</span></span>
<span data-ttu-id="35340-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35340-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35340-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35340-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35340-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35340-145">INPUTS</span></span>

### <span data-ttu-id="35340-146">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="35340-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="35340-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="35340-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="35340-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35340-148">OUTPUTS</span></span>

### <span data-ttu-id="35340-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="35340-149">System.Void</span></span>

## <span data-ttu-id="35340-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35340-150">NOTES</span></span>

## <span data-ttu-id="35340-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35340-151">RELATED LINKS</span></span>

[<span data-ttu-id="35340-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="35340-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="35340-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="35340-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="35340-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="35340-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="35340-155">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="35340-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
