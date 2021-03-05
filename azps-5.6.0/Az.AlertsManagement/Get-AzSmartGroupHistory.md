---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: 7a581d81938a647d845d2220b27347c1b42fcb03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960993"
---
# <span data-ttu-id="c22e3-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="c22e3-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="c22e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c22e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c22e3-103">Pobiera historię inteligentnych grup</span><span class="sxs-lookup"><span data-stu-id="c22e3-103">Gets smart group history</span></span>

## <span data-ttu-id="c22e3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c22e3-104">SYNTAX</span></span>

### <span data-ttu-id="c22e3-105">BySmartGroupId (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c22e3-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c22e3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c22e3-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c22e3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c22e3-107">DESCRIPTION</span></span>
<span data-ttu-id="c22e3-108">**Polecenie cmdlet Get-AzSmartGroupHistory** pobiera historię inteligentnej grupy.</span><span class="sxs-lookup"><span data-stu-id="c22e3-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="c22e3-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c22e3-109">EXAMPLES</span></span>

### <span data-ttu-id="c22e3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c22e3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="c22e3-111">Pobiera szczegółowe informacje historii grup inteligentnych.</span><span class="sxs-lookup"><span data-stu-id="c22e3-111">Gets smart group history details.</span></span>

## <span data-ttu-id="c22e3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c22e3-112">PARAMETERS</span></span>

### <span data-ttu-id="c22e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22e3-113">-DefaultProfile</span></span>
<span data-ttu-id="c22e3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c22e3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c22e3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c22e3-115">-InputObject</span></span>
<span data-ttu-id="c22e3-116">Obiekt wejściowy z potoku.</span><span class="sxs-lookup"><span data-stu-id="c22e3-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c22e3-117">- SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="c22e3-117">-SmartGroupId</span></span>
<span data-ttu-id="c22e3-118">Unikatowy identyfikator grupy SmartGroup/identyfikatora zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="c22e3-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22e3-119">CommonParameters</span></span>
<span data-ttu-id="c22e3-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c22e3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22e3-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c22e3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22e3-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c22e3-122">INPUTS</span></span>

### <span data-ttu-id="c22e3-123">Brak</span><span class="sxs-lookup"><span data-stu-id="c22e3-123">None</span></span>

## <span data-ttu-id="c22e3-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c22e3-124">OUTPUTS</span></span>

### <span data-ttu-id="c22e3-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="c22e3-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="c22e3-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c22e3-126">NOTES</span></span>

## <span data-ttu-id="c22e3-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c22e3-127">RELATED LINKS</span></span>
