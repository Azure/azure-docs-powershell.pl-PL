---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 16d528497532f026961941963049c61a470ad188
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955489"
---
# <span data-ttu-id="fa71e-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="fa71e-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="fa71e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa71e-102">SYNOPSIS</span></span>
<span data-ttu-id="fa71e-103">Uzyskaj przydział użycia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fa71e-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="fa71e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fa71e-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa71e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fa71e-105">DESCRIPTION</span></span>
<span data-ttu-id="fa71e-106">Uzyskaj przydział użycia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fa71e-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="fa71e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fa71e-107">EXAMPLES</span></span>

### <span data-ttu-id="fa71e-108">Uzyskiwanie przydziału użycia przez wprowadzenie informacji o lokalizacji</span><span class="sxs-lookup"><span data-stu-id="fa71e-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="fa71e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa71e-109">PARAMETERS</span></span>

### <span data-ttu-id="fa71e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa71e-110">-DefaultProfile</span></span>
<span data-ttu-id="fa71e-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa71e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa71e-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fa71e-112">-Location</span></span>
<span data-ttu-id="fa71e-113">Lokalizacja usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="fa71e-113">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa71e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa71e-114">CommonParameters</span></span>
<span data-ttu-id="fa71e-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa71e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa71e-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa71e-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa71e-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa71e-117">INPUTS</span></span>

### <span data-ttu-id="fa71e-118">Brak</span><span class="sxs-lookup"><span data-stu-id="fa71e-118">None</span></span>

## <span data-ttu-id="fa71e-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa71e-119">OUTPUTS</span></span>

### <span data-ttu-id="fa71e-120">Microsoft.Azure.Commands.Signalr.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="fa71e-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="fa71e-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fa71e-121">NOTES</span></span>

## <span data-ttu-id="fa71e-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa71e-122">RELATED LINKS</span></span>
