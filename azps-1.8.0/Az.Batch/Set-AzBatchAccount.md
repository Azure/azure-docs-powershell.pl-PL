---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 0a19ede4a990b10244204d8f633ed747adb7d30e
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710795"
---
# <span data-ttu-id="3e46a-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3e46a-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="3e46a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e46a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e46a-103">Umożliwia zaktualizowanie konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="3e46a-103">Updates a Batch account.</span></span>

## <span data-ttu-id="3e46a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e46a-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e46a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3e46a-105">DESCRIPTION</span></span>
<span data-ttu-id="3e46a-106">Polecenie cmdlet **Set-AzBatchAccount** aktualizuje konto usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="3e46a-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="3e46a-107">Obecnie to polecenie cmdlet może aktualizować tylko znaczniki.</span><span class="sxs-lookup"><span data-stu-id="3e46a-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="3e46a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e46a-108">EXAMPLES</span></span>

### <span data-ttu-id="3e46a-109">Przykład 1: aktualizowanie znaczników na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="3e46a-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
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

<span data-ttu-id="3e46a-110">To polecenie aktualizuje znaczniki na koncie o nazwie pfuller.</span><span class="sxs-lookup"><span data-stu-id="3e46a-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="3e46a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e46a-111">PARAMETERS</span></span>

### <span data-ttu-id="3e46a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3e46a-112">-AccountName</span></span>
<span data-ttu-id="3e46a-113">Określa nazwę konta wsadowego, które jest aktualizowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e46a-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="3e46a-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3e46a-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="3e46a-115">Określa identyfikator zasobu konta magazynu, który ma być wykorzystywany do automatycznego przechowywania danych.</span><span class="sxs-lookup"><span data-stu-id="3e46a-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="3e46a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e46a-116">-DefaultProfile</span></span>
<span data-ttu-id="3e46a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e46a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e46a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e46a-118">-ResourceGroupName</span></span>
<span data-ttu-id="3e46a-119">Określa grupę zasobów konta, które jest aktualizowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e46a-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="3e46a-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="3e46a-120">-Tag</span></span>
<span data-ttu-id="3e46a-121">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3e46a-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3e46a-122">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="3e46a-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3e46a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e46a-123">CommonParameters</span></span>
<span data-ttu-id="3e46a-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e46a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e46a-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e46a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e46a-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e46a-126">INPUTS</span></span>

### <span data-ttu-id="3e46a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3e46a-127">System.String</span></span>

### <span data-ttu-id="3e46a-128">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3e46a-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3e46a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e46a-129">OUTPUTS</span></span>

### <span data-ttu-id="3e46a-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3e46a-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3e46a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e46a-131">NOTES</span></span>

## <span data-ttu-id="3e46a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e46a-132">RELATED LINKS</span></span>

[<span data-ttu-id="3e46a-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3e46a-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="3e46a-134">Nowe — AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3e46a-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="3e46a-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3e46a-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="3e46a-136">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="3e46a-136">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)