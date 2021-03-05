---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: df263698a913faf361e5f23bb12d0267be314106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980058"
---
# <span data-ttu-id="d783a-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="d783a-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="d783a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d783a-102">SYNOPSIS</span></span>
<span data-ttu-id="d783a-103">Pobierz kategorię obsługiwanych ustawień diagnostycznych dla zasobu Azure lub przygotuj listę tych kategorii.</span><span class="sxs-lookup"><span data-stu-id="d783a-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="d783a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d783a-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d783a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d783a-105">DESCRIPTION</span></span>
<span data-ttu-id="d783a-106">Pobierz kategorię obsługiwanych ustawień diagnostycznych dla zasobu Azure lub przygotuj listę tych kategorii.</span><span class="sxs-lookup"><span data-stu-id="d783a-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="d783a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d783a-107">EXAMPLES</span></span>

### <span data-ttu-id="d783a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d783a-108">Example 1</span></span>
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

<span data-ttu-id="d783a-109">Uzyskaj obsługiwane kategorie ustawień diagnostycznych dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d783a-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="d783a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d783a-110">PARAMETERS</span></span>

### <span data-ttu-id="d783a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d783a-111">-DefaultProfile</span></span>
<span data-ttu-id="d783a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d783a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d783a-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d783a-113">-Name</span></span>
<span data-ttu-id="d783a-114">Nazwa kategorii ustawień diagnostycznych</span><span class="sxs-lookup"><span data-stu-id="d783a-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="d783a-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d783a-115">-TargetResourceId</span></span>
<span data-ttu-id="d783a-116">Identyfikator zasobu docelowego</span><span class="sxs-lookup"><span data-stu-id="d783a-116">Target resource Id</span></span>

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

### <span data-ttu-id="d783a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d783a-117">CommonParameters</span></span>
<span data-ttu-id="d783a-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d783a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d783a-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d783a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d783a-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d783a-120">INPUTS</span></span>

### <span data-ttu-id="d783a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d783a-121">System.String</span></span>

## <span data-ttu-id="d783a-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d783a-122">OUTPUTS</span></span>

### <span data-ttu-id="d783a-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDianossticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="d783a-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="d783a-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d783a-124">NOTES</span></span>

## <span data-ttu-id="d783a-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d783a-125">RELATED LINKS</span></span>
