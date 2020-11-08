---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroup.md
ms.openlocfilehash: b3bb193b47acf0f77851e5b9f4549d455a568b15
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063750"
---
# <span data-ttu-id="f54df-101">Get-AzSmartGroup</span><span class="sxs-lookup"><span data-stu-id="f54df-101">Get-AzSmartGroup</span></span>

## <span data-ttu-id="f54df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f54df-102">SYNOPSIS</span></span>
<span data-ttu-id="f54df-103">Pobiera informacje o grupach inteligentnych</span><span class="sxs-lookup"><span data-stu-id="f54df-103">Gets Smart Groups information</span></span>

## <span data-ttu-id="f54df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f54df-104">SYNTAX</span></span>

### <span data-ttu-id="f54df-105">SmartGroupsListByFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f54df-105">SmartGroupsListByFilter (Default)</span></span>
```
Get-AzSmartGroup [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f54df-106">SmartGroupById</span><span class="sxs-lookup"><span data-stu-id="f54df-106">SmartGroupById</span></span>
```
Get-AzSmartGroup -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f54df-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f54df-107">DESCRIPTION</span></span>
<span data-ttu-id="f54df-108">Polecenie cmdlet **Get-AzSmartGroup** pobiera informacje o grupach inteligentnych.</span><span class="sxs-lookup"><span data-stu-id="f54df-108">**Get-AzSmartGroup** cmdlet gets smart groups information.</span></span>

## <span data-ttu-id="f54df-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f54df-109">EXAMPLES</span></span>

### <span data-ttu-id="f54df-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f54df-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroup -TimeRange "1h"
```

<span data-ttu-id="f54df-111">Lista wszystkich inteligentnych grup utworzonych w ciągu ostatnich 1 godzin.</span><span class="sxs-lookup"><span data-stu-id="f54df-111">List all smart groups formed in last 1 hour.</span></span> <span data-ttu-id="f54df-112">Użyj Format-List, aby uzyskać pełne szczegóły każdej grupy inteligentnej na liście.</span><span class="sxs-lookup"><span data-stu-id="f54df-112">Use Format-List to get the complete details of each smart group in list.</span></span>

### <span data-ttu-id="f54df-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f54df-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSmartGroup -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="f54df-114">Uzyskiwanie szczegółowych informacji o grupie inteligentnej według identyfikatora (GUID) lub identyfikatora zasobu (pełna nazwa RAMIENIa)</span><span class="sxs-lookup"><span data-stu-id="f54df-114">Get Smart Group details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="f54df-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f54df-115">PARAMETERS</span></span>

### <span data-ttu-id="f54df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f54df-116">-DefaultProfile</span></span>
<span data-ttu-id="f54df-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f54df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f54df-118">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="f54df-118">-SmartGroupId</span></span>
<span data-ttu-id="f54df-119">Unikatowy identyfikator karty inteligentnej/ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f54df-119">Unique Identifier of SmartGroup / ResourceId of SmartGroup.</span></span>

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

### <span data-ttu-id="f54df-120">-SortBy</span><span class="sxs-lookup"><span data-stu-id="f54df-120">-SortBy</span></span>
<span data-ttu-id="f54df-121">Właściwość alertu używana podczas sortowania</span><span class="sxs-lookup"><span data-stu-id="f54df-121">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="f54df-122">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="f54df-122">-SortOrder</span></span>
<span data-ttu-id="f54df-123">Kolejność sortowania</span><span class="sxs-lookup"><span data-stu-id="f54df-123">Sort Order</span></span>

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

### <span data-ttu-id="f54df-124">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="f54df-124">-TimeRange</span></span>
<span data-ttu-id="f54df-125">Obsługiwane wartości zakresu czasu — 1H, 1D, 7D, 30d (wartość domyślna to 1D)</span><span class="sxs-lookup"><span data-stu-id="f54df-125">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="f54df-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54df-126">CommonParameters</span></span>
<span data-ttu-id="f54df-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f54df-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54df-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f54df-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54df-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f54df-129">INPUTS</span></span>

### <span data-ttu-id="f54df-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f54df-130">None</span></span>

## <span data-ttu-id="f54df-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f54df-131">OUTPUTS</span></span>

### <span data-ttu-id="f54df-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="f54df-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="f54df-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f54df-133">NOTES</span></span>

## <span data-ttu-id="f54df-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f54df-134">RELATED LINKS</span></span>
