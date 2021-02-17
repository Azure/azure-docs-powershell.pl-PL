---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 66bab11ab5632464eed8ee160df527b0e44f053d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239419"
---
# <span data-ttu-id="1af57-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1af57-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="1af57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1af57-102">SYNOPSIS</span></span>
<span data-ttu-id="1af57-103">Pobiera konto batch w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1af57-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="1af57-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1af57-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1af57-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1af57-105">DESCRIPTION</span></span>
<span data-ttu-id="1af57-106">Polecenie **cmdlet Get-AzBatchAccount** otrzymuje konto usługi Azure Batch w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1af57-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="1af57-107">Możesz użyć parametru *AccountName* w celu uzyskania jednego konta lub użyć parametru *ResourceGroupName* w celu uzyskania kont w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1af57-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="1af57-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1af57-108">EXAMPLES</span></span>

### <span data-ttu-id="1af57-109">Przykład 1. Uzyskiwanie konta wsadowego według nazwy</span><span class="sxs-lookup"><span data-stu-id="1af57-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="1af57-110">To polecenie pobiera konto partii o nazwie Pfuller.</span><span class="sxs-lookup"><span data-stu-id="1af57-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="1af57-111">Przykład 2. Uzyskiwanie kont partii skojarzonych z grupą zasobów</span><span class="sxs-lookup"><span data-stu-id="1af57-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="1af57-112">To polecenie pobiera konta partii skojarzone z grupą zasobów CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="1af57-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="1af57-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1af57-113">PARAMETERS</span></span>

### <span data-ttu-id="1af57-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1af57-114">-AccountName</span></span>
<span data-ttu-id="1af57-115">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="1af57-115">Specifies the name of an account.</span></span>
<span data-ttu-id="1af57-116">Jeśli określisz nazwę konta, to polecenie cmdlet zwróci tylko to konto.</span><span class="sxs-lookup"><span data-stu-id="1af57-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af57-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af57-117">-DefaultProfile</span></span>
<span data-ttu-id="1af57-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1af57-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1af57-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af57-119">-ResourceGroupName</span></span>
<span data-ttu-id="1af57-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1af57-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1af57-121">Jeśli określisz grupę zasobów, to polecenie cmdlet pobiera konta w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1af57-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af57-122">— Tag</span><span class="sxs-lookup"><span data-stu-id="1af57-122">-Tag</span></span>
<span data-ttu-id="1af57-123">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="1af57-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1af57-124">Na przykład: @{key0="value0";key1=$null;key2="value2"} To polecenie cmdlet pobiera konta zawierające tagi, które ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="1af57-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1af57-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af57-125">CommonParameters</span></span>
<span data-ttu-id="1af57-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af57-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af57-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1af57-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af57-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1af57-128">INPUTS</span></span>

### <span data-ttu-id="1af57-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1af57-129">System.String</span></span>

### <span data-ttu-id="1af57-130">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1af57-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1af57-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1af57-131">OUTPUTS</span></span>

### <span data-ttu-id="1af57-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1af57-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1af57-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1af57-133">NOTES</span></span>

## <span data-ttu-id="1af57-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1af57-134">RELATED LINKS</span></span>

[<span data-ttu-id="1af57-135">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1af57-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="1af57-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1af57-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="1af57-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="1af57-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="1af57-138">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1af57-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
