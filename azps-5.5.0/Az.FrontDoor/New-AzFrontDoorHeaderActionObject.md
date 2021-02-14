---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237839"
---
# <span data-ttu-id="91c10-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="91c10-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="91c10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91c10-102">SYNOPSIS</span></span>
<span data-ttu-id="91c10-103">Tworzenie obiektu PSHeaderAction.</span><span class="sxs-lookup"><span data-stu-id="91c10-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="91c10-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="91c10-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91c10-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="91c10-105">DESCRIPTION</span></span>
<span data-ttu-id="91c10-106">Tworzy obiekt PSHeaderAction w celu utworzenia obiektu PSRulesEngineAction.</span><span class="sxs-lookup"><span data-stu-id="91c10-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="91c10-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="91c10-107">EXAMPLES</span></span>

### <span data-ttu-id="91c10-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="91c10-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="91c10-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91c10-109">PARAMETERS</span></span>

### <span data-ttu-id="91c10-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c10-110">-DefaultProfile</span></span>
<span data-ttu-id="91c10-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="91c10-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91c10-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="91c10-112">-HeaderActionType</span></span>
<span data-ttu-id="91c10-113">Jakiego rodzaju manipulowanie ma dotyczyć nagłówek.</span><span class="sxs-lookup"><span data-stu-id="91c10-113">Which type of manipulation to apply to the header.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderActionType
Parameter Sets: (All)
Aliases:
Accepted values: Append, Delete, Overwrite

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c10-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="91c10-114">-HeaderName</span></span>
<span data-ttu-id="91c10-115">Nazwa nagłówka, do których ta akcja będzie dotyczyć.</span><span class="sxs-lookup"><span data-stu-id="91c10-115">The name of the header this action will apply to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c10-116">— Wartość</span><span class="sxs-lookup"><span data-stu-id="91c10-116">-Value</span></span>
<span data-ttu-id="91c10-117">Wartość, za pomocą która ma być podana nazwa nagłówka.</span><span class="sxs-lookup"><span data-stu-id="91c10-117">The value to update the given header name with.</span></span>
<span data-ttu-id="91c10-118">Ta wartość nie jest używana, jeśli typ akcji to Delete.</span><span class="sxs-lookup"><span data-stu-id="91c10-118">This value is not used if the actionType is Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c10-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c10-119">CommonParameters</span></span>
<span data-ttu-id="91c10-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c10-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c10-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91c10-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c10-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91c10-122">INPUTS</span></span>

### <span data-ttu-id="91c10-123">Brak</span><span class="sxs-lookup"><span data-stu-id="91c10-123">None</span></span>

## <span data-ttu-id="91c10-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91c10-124">OUTPUTS</span></span>

### <span data-ttu-id="91c10-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="91c10-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="91c10-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="91c10-126">NOTES</span></span>

## <span data-ttu-id="91c10-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91c10-127">RELATED LINKS</span></span>
