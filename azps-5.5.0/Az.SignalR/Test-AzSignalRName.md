---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198642"
---
# <span data-ttu-id="bb723-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="bb723-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="bb723-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb723-102">SYNOPSIS</span></span>
<span data-ttu-id="bb723-103">Sprawdź dostępność nazwy.</span><span class="sxs-lookup"><span data-stu-id="bb723-103">Check the availability of a name.</span></span> <span data-ttu-id="bb723-104">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="bb723-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="bb723-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb723-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb723-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb723-106">DESCRIPTION</span></span>
<span data-ttu-id="bb723-107">Sprawdź dostępność nazwy.</span><span class="sxs-lookup"><span data-stu-id="bb723-107">Check the availability of a name.</span></span> <span data-ttu-id="bb723-108">Alias: Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="bb723-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="bb723-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb723-109">EXAMPLES</span></span>

### <span data-ttu-id="bb723-110">Sprawdź nazwę, w przypadku których istnieje.</span><span class="sxs-lookup"><span data-stu-id="bb723-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="bb723-111">Sprawdź nieistnieną nazwę.</span><span class="sxs-lookup"><span data-stu-id="bb723-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="bb723-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb723-112">PARAMETERS</span></span>

### <span data-ttu-id="bb723-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb723-113">-DefaultProfile</span></span>
<span data-ttu-id="bb723-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb723-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb723-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bb723-115">-Location</span></span>
<span data-ttu-id="bb723-116">Lokalizacja usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="bb723-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="bb723-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bb723-117">-Name</span></span>
<span data-ttu-id="bb723-118">Nazwa usługi SignalR.</span><span class="sxs-lookup"><span data-stu-id="bb723-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="bb723-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb723-119">CommonParameters</span></span>
<span data-ttu-id="bb723-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb723-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb723-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb723-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb723-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb723-122">INPUTS</span></span>

### <span data-ttu-id="bb723-123">System.String</span><span class="sxs-lookup"><span data-stu-id="bb723-123">System.String</span></span>

## <span data-ttu-id="bb723-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb723-124">OUTPUTS</span></span>

### <span data-ttu-id="bb723-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bb723-125">System.Boolean</span></span>

## <span data-ttu-id="bb723-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb723-126">NOTES</span></span>

## <span data-ttu-id="bb723-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb723-127">RELATED LINKS</span></span>
