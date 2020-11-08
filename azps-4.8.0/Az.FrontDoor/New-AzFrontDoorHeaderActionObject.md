---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223911"
---
# <span data-ttu-id="15717-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="15717-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="15717-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15717-102">SYNOPSIS</span></span>
<span data-ttu-id="15717-103">Utwórz obiekt PSHeaderAction.</span><span class="sxs-lookup"><span data-stu-id="15717-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="15717-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15717-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15717-105">Opis</span><span class="sxs-lookup"><span data-stu-id="15717-105">DESCRIPTION</span></span>
<span data-ttu-id="15717-106">Tworzy obiekt PSHeaderAction do utworzenia obiektu PSRulesEngineAction.</span><span class="sxs-lookup"><span data-stu-id="15717-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="15717-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15717-107">EXAMPLES</span></span>

### <span data-ttu-id="15717-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="15717-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="15717-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15717-109">PARAMETERS</span></span>

### <span data-ttu-id="15717-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15717-110">-DefaultProfile</span></span>
<span data-ttu-id="15717-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15717-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15717-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="15717-112">-HeaderActionType</span></span>
<span data-ttu-id="15717-113">Typ manipulacji, który ma zostać zastosowany do nagłówka.</span><span class="sxs-lookup"><span data-stu-id="15717-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="15717-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="15717-114">-HeaderName</span></span>
<span data-ttu-id="15717-115">Nazwa nagłówka, do którego będzie stosowana ta akcja.</span><span class="sxs-lookup"><span data-stu-id="15717-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="15717-116">-Value</span><span class="sxs-lookup"><span data-stu-id="15717-116">-Value</span></span>
<span data-ttu-id="15717-117">Wartość, która ma zostać zaktualizowana przy użyciu danej nazwy nagłówka.</span><span class="sxs-lookup"><span data-stu-id="15717-117">The value to update the given header name with.</span></span>
<span data-ttu-id="15717-118">Ta wartość nie jest używana, jeśli argument ActionType jest usuwany.</span><span class="sxs-lookup"><span data-stu-id="15717-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="15717-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15717-119">CommonParameters</span></span>
<span data-ttu-id="15717-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15717-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15717-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15717-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15717-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15717-122">INPUTS</span></span>

### <span data-ttu-id="15717-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="15717-123">None</span></span>

## <span data-ttu-id="15717-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15717-124">OUTPUTS</span></span>

### <span data-ttu-id="15717-125">Microsoft. Azure. Commands. FrontDoor. models. PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="15717-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="15717-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15717-126">NOTES</span></span>

## <span data-ttu-id="15717-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15717-127">RELATED LINKS</span></span>
