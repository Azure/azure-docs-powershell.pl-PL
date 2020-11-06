---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6289aa916b4d03559fccb11ea0a8897f4b506b53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547060"
---
# <span data-ttu-id="48ca3-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="48ca3-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="48ca3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="48ca3-103">Tworzy konto użytkownika w węźle obliczeniowym partii.</span><span class="sxs-lookup"><span data-stu-id="48ca3-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48ca3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48ca3-104">SYNTAX</span></span>

### <span data-ttu-id="48ca3-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="48ca3-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48ca3-106">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="48ca3-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48ca3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="48ca3-107">DESCRIPTION</span></span>
<span data-ttu-id="48ca3-108">Polecenie cmdlet **New-AzureBatchComputeNodeUser** tworzy konto użytkownika w węźle obliczeniowym usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="48ca3-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="48ca3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48ca3-109">EXAMPLES</span></span>

### <span data-ttu-id="48ca3-110">Przykład 1. Tworzenie konta użytkownika z poświadczeniami administracyjnymi</span><span class="sxs-lookup"><span data-stu-id="48ca3-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="48ca3-111">To polecenie tworzy konto użytkownika na węźle obliczeniowym o IDENTYFIKATORze ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="48ca3-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="48ca3-112">Węzeł znajduje się w puli o IDENTYFIKATORze MyPool01.</span><span class="sxs-lookup"><span data-stu-id="48ca3-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="48ca3-113">Nazwa użytkownika to TestUser, hasło to hasło, konto wygasa za siedem dni, a konto ma poświadczenia administracyjne.</span><span class="sxs-lookup"><span data-stu-id="48ca3-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="48ca3-114">Przykład 2: Tworzenie konta użytkownika w węźle obliczeniowym za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="48ca3-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="48ca3-115">To polecenie uzyskuje węzeł obliczeniowy o nazwie ComputeNode01 przy użyciu polecenia cmdlet **Get-AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="48ca3-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="48ca3-116">Ten węzeł znajduje się w puli o IDENTYFIKATORze MyPool01.</span><span class="sxs-lookup"><span data-stu-id="48ca3-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="48ca3-117">Polecenie przekazuje ten węzeł obliczeniowy do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="48ca3-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="48ca3-118">Polecenie tworzy konto użytkownika zawierające nazwę użytkownika TestUserand hasło.</span><span class="sxs-lookup"><span data-stu-id="48ca3-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="48ca3-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48ca3-119">PARAMETERS</span></span>

### <span data-ttu-id="48ca3-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="48ca3-120">-BatchContext</span></span>
<span data-ttu-id="48ca3-121">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="48ca3-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="48ca3-122">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="48ca3-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="48ca3-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="48ca3-123">-ComputeNode</span></span>
<span data-ttu-id="48ca3-124">Określa węzeł obliczeniowe jako obiekt **PSComputeNode** , na którym to polecenie cmdlet tworzy konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="48ca3-124">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="48ca3-125">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="48ca3-125">-ComputeNodeId</span></span>
<span data-ttu-id="48ca3-126">Określa identyfikator węzła obliczeniowego, na którym to polecenie cmdlet tworzy konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="48ca3-126">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="48ca3-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="48ca3-127">-ExpiryTime</span></span>
<span data-ttu-id="48ca3-128">Określa czas wygaśnięcia nowego konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="48ca3-128">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="48ca3-129">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="48ca3-129">-IsAdmin</span></span>
<span data-ttu-id="48ca3-130">Wskazuje, że polecenie cmdlet tworzy konto użytkownika z poświadczeniami administracyjnymi.</span><span class="sxs-lookup"><span data-stu-id="48ca3-130">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="48ca3-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48ca3-131">-Name</span></span>
<span data-ttu-id="48ca3-132">Określa nazwę nowego lokalnego konta systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="48ca3-132">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="48ca3-133">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="48ca3-133">-Password</span></span>
<span data-ttu-id="48ca3-134">Określa hasło do konta użytkownika.</span><span class="sxs-lookup"><span data-stu-id="48ca3-134">Specifies the user account password.</span></span>

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

### <span data-ttu-id="48ca3-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="48ca3-135">-PoolId</span></span>
<span data-ttu-id="48ca3-136">Określa identyfikator puli zawierającej węzeł obliczeniowy, na którym ma zostać utworzone konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="48ca3-136">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="48ca3-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ca3-137">-DefaultProfile</span></span>
<span data-ttu-id="48ca3-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48ca3-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48ca3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ca3-139">CommonParameters</span></span>
<span data-ttu-id="48ca3-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48ca3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ca3-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48ca3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ca3-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48ca3-142">INPUTS</span></span>

### <span data-ttu-id="48ca3-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="48ca3-143">BatchAccountContext</span></span>
<span data-ttu-id="48ca3-144">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="48ca3-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="48ca3-145">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="48ca3-145">PSComputeNode</span></span>
<span data-ttu-id="48ca3-146">Parametr "ComputeNode" akceptuje wartość typu "PSComputeNode" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="48ca3-146">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="48ca3-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48ca3-147">OUTPUTS</span></span>

## <span data-ttu-id="48ca3-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48ca3-148">NOTES</span></span>

## <span data-ttu-id="48ca3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48ca3-149">RELATED LINKS</span></span>

[<span data-ttu-id="48ca3-150">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="48ca3-150">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="48ca3-151">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="48ca3-151">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="48ca3-152">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="48ca3-152">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="48ca3-153">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="48ca3-153">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


