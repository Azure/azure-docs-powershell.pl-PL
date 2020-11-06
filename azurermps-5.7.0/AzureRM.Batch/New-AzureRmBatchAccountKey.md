---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: 067f3be3aa668ba5402881b697d7def09cb88658
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552252"
---
# <span data-ttu-id="1d7ec-101">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1d7ec-101">New-AzureRmBatchAccountKey</span></span>

## <span data-ttu-id="1d7ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1d7ec-103">Generuje ponownie klucz konta partii.</span><span class="sxs-lookup"><span data-stu-id="1d7ec-103">Regenerates a key of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d7ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d7ec-104">SYNTAX</span></span>

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d7ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d7ec-105">DESCRIPTION</span></span>
<span data-ttu-id="1d7ec-106">Polecenie cmdlet **New-AzureRmBatchAccountKey** generuje klucz podstawowy lub pomocniczy konta usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="1d7ec-106">The **New-AzureRmBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="1d7ec-107">Polecenie cmdlet zwraca obiekt **BatchAccountContext** , który ma bieżące właściwości **PrimaryAccountKey** i **SecondaryAccountKey** .</span><span class="sxs-lookup"><span data-stu-id="1d7ec-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="1d7ec-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d7ec-108">EXAMPLES</span></span>

### <span data-ttu-id="1d7ec-109">Przykład 1. Regeneruj podstawowy klucz konta na koncie wsadowym</span><span class="sxs-lookup"><span data-stu-id="1d7ec-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="1d7ec-110">To polecenie generuje klucz konta podstawowego na koncie wsadowym o nazwie pfuller.</span><span class="sxs-lookup"><span data-stu-id="1d7ec-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="1d7ec-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d7ec-111">PARAMETERS</span></span>

### <span data-ttu-id="1d7ec-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d7ec-112">-AccountName</span></span>
<span data-ttu-id="1d7ec-113">Określa nazwę konta wsadowego, dla którego to polecenie cmdlet ponownie generuje klucz.</span><span class="sxs-lookup"><span data-stu-id="1d7ec-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d7ec-114">-DefaultProfile</span></span>
<span data-ttu-id="1d7ec-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d7ec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d7ec-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1d7ec-116">-KeyType</span></span>
<span data-ttu-id="1d7ec-117">Określa typ klucza, który zostanie ponownie wyodtwarzany przez ten polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d7ec-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="1d7ec-118">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="1d7ec-118">Valid values are:</span></span> 

- <span data-ttu-id="1d7ec-119">Początkowe</span><span class="sxs-lookup"><span data-stu-id="1d7ec-119">Primary</span></span>
- <span data-ttu-id="1d7ec-120">Dodatkowej</span><span class="sxs-lookup"><span data-stu-id="1d7ec-120">Secondary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d7ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d7ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="1d7ec-122">Określa grupę zasobów konta, dla którego ten aplet polecenia ponownie generuje klucz.</span><span class="sxs-lookup"><span data-stu-id="1d7ec-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7ec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d7ec-123">CommonParameters</span></span>
<span data-ttu-id="1d7ec-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d7ec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d7ec-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d7ec-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d7ec-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d7ec-126">INPUTS</span></span>

### <span data-ttu-id="1d7ec-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1d7ec-127">None</span></span>
<span data-ttu-id="1d7ec-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1d7ec-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d7ec-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d7ec-129">OUTPUTS</span></span>

### <span data-ttu-id="1d7ec-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1d7ec-130">BatchAccountContext</span></span>

## <span data-ttu-id="1d7ec-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d7ec-131">NOTES</span></span>

## <span data-ttu-id="1d7ec-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d7ec-132">RELATED LINKS</span></span>

[<span data-ttu-id="1d7ec-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1d7ec-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="1d7ec-134">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="1d7ec-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


