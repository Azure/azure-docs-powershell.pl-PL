---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchlocationquotas
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: dea724c77b0574e8235c58a2a696987c94ca586d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718380"
---
# <span data-ttu-id="b8b0f-101">Get-AzureRmBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="b8b0f-101">Get-AzureRmBatchLocationQuotas</span></span>

## <span data-ttu-id="b8b0f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b0f-103">Pobiera przydziały usług partii dla subskrypcji w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b8b0f-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8b0f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8b0f-104">SYNTAX</span></span>

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8b0f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b8b0f-105">DESCRIPTION</span></span>
<span data-ttu-id="b8b0f-106">Pobiera przydziały usług partii dla określonej subskrypcji w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b8b0f-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="b8b0f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8b0f-107">EXAMPLES</span></span>

### <span data-ttu-id="b8b0f-108">Przykład 1: pobieranie przydziałów usług partii dla subskrypcji w zachodnim regionie Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="b8b0f-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="b8b0f-109">To polecenie pobiera przydziały dla bieżącego abonamentu w zachodnim regionie Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="b8b0f-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="b8b0f-110">Wartość zwracana oznacza, że ten abonament może utworzyć tylko jedno konto wsadowe w tym regionie.</span><span class="sxs-lookup"><span data-stu-id="b8b0f-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="b8b0f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8b0f-111">PARAMETERS</span></span>

### <span data-ttu-id="b8b0f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b0f-112">-DefaultProfile</span></span>
<span data-ttu-id="b8b0f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8b0f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8b0f-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b8b0f-114">-Location</span></span>
<span data-ttu-id="b8b0f-115">Określa region, w którym to polecenie cmdlet sprawdza przydziały.</span><span class="sxs-lookup"><span data-stu-id="b8b0f-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="b8b0f-116">Aby uzyskać więcej informacji, zobacz regiony platformy Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="b8b0f-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b0f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b0f-117">CommonParameters</span></span>
<span data-ttu-id="b8b0f-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8b0f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b0f-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8b0f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b0f-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8b0f-120">INPUTS</span></span>

### <span data-ttu-id="b8b0f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b8b0f-121">System.String</span></span>

## <span data-ttu-id="b8b0f-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8b0f-122">OUTPUTS</span></span>

### <span data-ttu-id="b8b0f-123">Microsoft.Azure.Commands.Batch. Modele. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="b8b0f-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="b8b0f-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8b0f-124">NOTES</span></span>

## <span data-ttu-id="b8b0f-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8b0f-125">RELATED LINKS</span></span>
