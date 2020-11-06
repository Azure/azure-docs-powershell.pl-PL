---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
ms.openlocfilehash: fbf1911f7ec0483509c8a4e93f326f17c47d7f01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550088"
---
# <span data-ttu-id="78493-101">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="78493-101">Set-AzureRmBatchAccount</span></span>

## <span data-ttu-id="78493-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78493-102">SYNOPSIS</span></span>
<span data-ttu-id="78493-103">Umożliwia zaktualizowanie konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="78493-103">Updates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78493-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78493-104">SYNTAX</span></span>

```
Set-AzureRmBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78493-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78493-105">DESCRIPTION</span></span>
<span data-ttu-id="78493-106">Polecenie cmdlet **Set-AzureRmBatchAccount** aktualizuje konto usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="78493-106">The **Set-AzureRmBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="78493-107">Obecnie to polecenie cmdlet może aktualizować tylko znaczniki.</span><span class="sxs-lookup"><span data-stu-id="78493-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="78493-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78493-108">EXAMPLES</span></span>

### <span data-ttu-id="78493-109">Przykład 1: aktualizowanie znaczników na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="78493-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="78493-110">To polecenie aktualizuje znaczniki na koncie o nazwie pfuller.</span><span class="sxs-lookup"><span data-stu-id="78493-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="78493-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78493-111">PARAMETERS</span></span>

### <span data-ttu-id="78493-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78493-112">-AccountName</span></span>
<span data-ttu-id="78493-113">Określa nazwę konta wsadowego, które jest aktualizowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78493-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78493-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="78493-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="78493-115">Określa identyfikator zasobu konta magazynu, który ma być wykorzystywany do automatycznego przechowywania danych.</span><span class="sxs-lookup"><span data-stu-id="78493-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78493-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78493-116">-ResourceGroupName</span></span>
<span data-ttu-id="78493-117">Określa grupę zasobów konta, które jest aktualizowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78493-117">Specifies the resource group of the account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78493-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="78493-118">-Tag</span></span>
<span data-ttu-id="78493-119">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="78493-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="78493-120">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="78493-120">For example:</span></span>

<span data-ttu-id="78493-121">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="78493-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78493-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78493-122">-DefaultProfile</span></span>
<span data-ttu-id="78493-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78493-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78493-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78493-124">CommonParameters</span></span>
<span data-ttu-id="78493-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78493-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78493-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78493-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78493-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78493-127">INPUTS</span></span>

## <span data-ttu-id="78493-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78493-128">OUTPUTS</span></span>

### <span data-ttu-id="78493-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="78493-129">BatchAccountContext</span></span>

## <span data-ttu-id="78493-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78493-130">NOTES</span></span>

## <span data-ttu-id="78493-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78493-131">RELATED LINKS</span></span>

[<span data-ttu-id="78493-132">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="78493-132">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="78493-133">Nowe — AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="78493-133">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="78493-134">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="78493-134">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="78493-135">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="78493-135">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
