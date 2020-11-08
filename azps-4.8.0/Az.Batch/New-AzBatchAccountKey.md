---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: 121e4b4b2ffe25d9e5ae53cb03e60cb7a1da91b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219588"
---
# <span data-ttu-id="fb88d-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="fb88d-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="fb88d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb88d-102">SYNOPSIS</span></span>
<span data-ttu-id="fb88d-103">Generuje ponownie klucz konta partii.</span><span class="sxs-lookup"><span data-stu-id="fb88d-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="fb88d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb88d-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb88d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fb88d-105">DESCRIPTION</span></span>
<span data-ttu-id="fb88d-106">Polecenie cmdlet **New-AzBatchAccountKey** generuje klucz podstawowy lub pomocniczy konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="fb88d-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="fb88d-107">Polecenie cmdlet zwraca obiekt **BatchAccountContext** , który ma bieżące właściwości **PrimaryAccountKey** i **SecondaryAccountKey** .</span><span class="sxs-lookup"><span data-stu-id="fb88d-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="fb88d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb88d-108">EXAMPLES</span></span>

### <span data-ttu-id="fb88d-109">Przykład 1. Regeneruj podstawowy klucz konta na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="fb88d-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="fb88d-110">To polecenie generuje klucz konta podstawowego na koncie wsadowym o nazwie pfuller.</span><span class="sxs-lookup"><span data-stu-id="fb88d-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="fb88d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb88d-111">PARAMETERS</span></span>

### <span data-ttu-id="fb88d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fb88d-112">-AccountName</span></span>
<span data-ttu-id="fb88d-113">Określa nazwę konta wsadowego, dla którego to polecenie cmdlet ponownie generuje klucz.</span><span class="sxs-lookup"><span data-stu-id="fb88d-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="fb88d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb88d-114">-DefaultProfile</span></span>
<span data-ttu-id="fb88d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb88d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb88d-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="fb88d-116">-KeyType</span></span>
<span data-ttu-id="fb88d-117">Określa typ klucza, który zostanie ponownie wyodtwarzany przez ten polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb88d-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="fb88d-118">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="fb88d-118">Valid values are:</span></span>
- <span data-ttu-id="fb88d-119">Początkowe</span><span class="sxs-lookup"><span data-stu-id="fb88d-119">Primary</span></span>
- <span data-ttu-id="fb88d-120">Dodatkowej</span><span class="sxs-lookup"><span data-stu-id="fb88d-120">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb88d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb88d-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb88d-122">Określa grupę zasobów konta, dla którego ten aplet polecenia ponownie generuje klucz.</span><span class="sxs-lookup"><span data-stu-id="fb88d-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="fb88d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb88d-123">CommonParameters</span></span>
<span data-ttu-id="fb88d-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb88d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb88d-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb88d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb88d-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb88d-126">INPUTS</span></span>

### <span data-ttu-id="fb88d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fb88d-127">System.String</span></span>

## <span data-ttu-id="fb88d-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb88d-128">OUTPUTS</span></span>

### <span data-ttu-id="fb88d-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fb88d-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fb88d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb88d-130">NOTES</span></span>

## <span data-ttu-id="fb88d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb88d-131">RELATED LINKS</span></span>

[<span data-ttu-id="fb88d-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="fb88d-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="fb88d-133">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="fb88d-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
