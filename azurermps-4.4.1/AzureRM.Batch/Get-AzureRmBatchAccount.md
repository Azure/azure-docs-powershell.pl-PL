---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: 06d4632d9e7977639c708e81d4613b200189a2a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551924"
---
# <span data-ttu-id="885b6-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="885b6-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="885b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="885b6-102">SYNOPSIS</span></span>
<span data-ttu-id="885b6-103">Pobiera konto wsadowe w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="885b6-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="885b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="885b6-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="885b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="885b6-105">DESCRIPTION</span></span>
<span data-ttu-id="885b6-106">Polecenie cmdlet **Get-AzureRmBatchAccount** pobiera konto Azure Batch w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="885b6-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="885b6-107">Za pomocą parametru *AccountName* można uzyskać pojedyncze konto lub można użyć parametru *ResourceGroupName* , aby uzyskać konta w obszarze tej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="885b6-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="885b6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="885b6-108">EXAMPLES</span></span>

### <span data-ttu-id="885b6-109">Przykład 1: Uzyskiwanie konta wsadowego według nazwy</span><span class="sxs-lookup"><span data-stu-id="885b6-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzureRmBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="885b6-110">To polecenie pobiera konto wsadowe o nazwie pfuller.</span><span class="sxs-lookup"><span data-stu-id="885b6-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="885b6-111">Przykład 2: uzyskiwanie kont wsadowych skojarzonych z grupą zasobów</span><span class="sxs-lookup"><span data-stu-id="885b6-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzureRmBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="885b6-112">To polecenie umożliwia pobieranie kont wsadowych skojarzonych z grupą zasobów CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="885b6-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="885b6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="885b6-113">PARAMETERS</span></span>

### <span data-ttu-id="885b6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="885b6-114">-AccountName</span></span>
<span data-ttu-id="885b6-115">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="885b6-115">Specifies the name of an account.</span></span>
<span data-ttu-id="885b6-116">Jeśli określisz nazwę konta, to polecenie cmdlet zwróci tylko to konto.</span><span class="sxs-lookup"><span data-stu-id="885b6-116">If you specify an account name, this cmdlet only returns that account.</span></span>

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

### <span data-ttu-id="885b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="885b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="885b6-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="885b6-118">Specifies the name of a resource group.</span></span>
<span data-ttu-id="885b6-119">Jeśli określisz grupę zasobów, to polecenie cmdlet będzie pobierać konta w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="885b6-119">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

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

### <span data-ttu-id="885b6-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="885b6-120">-Tag</span></span>
<span data-ttu-id="885b6-121">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="885b6-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="885b6-122">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="885b6-122">For example:</span></span>

<span data-ttu-id="885b6-123">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="885b6-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="885b6-124">To polecenie cmdlet umożliwia pobieranie kont zawierających znaczniki, które ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="885b6-124">This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

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

### <span data-ttu-id="885b6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="885b6-125">-DefaultProfile</span></span>
<span data-ttu-id="885b6-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="885b6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="885b6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="885b6-127">CommonParameters</span></span>
<span data-ttu-id="885b6-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="885b6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="885b6-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="885b6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="885b6-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="885b6-130">INPUTS</span></span>

## <span data-ttu-id="885b6-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="885b6-131">OUTPUTS</span></span>

### <span data-ttu-id="885b6-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="885b6-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="885b6-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="885b6-133">NOTES</span></span>

## <span data-ttu-id="885b6-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="885b6-134">RELATED LINKS</span></span>

[<span data-ttu-id="885b6-135">Nowe — AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="885b6-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="885b6-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="885b6-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="885b6-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="885b6-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="885b6-138">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="885b6-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
