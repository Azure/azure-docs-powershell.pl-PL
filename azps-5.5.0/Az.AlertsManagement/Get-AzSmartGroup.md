---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199795"
---
# <span data-ttu-id="1a9cb-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="1a9cb-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="1a9cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a9cb-102">SYNOPSIS</span></span>
<span data-ttu-id="1a9cb-103">Pobiera informacje o grupach inteligentnych</span><span class="sxs-lookup"><span data-stu-id="1a9cb-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="1a9cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1a9cb-104">SYNTAX</span></span>

### <span data-ttu-id="1a9cb-105">SmartGroupsListByFilter (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1a9cb-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a9cb-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="1a9cb-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a9cb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1a9cb-107">DESCRIPTION</span></span>
<span data-ttu-id="1a9cb-108">**Polecenie cmdlet Get-AzSmartGroup** pobiera informacje o grupach inteligentnych.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="1a9cb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1a9cb-109">EXAMPLES</span></span>

### <span data-ttu-id="1a9cb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1a9cb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="1a9cb-111">Lista wszystkich grup inteligentnych tworzyć w ciągu ostatniej godziny.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="1a9cb-112">Użyj Format-List, aby uzyskać pełne szczegóły każdej grupy inteligentnej na liście.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="1a9cb-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1a9cb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="1a9cb-114">Uzyskiwanie szczegółów grupy inteligentnej według identyfikatora (GUID) lub identyfikatora zasobu (identyfikator ARM zasobów)</span><span class="sxs-lookup"><span data-stu-id="1a9cb-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="1a9cb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a9cb-115">PARAMETERS</span></span>

### <span data-ttu-id="1a9cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a9cb-116">-DefaultProfile</span></span>
<span data-ttu-id="1a9cb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a9cb-118">- SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="1a9cb-118">-SmartGroupId</span></span>
<span data-ttu-id="1a9cb-119">Unikatowy identyfikator grupy SmartGroup/identyfikatora zasobu grupy inteligentnej.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9cb-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="1a9cb-120">-SortBy</span></span>
<span data-ttu-id="1a9cb-121">Właściwość alertu do użycia podczas sortowania</span><span class="sxs-lookup"><span data-stu-id="1a9cb-121">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9cb-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="1a9cb-122">-SortOrder</span></span>
<span data-ttu-id="1a9cb-123">Porządek sortowania</span><span class="sxs-lookup"><span data-stu-id="1a9cb-123">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9cb-124">- TimeRange</span><span class="sxs-lookup"><span data-stu-id="1a9cb-124">-TimeRange</span></span>
<span data-ttu-id="1a9cb-125">Obsługiwane wartości zakresu czasu — 1h, 1d, 7d, 30d (wartość domyślna to 1d)</span><span class="sxs-lookup"><span data-stu-id="1a9cb-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: SmartGroupsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9cb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a9cb-126">CommonParameters</span></span>
<span data-ttu-id="1a9cb-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a9cb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a9cb-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a9cb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a9cb-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a9cb-129">INPUTS</span></span>

### <span data-ttu-id="1a9cb-130">Brak</span><span class="sxs-lookup"><span data-stu-id="1a9cb-130">None</span></span>

## <span data-ttu-id="1a9cb-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a9cb-131">OUTPUTS</span></span>

### <span data-ttu-id="1a9cb-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="1a9cb-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="1a9cb-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1a9cb-133">NOTES</span></span>

## <span data-ttu-id="1a9cb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a9cb-134">RELATED LINKS</span></span>
