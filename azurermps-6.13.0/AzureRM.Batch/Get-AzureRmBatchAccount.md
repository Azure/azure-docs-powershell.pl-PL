---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: ddc3bab48e766f80375fdf98add15e16e0086fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526318"
---
# <span data-ttu-id="af7c9-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="af7c9-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="af7c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af7c9-102">SYNOPSIS</span></span>
<span data-ttu-id="af7c9-103">Pobiera konto wsadowe w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="af7c9-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af7c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af7c9-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af7c9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af7c9-105">DESCRIPTION</span></span>
<span data-ttu-id="af7c9-106">Polecenie cmdlet **Get-AzureRmBatchAccount** pobiera konto Azure Batch w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="af7c9-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="af7c9-107">Za pomocą parametru *AccountName* można uzyskać pojedyncze konto lub można użyć parametru *ResourceGroupName* , aby uzyskać konta w obszarze tej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="af7c9-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="af7c9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af7c9-108">EXAMPLES</span></span>

### <span data-ttu-id="af7c9-109">Przykład 1: Uzyskiwanie konta wsadowego według nazwy</span><span class="sxs-lookup"><span data-stu-id="af7c9-109">Example 1: Get a batch account by name</span></span>
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

<span data-ttu-id="af7c9-110">To polecenie pobiera konto wsadowe o nazwie pfuller.</span><span class="sxs-lookup"><span data-stu-id="af7c9-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="af7c9-111">Przykład 2: uzyskiwanie kont wsadowych skojarzonych z grupą zasobów</span><span class="sxs-lookup"><span data-stu-id="af7c9-111">Example 2: Get the batch accounts associated with a resource group</span></span>
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

<span data-ttu-id="af7c9-112">To polecenie umożliwia pobieranie kont wsadowych skojarzonych z grupą zasobów CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="af7c9-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="af7c9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af7c9-113">PARAMETERS</span></span>

### <span data-ttu-id="af7c9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="af7c9-114">-AccountName</span></span>
<span data-ttu-id="af7c9-115">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="af7c9-115">Specifies the name of an account.</span></span>
<span data-ttu-id="af7c9-116">Jeśli określisz nazwę konta, to polecenie cmdlet zwróci tylko to konto.</span><span class="sxs-lookup"><span data-stu-id="af7c9-116">If you specify an account name, this cmdlet only returns that account.</span></span>

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

### <span data-ttu-id="af7c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7c9-117">-DefaultProfile</span></span>
<span data-ttu-id="af7c9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af7c9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af7c9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af7c9-119">-ResourceGroupName</span></span>
<span data-ttu-id="af7c9-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="af7c9-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="af7c9-121">Jeśli określisz grupę zasobów, to polecenie cmdlet będzie pobierać konta w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="af7c9-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

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

### <span data-ttu-id="af7c9-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="af7c9-122">-Tag</span></span>
<span data-ttu-id="af7c9-123">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="af7c9-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="af7c9-124">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"} to polecenie cmdlet umożliwia pobieranie kont zawierających Tagi, które określono w tym parametrze.</span><span class="sxs-lookup"><span data-stu-id="af7c9-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

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

### <span data-ttu-id="af7c9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7c9-125">CommonParameters</span></span>
<span data-ttu-id="af7c9-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af7c9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7c9-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af7c9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7c9-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af7c9-128">INPUTS</span></span>

### <span data-ttu-id="af7c9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="af7c9-129">System.String</span></span>

### <span data-ttu-id="af7c9-130">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="af7c9-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="af7c9-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af7c9-131">OUTPUTS</span></span>

### <span data-ttu-id="af7c9-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="af7c9-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="af7c9-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af7c9-133">NOTES</span></span>

## <span data-ttu-id="af7c9-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af7c9-134">RELATED LINKS</span></span>

[<span data-ttu-id="af7c9-135">Nowe — AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="af7c9-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="af7c9-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="af7c9-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="af7c9-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="af7c9-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="af7c9-138">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="af7c9-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
