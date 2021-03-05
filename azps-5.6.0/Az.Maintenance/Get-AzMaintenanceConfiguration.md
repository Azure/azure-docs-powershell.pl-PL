---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: 6939cde26695cb4273d776437c3697c03d426db3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984600"
---
# <span data-ttu-id="e7860-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7860-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="e7860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7860-102">SYNOPSIS</span></span>
<span data-ttu-id="e7860-103">Pobierz rekord konfiguracji konserwacji</span><span class="sxs-lookup"><span data-stu-id="e7860-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="e7860-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7860-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7860-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7860-105">DESCRIPTION</span></span>
<span data-ttu-id="e7860-106">Pobierz rekord konfiguracji konserwacji</span><span class="sxs-lookup"><span data-stu-id="e7860-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="e7860-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7860-107">EXAMPLES</span></span>

### <span data-ttu-id="e7860-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7860-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="e7860-109">Pobierz rekord konfiguracji konserwacji</span><span class="sxs-lookup"><span data-stu-id="e7860-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="e7860-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7860-110">PARAMETERS</span></span>

### <span data-ttu-id="e7860-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7860-111">-DefaultProfile</span></span>
<span data-ttu-id="e7860-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7860-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7860-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e7860-113">-Name</span></span>
<span data-ttu-id="e7860-114">Nazwa konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="e7860-114">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7860-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7860-115">-ResourceGroupName</span></span>
<span data-ttu-id="e7860-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7860-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7860-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7860-117">CommonParameters</span></span>
<span data-ttu-id="e7860-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7860-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7860-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7860-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7860-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7860-120">INPUTS</span></span>

### <span data-ttu-id="e7860-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e7860-121">System.String</span></span>

## <span data-ttu-id="e7860-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7860-122">OUTPUTS</span></span>

### <span data-ttu-id="e7860-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7860-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="e7860-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7860-124">NOTES</span></span>

## <span data-ttu-id="e7860-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7860-125">RELATED LINKS</span></span>
