---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192610"
---
# <span data-ttu-id="712c8-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="712c8-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="712c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="712c8-102">SYNOPSIS</span></span>
<span data-ttu-id="712c8-103">Pobiera informacje historii alertów</span><span class="sxs-lookup"><span data-stu-id="712c8-103">Gets Alert History information</span></span>

## <span data-ttu-id="712c8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="712c8-104">SYNTAX</span></span>

### <span data-ttu-id="712c8-105">ByAlertId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="712c8-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="712c8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="712c8-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="712c8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="712c8-107">DESCRIPTION</span></span>
<span data-ttu-id="712c8-108">**Polecenie cmdlet Get-AzAlertObjectHistory** pobiera historię alertów.</span><span class="sxs-lookup"><span data-stu-id="712c8-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="712c8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="712c8-109">EXAMPLES</span></span>

### <span data-ttu-id="712c8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="712c8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="712c8-111">Pobiera szczegóły historii alertów.</span><span class="sxs-lookup"><span data-stu-id="712c8-111">Gets alert history details.</span></span> 

## <span data-ttu-id="712c8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="712c8-112">PARAMETERS</span></span>

### <span data-ttu-id="712c8-113">- AlertId</span><span class="sxs-lookup"><span data-stu-id="712c8-113">-AlertId</span></span>
<span data-ttu-id="712c8-114">Unikatowy identyfikator alertu/identyfikatora zasobu alertu.</span><span class="sxs-lookup"><span data-stu-id="712c8-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="712c8-115">-DefaultProfile</span></span>
<span data-ttu-id="712c8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="712c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="712c8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="712c8-117">-InputObject</span></span>
<span data-ttu-id="712c8-118">Obiekt wejściowy z potoku.</span><span class="sxs-lookup"><span data-stu-id="712c8-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="712c8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="712c8-119">CommonParameters</span></span>
<span data-ttu-id="712c8-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="712c8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="712c8-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="712c8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="712c8-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="712c8-122">INPUTS</span></span>

### <span data-ttu-id="712c8-123">Brak</span><span class="sxs-lookup"><span data-stu-id="712c8-123">None</span></span>

## <span data-ttu-id="712c8-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="712c8-124">OUTPUTS</span></span>

### <span data-ttu-id="712c8-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="712c8-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="712c8-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="712c8-126">NOTES</span></span>

## <span data-ttu-id="712c8-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="712c8-127">RELATED LINKS</span></span>
