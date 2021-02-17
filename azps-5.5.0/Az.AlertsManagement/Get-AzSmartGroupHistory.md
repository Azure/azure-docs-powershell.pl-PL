---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192603"
---
# <span data-ttu-id="7faaf-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="7faaf-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="7faaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7faaf-102">SYNOPSIS</span></span>
<span data-ttu-id="7faaf-103">Pobiera historię inteligentnych grup</span><span class="sxs-lookup"><span data-stu-id="7faaf-103">Gets smart group history</span></span>

## <span data-ttu-id="7faaf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7faaf-104">SYNTAX</span></span>

### <span data-ttu-id="7faaf-105">BySmartGroupId (Default)</span><span class="sxs-lookup"><span data-stu-id="7faaf-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7faaf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7faaf-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7faaf-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7faaf-107">DESCRIPTION</span></span>
<span data-ttu-id="7faaf-108">**Polecenie cmdlet Get-AzSmartGroupHistory** pobiera historię inteligentnej grupy.</span><span class="sxs-lookup"><span data-stu-id="7faaf-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="7faaf-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7faaf-109">EXAMPLES</span></span>

### <span data-ttu-id="7faaf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7faaf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="7faaf-111">Pobiera szczegółowe informacje historii grup inteligentnych.</span><span class="sxs-lookup"><span data-stu-id="7faaf-111">Gets smart group history details.</span></span>

## <span data-ttu-id="7faaf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7faaf-112">PARAMETERS</span></span>

### <span data-ttu-id="7faaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7faaf-113">-DefaultProfile</span></span>
<span data-ttu-id="7faaf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7faaf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7faaf-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7faaf-115">-InputObject</span></span>
<span data-ttu-id="7faaf-116">Obiekt wejściowy z potoku.</span><span class="sxs-lookup"><span data-stu-id="7faaf-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="7faaf-117">- SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="7faaf-117">-SmartGroupId</span></span>
<span data-ttu-id="7faaf-118">Unikatowy identyfikator grupy SmartGroup/identyfikatora zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="7faaf-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="7faaf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7faaf-119">CommonParameters</span></span>
<span data-ttu-id="7faaf-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7faaf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7faaf-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7faaf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7faaf-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7faaf-122">INPUTS</span></span>

### <span data-ttu-id="7faaf-123">Brak</span><span class="sxs-lookup"><span data-stu-id="7faaf-123">None</span></span>

## <span data-ttu-id="7faaf-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7faaf-124">OUTPUTS</span></span>

### <span data-ttu-id="7faaf-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="7faaf-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="7faaf-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7faaf-126">NOTES</span></span>

## <span data-ttu-id="7faaf-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7faaf-127">RELATED LINKS</span></span>
