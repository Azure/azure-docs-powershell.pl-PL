---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: ad005dbf386bc8340fa0da0c5e8dac1d11bf4bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971034"
---
# <span data-ttu-id="f6924-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="f6924-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="f6924-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6924-102">SYNOPSIS</span></span>
<span data-ttu-id="f6924-103">Tworzenie obiektu PSHeaderAction.</span><span class="sxs-lookup"><span data-stu-id="f6924-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="f6924-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f6924-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6924-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f6924-105">DESCRIPTION</span></span>
<span data-ttu-id="f6924-106">Tworzy obiekt PSHeaderAction w celu utworzenia obiektu PSRulesEngineAction.</span><span class="sxs-lookup"><span data-stu-id="f6924-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="f6924-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f6924-107">EXAMPLES</span></span>

### <span data-ttu-id="f6924-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6924-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="f6924-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6924-109">PARAMETERS</span></span>

### <span data-ttu-id="f6924-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6924-110">-DefaultProfile</span></span>
<span data-ttu-id="f6924-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6924-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6924-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="f6924-112">-HeaderActionType</span></span>
<span data-ttu-id="f6924-113">Jakiego typu manipulowanie ma dotyczyć nagłówek.</span><span class="sxs-lookup"><span data-stu-id="f6924-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="f6924-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="f6924-114">-HeaderName</span></span>
<span data-ttu-id="f6924-115">Nazwa nagłówka, do których będzie stosowane ta akcja.</span><span class="sxs-lookup"><span data-stu-id="f6924-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="f6924-116">— Wartość</span><span class="sxs-lookup"><span data-stu-id="f6924-116">-Value</span></span>
<span data-ttu-id="f6924-117">Wartość, za pomocą która ma być aktualizowana nazwa nagłówka.</span><span class="sxs-lookup"><span data-stu-id="f6924-117">The value to update the given header name with.</span></span>
<span data-ttu-id="f6924-118">Ta wartość nie jest używana, jeśli actionType (Typ akcji) to Delete (Usuń).</span><span class="sxs-lookup"><span data-stu-id="f6924-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="f6924-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6924-119">CommonParameters</span></span>
<span data-ttu-id="f6924-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6924-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6924-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6924-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6924-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6924-122">INPUTS</span></span>

### <span data-ttu-id="f6924-123">Brak</span><span class="sxs-lookup"><span data-stu-id="f6924-123">None</span></span>

## <span data-ttu-id="f6924-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6924-124">OUTPUTS</span></span>

### <span data-ttu-id="f6924-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="f6924-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="f6924-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f6924-126">NOTES</span></span>

## <span data-ttu-id="f6924-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6924-127">RELATED LINKS</span></span>
