---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: 7fd0283860fd5a0bbca1376afff00c8d4add29b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527085"
---
# <span data-ttu-id="d8dc8-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="d8dc8-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="d8dc8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="d8dc8-103">Pobiera konto wsadowe w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8dc8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8dc8-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8dc8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8dc8-105">DESCRIPTION</span></span>
<span data-ttu-id="d8dc8-106">Polecenie cmdlet **Get-AzureRmBatchAccount** pobiera konto Azure Batch w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="d8dc8-107">Za pomocą parametru *AccountName* można uzyskać pojedyncze konto lub można użyć parametru *ResourceGroupName* , aby uzyskać konta w obszarze tej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="d8dc8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8dc8-108">EXAMPLES</span></span>

### <span data-ttu-id="d8dc8-109">Przykład 1: Uzyskiwanie konta wsadowego według nazwy</span><span class="sxs-lookup"><span data-stu-id="d8dc8-109">Example 1: Get a batch account by name</span></span>
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

<span data-ttu-id="d8dc8-110">To polecenie pobiera konto wsadowe o nazwie pfuller.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="d8dc8-111">Przykład 2: uzyskiwanie kont wsadowych skojarzonych z grupą zasobów</span><span class="sxs-lookup"><span data-stu-id="d8dc8-111">Example 2: Get the batch accounts associated with a resource group</span></span>
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

<span data-ttu-id="d8dc8-112">To polecenie umożliwia pobieranie kont wsadowych skojarzonych z grupą zasobów CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="d8dc8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8dc8-113">PARAMETERS</span></span>

### <span data-ttu-id="d8dc8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d8dc8-114">-AccountName</span></span>
<span data-ttu-id="d8dc8-115">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-115">Specifies the name of an account.</span></span>
<span data-ttu-id="d8dc8-116">Jeśli określisz nazwę konta, to polecenie cmdlet zwróci tylko to konto.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dc8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8dc8-117">-DefaultProfile</span></span>
<span data-ttu-id="d8dc8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8dc8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8dc8-119">-ResourceGroupName</span></span>
<span data-ttu-id="d8dc8-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d8dc8-121">Jeśli określisz grupę zasobów, to polecenie cmdlet będzie pobierać konta w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dc8-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8dc8-122">-Tag</span></span>
<span data-ttu-id="d8dc8-123">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d8dc8-124">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="d8dc8-124">For example:</span></span>

<span data-ttu-id="d8dc8-125">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d8dc8-125">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="d8dc8-126">To polecenie cmdlet umożliwia pobieranie kont zawierających znaczniki, które ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-126">This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dc8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8dc8-127">CommonParameters</span></span>
<span data-ttu-id="d8dc8-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8dc8-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8dc8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8dc8-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8dc8-130">INPUTS</span></span>

### <span data-ttu-id="d8dc8-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d8dc8-131">None</span></span>
<span data-ttu-id="d8dc8-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d8dc8-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8dc8-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8dc8-133">OUTPUTS</span></span>

### <span data-ttu-id="d8dc8-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d8dc8-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d8dc8-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8dc8-135">NOTES</span></span>

## <span data-ttu-id="d8dc8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8dc8-136">RELATED LINKS</span></span>

[<span data-ttu-id="d8dc8-137">Nowe — AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="d8dc8-137">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="d8dc8-138">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="d8dc8-138">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="d8dc8-139">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="d8dc8-139">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="d8dc8-140">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="d8dc8-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
