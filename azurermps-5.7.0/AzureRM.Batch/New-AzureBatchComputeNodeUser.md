---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 3e52b2f3c9bddb2039b87b373d0963d51827f293
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546919"
---
# <span data-ttu-id="dd78c-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="dd78c-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="dd78c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd78c-102">SYNOPSIS</span></span>
<span data-ttu-id="dd78c-103">Tworzy konto użytkownika w węźle obliczeniowym partii.</span><span class="sxs-lookup"><span data-stu-id="dd78c-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd78c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd78c-104">SYNTAX</span></span>

### <span data-ttu-id="dd78c-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="dd78c-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String>
 -Password <SecureString> [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd78c-106">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="dd78c-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd78c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dd78c-107">DESCRIPTION</span></span>
<span data-ttu-id="dd78c-108">Polecenie cmdlet **New-AzureBatchComputeNodeUser** tworzy konto użytkownika w węźle obliczeniowym usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="dd78c-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="dd78c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd78c-109">EXAMPLES</span></span>

### <span data-ttu-id="dd78c-110">Przykład 1. Tworzenie konta użytkownika z poświadczeniami administracyjnymi</span><span class="sxs-lookup"><span data-stu-id="dd78c-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="dd78c-111">To polecenie tworzy konto użytkownika na węźle obliczeniowym o IDENTYFIKATORze ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="dd78c-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="dd78c-112">Węzeł znajduje się w puli o IDENTYFIKATORze MyPool01.</span><span class="sxs-lookup"><span data-stu-id="dd78c-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="dd78c-113">Nazwa użytkownika to TestUser, hasło to hasło, konto wygasa za siedem dni, a konto ma poświadczenia administracyjne.</span><span class="sxs-lookup"><span data-stu-id="dd78c-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="dd78c-114">Przykład 2: Tworzenie konta użytkownika w węźle obliczeniowym za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="dd78c-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="dd78c-115">To polecenie uzyskuje węzeł obliczeniowy o nazwie ComputeNode01 przy użyciu polecenia cmdlet **Get-AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="dd78c-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="dd78c-116">Ten węzeł znajduje się w puli o IDENTYFIKATORze MyPool01.</span><span class="sxs-lookup"><span data-stu-id="dd78c-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="dd78c-117">Polecenie przekazuje ten węzeł obliczeniowy do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="dd78c-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dd78c-118">Polecenie tworzy konto użytkownika zawierające nazwę użytkownika TestUserand hasło.</span><span class="sxs-lookup"><span data-stu-id="dd78c-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="dd78c-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd78c-119">PARAMETERS</span></span>

### <span data-ttu-id="dd78c-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dd78c-120">-BatchContext</span></span>
<span data-ttu-id="dd78c-121">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="dd78c-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dd78c-122">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="dd78c-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dd78c-123">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="dd78c-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dd78c-124">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="dd78c-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dd78c-125">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="dd78c-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dd78c-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="dd78c-126">-ComputeNode</span></span>
<span data-ttu-id="dd78c-127">Określa węzeł obliczeniowe jako obiekt **PSComputeNode** , na którym to polecenie cmdlet tworzy konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dd78c-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd78c-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="dd78c-128">-ComputeNodeId</span></span>
<span data-ttu-id="dd78c-129">Określa identyfikator węzła obliczeniowego, na którym to polecenie cmdlet tworzy konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dd78c-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="dd78c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd78c-130">-DefaultProfile</span></span>
<span data-ttu-id="dd78c-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd78c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd78c-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="dd78c-132">-ExpiryTime</span></span>
<span data-ttu-id="dd78c-133">Określa czas wygaśnięcia nowego konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dd78c-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="dd78c-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="dd78c-134">-IsAdmin</span></span>
<span data-ttu-id="dd78c-135">Wskazuje, że polecenie cmdlet tworzy konto użytkownika z poświadczeniami administracyjnymi.</span><span class="sxs-lookup"><span data-stu-id="dd78c-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd78c-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd78c-136">-Name</span></span>
<span data-ttu-id="dd78c-137">Określa nazwę nowego lokalnego konta systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="dd78c-137">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd78c-138">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="dd78c-138">-Password</span></span>
<span data-ttu-id="dd78c-139">Określa hasło do konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dd78c-139">Specifies the user account password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd78c-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="dd78c-140">-PoolId</span></span>
<span data-ttu-id="dd78c-141">Określa identyfikator puli zawierającej węzeł obliczeniowy, na którym ma zostać utworzone konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dd78c-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="dd78c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd78c-142">CommonParameters</span></span>
<span data-ttu-id="dd78c-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd78c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd78c-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd78c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd78c-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd78c-145">INPUTS</span></span>

### <span data-ttu-id="dd78c-146">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dd78c-146">BatchAccountContext</span></span>
<span data-ttu-id="dd78c-147">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="dd78c-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="dd78c-148">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="dd78c-148">PSComputeNode</span></span>
<span data-ttu-id="dd78c-149">Parametr "ComputeNode" akceptuje wartość typu "PSComputeNode" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="dd78c-149">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="dd78c-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd78c-150">OUTPUTS</span></span>

## <span data-ttu-id="dd78c-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd78c-151">NOTES</span></span>

## <span data-ttu-id="dd78c-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd78c-152">RELATED LINKS</span></span>

[<span data-ttu-id="dd78c-153">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dd78c-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="dd78c-154">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="dd78c-154">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="dd78c-155">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="dd78c-155">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="dd78c-156">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="dd78c-156">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


