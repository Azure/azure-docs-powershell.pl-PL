---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 29c65ef5f5ec3b2b54fb883da706ddc9a38e1d4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180178"
---
# <span data-ttu-id="77d1b-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="77d1b-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="77d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="77d1b-103">Pobierz kategorię obsługiwanych ustawień diagnostycznych dla zasobu Azure lub uzyskaj dostęp do tej listy.</span><span class="sxs-lookup"><span data-stu-id="77d1b-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="77d1b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="77d1b-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77d1b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="77d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="77d1b-106">Pobierz kategorię obsługiwanych ustawień diagnostycznych dla zasobu Azure lub przygotuj listę tych kategorii.</span><span class="sxs-lookup"><span data-stu-id="77d1b-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="77d1b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="77d1b-107">EXAMPLES</span></span>

### <span data-ttu-id="77d1b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77d1b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSettingCategory -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="77d1b-109">Uzyskaj obsługiwane kategorie ustawień diagnostycznych dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="77d1b-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="77d1b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77d1b-110">PARAMETERS</span></span>

### <span data-ttu-id="77d1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d1b-111">-DefaultProfile</span></span>
<span data-ttu-id="77d1b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="77d1b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77d1b-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="77d1b-113">-Name</span></span>
<span data-ttu-id="77d1b-114">Nazwa kategorii ustawień diagnostycznych</span><span class="sxs-lookup"><span data-stu-id="77d1b-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="77d1b-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="77d1b-115">-TargetResourceId</span></span>
<span data-ttu-id="77d1b-116">Identyfikator zasobu docelowego</span><span class="sxs-lookup"><span data-stu-id="77d1b-116">Target resource Id</span></span>

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

### <span data-ttu-id="77d1b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d1b-117">CommonParameters</span></span>
<span data-ttu-id="77d1b-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77d1b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d1b-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77d1b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d1b-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77d1b-120">INPUTS</span></span>

### <span data-ttu-id="77d1b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="77d1b-121">System.String</span></span>

## <span data-ttu-id="77d1b-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77d1b-122">OUTPUTS</span></span>

### <span data-ttu-id="77d1b-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDianossticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="77d1b-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="77d1b-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="77d1b-124">NOTES</span></span>

## <span data-ttu-id="77d1b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77d1b-125">RELATED LINKS</span></span>
