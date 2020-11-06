---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 8e6e10c45034402e5339ed5cb6d60a9319362450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525353"
---
# <span data-ttu-id="398e0-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="398e0-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="398e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="398e0-102">SYNOPSIS</span></span>
<span data-ttu-id="398e0-103">Pobiera klucze konta wsadowego.</span><span class="sxs-lookup"><span data-stu-id="398e0-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="398e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="398e0-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="398e0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="398e0-105">DESCRIPTION</span></span>
<span data-ttu-id="398e0-106">Polecenie cmdlet **Get-AzureRmBatchAccountKeys** pobiera klucze konta usługi Azure Batch w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="398e0-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="398e0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="398e0-107">EXAMPLES</span></span>

## <span data-ttu-id="398e0-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="398e0-108">PARAMETERS</span></span>

### <span data-ttu-id="398e0-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="398e0-109">-AccountName</span></span>
<span data-ttu-id="398e0-110">Określa nazwę konta, dla którego to polecenie cmdlet pobiera klucze.</span><span class="sxs-lookup"><span data-stu-id="398e0-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="398e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="398e0-111">-DefaultProfile</span></span>
<span data-ttu-id="398e0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="398e0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="398e0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="398e0-113">-ResourceGroupName</span></span>
<span data-ttu-id="398e0-114">Określa nazwę grupy zasobów zawierającej konto, dla którego to polecenie cmdlet pobiera klucze.</span><span class="sxs-lookup"><span data-stu-id="398e0-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="398e0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="398e0-115">CommonParameters</span></span>
<span data-ttu-id="398e0-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="398e0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="398e0-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="398e0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="398e0-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="398e0-118">INPUTS</span></span>

### <span data-ttu-id="398e0-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="398e0-119">None</span></span>
<span data-ttu-id="398e0-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="398e0-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="398e0-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="398e0-121">OUTPUTS</span></span>

### <span data-ttu-id="398e0-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="398e0-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="398e0-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="398e0-123">NOTES</span></span>

## <span data-ttu-id="398e0-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="398e0-124">RELATED LINKS</span></span>

[<span data-ttu-id="398e0-125">Nowe — AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="398e0-125">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="398e0-126">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="398e0-126">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


