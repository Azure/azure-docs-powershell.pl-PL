---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccountKey.md
ms.openlocfilehash: ee5ae846ed83065b797f1389827d7d53ae1988d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015521"
---
# <span data-ttu-id="9b66b-101">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9b66b-101">New-AzBatchAccountKey</span></span>

## <span data-ttu-id="9b66b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b66b-102">SYNOPSIS</span></span>
<span data-ttu-id="9b66b-103">Ponownie generuje klucz konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9b66b-103">Regenerates a key of a Batch account.</span></span>

## <span data-ttu-id="9b66b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b66b-104">SYNTAX</span></span>

```
New-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b66b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b66b-105">DESCRIPTION</span></span>
<span data-ttu-id="9b66b-106">Polecenie **cmdlet New-AzBatchAccountKey** ponownie generuje klucz podstawowy lub pomocniczy konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="9b66b-106">The **New-AzBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="9b66b-107">Polecenie cmdlet zwraca **obiekt BatchAccountContext,** który ma swoje bieżące właściwości **PrimaryAccountKey** i **SecondaryAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="9b66b-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="9b66b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b66b-108">EXAMPLES</span></span>

### <span data-ttu-id="9b66b-109">Przykład 1. Ponowne generowanie klucza konta podstawowego na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="9b66b-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
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

<span data-ttu-id="9b66b-110">To polecenie ponownie generuje klucz konta podstawowego na koncie batch o nazwie pfuller.</span><span class="sxs-lookup"><span data-stu-id="9b66b-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="9b66b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b66b-111">PARAMETERS</span></span>

### <span data-ttu-id="9b66b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9b66b-112">-AccountName</span></span>
<span data-ttu-id="9b66b-113">Określa nazwę konta usługi Batch, dla którego to polecenie cmdlet ponownie generuje klucz.</span><span class="sxs-lookup"><span data-stu-id="9b66b-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="9b66b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b66b-114">-DefaultProfile</span></span>
<span data-ttu-id="9b66b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b66b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b66b-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="9b66b-116">-KeyType</span></span>
<span data-ttu-id="9b66b-117">Określa typ klucza, który jest ponownie generowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b66b-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="9b66b-118">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="9b66b-118">Valid values are:</span></span>
- <span data-ttu-id="9b66b-119">Podstawowa</span><span class="sxs-lookup"><span data-stu-id="9b66b-119">Primary</span></span>
- <span data-ttu-id="9b66b-120">Pomocniczy</span><span class="sxs-lookup"><span data-stu-id="9b66b-120">Secondary</span></span>

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

### <span data-ttu-id="9b66b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b66b-121">-ResourceGroupName</span></span>
<span data-ttu-id="9b66b-122">Określa grupę zasobów konta, dla którego to polecenie cmdlet ponownie generuje klucz.</span><span class="sxs-lookup"><span data-stu-id="9b66b-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="9b66b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b66b-123">CommonParameters</span></span>
<span data-ttu-id="9b66b-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b66b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b66b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b66b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b66b-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b66b-126">INPUTS</span></span>

### <span data-ttu-id="9b66b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9b66b-127">System.String</span></span>

## <span data-ttu-id="9b66b-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b66b-128">OUTPUTS</span></span>

### <span data-ttu-id="9b66b-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9b66b-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9b66b-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b66b-130">NOTES</span></span>

## <span data-ttu-id="9b66b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b66b-131">RELATED LINKS</span></span>

[<span data-ttu-id="9b66b-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9b66b-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9b66b-133">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="9b66b-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
