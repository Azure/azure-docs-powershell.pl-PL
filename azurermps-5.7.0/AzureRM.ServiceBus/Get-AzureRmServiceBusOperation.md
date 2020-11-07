---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: de2e826223520c13306411c5d52f448468186804
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718463"
---
# <span data-ttu-id="58f3f-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="58f3f-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="58f3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58f3f-102">SYNOPSIS</span></span>
<span data-ttu-id="58f3f-103">Lista obsługiwanych operacji ServiceBus</span><span class="sxs-lookup"><span data-stu-id="58f3f-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58f3f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58f3f-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58f3f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58f3f-105">DESCRIPTION</span></span>
<span data-ttu-id="58f3f-106">Polecenie cmdlet **Get-AzureRmServiceBusOperation** zawiera listę ServiceBus obsługiwanych operacji.</span><span class="sxs-lookup"><span data-stu-id="58f3f-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="58f3f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58f3f-107">EXAMPLES</span></span>

### <span data-ttu-id="58f3f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58f3f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="58f3f-109">Lista obsługiwanych operacji ServiceBus</span><span class="sxs-lookup"><span data-stu-id="58f3f-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="58f3f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58f3f-110">PARAMETERS</span></span>

### <span data-ttu-id="58f3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f3f-111">-DefaultProfile</span></span>
<span data-ttu-id="58f3f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58f3f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58f3f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f3f-113">CommonParameters</span></span>
<span data-ttu-id="58f3f-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58f3f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f3f-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58f3f-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f3f-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58f3f-116">INPUTS</span></span>

### <span data-ttu-id="58f3f-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="58f3f-117">None</span></span>

### <span data-ttu-id="58f3f-118">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. ServiceBus. MODELES. PSOperationAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.4.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="58f3f-118">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="58f3f-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58f3f-119">OUTPUTS</span></span>

### <span data-ttu-id="58f3f-120">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. ServiceBus. modele. OperationAttributes]</span><span class="sxs-lookup"><span data-stu-id="58f3f-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes]</span></span>

## <span data-ttu-id="58f3f-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58f3f-121">NOTES</span></span>

## <span data-ttu-id="58f3f-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58f3f-122">RELATED LINKS</span></span>

