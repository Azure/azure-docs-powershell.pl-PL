---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: 85dd98ac4eeb262564dcca58ec57f1f5df80842a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993399"
---
# <span data-ttu-id="036e2-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="036e2-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="036e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="036e2-102">SYNOPSIS</span></span>
<span data-ttu-id="036e2-103">Lista obsługiwanych operacji ServiceBus</span><span class="sxs-lookup"><span data-stu-id="036e2-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="036e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="036e2-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="036e2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="036e2-105">DESCRIPTION</span></span>
<span data-ttu-id="036e2-106">Polecenie **cmdlet Get-AzServiceBusOperation** wyświetla listę operacji obsługiwanych przez usługę ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="036e2-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="036e2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="036e2-107">EXAMPLES</span></span>

### <span data-ttu-id="036e2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="036e2-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="036e2-109">Lista operacji obsługiwanych przez usługę ServiceBus</span><span class="sxs-lookup"><span data-stu-id="036e2-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="036e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="036e2-110">PARAMETERS</span></span>

### <span data-ttu-id="036e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="036e2-111">-DefaultProfile</span></span>
<span data-ttu-id="036e2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="036e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="036e2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036e2-113">CommonParameters</span></span>
<span data-ttu-id="036e2-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="036e2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036e2-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="036e2-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036e2-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="036e2-116">INPUTS</span></span>

### <span data-ttu-id="036e2-117">Brak</span><span class="sxs-lookup"><span data-stu-id="036e2-117">None</span></span>

## <span data-ttu-id="036e2-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="036e2-118">OUTPUTS</span></span>

### <span data-ttu-id="036e2-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="036e2-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="036e2-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="036e2-120">NOTES</span></span>

## <span data-ttu-id="036e2-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="036e2-121">RELATED LINKS</span></span>
