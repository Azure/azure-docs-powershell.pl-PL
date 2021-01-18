---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 2d1c4b2f272516af31fba17db50d33991dd1db50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501405"
---
# <span data-ttu-id="85a00-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="85a00-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="85a00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85a00-102">SYNOPSIS</span></span>
<span data-ttu-id="85a00-103">Uzyskaj lub Wyświetl listę obsługiwanych kategorii ustawień diagnostycznych dla zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85a00-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="85a00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85a00-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85a00-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85a00-105">DESCRIPTION</span></span>
<span data-ttu-id="85a00-106">Uzyskaj lub Wyświetl listę obsługiwanych kategorii ustawień diagnostycznych dla zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85a00-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="85a00-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85a00-107">EXAMPLES</span></span>

### <span data-ttu-id="85a00-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85a00-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSetting -TargetResourceId -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="85a00-109">Uzyskaj obsługiwane kategorie ustawień diagnostycznych dla sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="85a00-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="85a00-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85a00-110">PARAMETERS</span></span>

### <span data-ttu-id="85a00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a00-111">-DefaultProfile</span></span>
<span data-ttu-id="85a00-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85a00-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85a00-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85a00-113">-Name</span></span>
<span data-ttu-id="85a00-114">Nazwa kategorii ustawień diagnostycznych</span><span class="sxs-lookup"><span data-stu-id="85a00-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="85a00-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="85a00-115">-TargetResourceId</span></span>
<span data-ttu-id="85a00-116">Identyfikator zasobu docelowego</span><span class="sxs-lookup"><span data-stu-id="85a00-116">Target resource Id</span></span>

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

### <span data-ttu-id="85a00-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a00-117">CommonParameters</span></span>
<span data-ttu-id="85a00-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85a00-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a00-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85a00-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a00-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85a00-120">INPUTS</span></span>

### <span data-ttu-id="85a00-121">System. String</span><span class="sxs-lookup"><span data-stu-id="85a00-121">System.String</span></span>

## <span data-ttu-id="85a00-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85a00-122">OUTPUTS</span></span>

### <span data-ttu-id="85a00-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="85a00-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="85a00-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85a00-124">NOTES</span></span>

## <span data-ttu-id="85a00-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85a00-125">RELATED LINKS</span></span>
