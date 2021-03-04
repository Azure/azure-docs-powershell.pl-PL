---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: 01fc755564fdfd702773c31a52e13d8a95c40ede
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955361"
---
# <span data-ttu-id="92d92-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="92d92-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="92d92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92d92-102">SYNOPSIS</span></span>
<span data-ttu-id="92d92-103">Sprawdź dostępność nazwy.</span><span class="sxs-lookup"><span data-stu-id="92d92-103">Check the availability of a name.</span></span> <span data-ttu-id="92d92-104">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="92d92-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="92d92-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="92d92-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92d92-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="92d92-106">DESCRIPTION</span></span>
<span data-ttu-id="92d92-107">Sprawdź dostępność nazwy.</span><span class="sxs-lookup"><span data-stu-id="92d92-107">Check the availability of a name.</span></span> <span data-ttu-id="92d92-108">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="92d92-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="92d92-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="92d92-109">EXAMPLES</span></span>

### <span data-ttu-id="92d92-110">Sprawdź nazwę, w przypadku których istnieje.</span><span class="sxs-lookup"><span data-stu-id="92d92-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="92d92-111">Sprawdź nieistnieną nazwę.</span><span class="sxs-lookup"><span data-stu-id="92d92-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="92d92-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92d92-112">PARAMETERS</span></span>

### <span data-ttu-id="92d92-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d92-113">-DefaultProfile</span></span>
<span data-ttu-id="92d92-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="92d92-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d92-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="92d92-115">-Location</span></span>
<span data-ttu-id="92d92-116">Lokalizacja usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="92d92-116">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d92-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="92d92-117">-Name</span></span>
<span data-ttu-id="92d92-118">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="92d92-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="92d92-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d92-119">CommonParameters</span></span>
<span data-ttu-id="92d92-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92d92-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d92-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92d92-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d92-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92d92-122">INPUTS</span></span>

### <span data-ttu-id="92d92-123">System.String</span><span class="sxs-lookup"><span data-stu-id="92d92-123">System.String</span></span>

## <span data-ttu-id="92d92-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92d92-124">OUTPUTS</span></span>

### <span data-ttu-id="92d92-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92d92-125">System.Boolean</span></span>

## <span data-ttu-id="92d92-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="92d92-126">NOTES</span></span>

## <span data-ttu-id="92d92-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92d92-127">RELATED LINKS</span></span>
