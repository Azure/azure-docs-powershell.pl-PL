---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: d1ae8cf3d0fd05acf4fa4897d362bd2cde70b346
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242242"
---
# <span data-ttu-id="299df-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="299df-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="299df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="299df-102">SYNOPSIS</span></span>
<span data-ttu-id="299df-103">Lista obsługiwanych operacji ServiceBus</span><span class="sxs-lookup"><span data-stu-id="299df-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="299df-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="299df-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="299df-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="299df-105">DESCRIPTION</span></span>
<span data-ttu-id="299df-106">Polecenie **cmdlet Get-AzServiceBusOperation** wyświetla listę operacji obsługiwanych przez usługę ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="299df-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="299df-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="299df-107">EXAMPLES</span></span>

### <span data-ttu-id="299df-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="299df-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="299df-109">Lista operacji obsługiwanych przez usługę ServiceBus</span><span class="sxs-lookup"><span data-stu-id="299df-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="299df-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="299df-110">PARAMETERS</span></span>

### <span data-ttu-id="299df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299df-111">-DefaultProfile</span></span>
<span data-ttu-id="299df-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="299df-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="299df-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299df-113">CommonParameters</span></span>
<span data-ttu-id="299df-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="299df-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299df-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="299df-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299df-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="299df-116">INPUTS</span></span>

### <span data-ttu-id="299df-117">Brak</span><span class="sxs-lookup"><span data-stu-id="299df-117">None</span></span>

## <span data-ttu-id="299df-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="299df-118">OUTPUTS</span></span>

### <span data-ttu-id="299df-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="299df-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="299df-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="299df-120">NOTES</span></span>

## <span data-ttu-id="299df-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="299df-121">RELATED LINKS</span></span>
