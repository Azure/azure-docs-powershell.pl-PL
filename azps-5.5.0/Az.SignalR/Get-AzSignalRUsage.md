---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189035"
---
# <span data-ttu-id="5e8dc-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="5e8dc-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="5e8dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="5e8dc-103">Uzyskaj przydział użycia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5e8dc-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="5e8dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5e8dc-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e8dc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5e8dc-105">DESCRIPTION</span></span>
<span data-ttu-id="5e8dc-106">Uzyskaj przydział użycia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5e8dc-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="5e8dc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5e8dc-107">EXAMPLES</span></span>

### <span data-ttu-id="5e8dc-108">Uzyskiwanie przydziału użycia przez wprowadzenie informacji o lokalizacji</span><span class="sxs-lookup"><span data-stu-id="5e8dc-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="5e8dc-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e8dc-109">PARAMETERS</span></span>

### <span data-ttu-id="5e8dc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e8dc-110">-DefaultProfile</span></span>
<span data-ttu-id="5e8dc-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e8dc-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e8dc-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5e8dc-112">-Location</span></span>
<span data-ttu-id="5e8dc-113">Lokalizacja usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="5e8dc-113">The SignalR service location.</span></span>

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

### <span data-ttu-id="5e8dc-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e8dc-114">CommonParameters</span></span>
<span data-ttu-id="5e8dc-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e8dc-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e8dc-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e8dc-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e8dc-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e8dc-117">INPUTS</span></span>

### <span data-ttu-id="5e8dc-118">Brak</span><span class="sxs-lookup"><span data-stu-id="5e8dc-118">None</span></span>

## <span data-ttu-id="5e8dc-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5e8dc-119">OUTPUTS</span></span>

### <span data-ttu-id="5e8dc-120">Microsoft.Azure.Commands.Signalr.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="5e8dc-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="5e8dc-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5e8dc-121">NOTES</span></span>

## <span data-ttu-id="5e8dc-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e8dc-122">RELATED LINKS</span></span>
