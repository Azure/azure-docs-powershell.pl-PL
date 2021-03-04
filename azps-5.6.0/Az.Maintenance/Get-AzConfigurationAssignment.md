---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 32e40bf33ac5f79529f7924b604998c97d004bef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987827"
---
# <span data-ttu-id="13054-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="13054-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="13054-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13054-102">SYNOPSIS</span></span>
<span data-ttu-id="13054-103">Lista pól KonfiguracjiAspisów dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="13054-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="13054-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="13054-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13054-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="13054-105">DESCRIPTION</span></span>
<span data-ttu-id="13054-106">Lista pól KonfiguracjiAspisów dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="13054-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="13054-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="13054-107">EXAMPLES</span></span>

### <span data-ttu-id="13054-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13054-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="13054-109">Lista podpisów konfiguracji dedykowanego hosta.</span><span class="sxs-lookup"><span data-stu-id="13054-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="13054-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13054-110">PARAMETERS</span></span>

### <span data-ttu-id="13054-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13054-111">-DefaultProfile</span></span>
<span data-ttu-id="13054-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="13054-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13054-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="13054-113">-ProviderName</span></span>
<span data-ttu-id="13054-114">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13054-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13054-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13054-115">-ResourceGroupName</span></span>
<span data-ttu-id="13054-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13054-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13054-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="13054-117">-ResourceName</span></span>
<span data-ttu-id="13054-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="13054-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13054-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="13054-119">-ResourceParentName</span></span>
<span data-ttu-id="13054-120">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="13054-120">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13054-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="13054-121">-ResourceParentType</span></span>
<span data-ttu-id="13054-122">Nadrzędny typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="13054-122">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13054-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="13054-123">-ResourceType</span></span>
<span data-ttu-id="13054-124">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="13054-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13054-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13054-125">CommonParameters</span></span>
<span data-ttu-id="13054-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13054-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13054-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13054-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13054-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13054-128">INPUTS</span></span>

### <span data-ttu-id="13054-129">System.String</span><span class="sxs-lookup"><span data-stu-id="13054-129">System.String</span></span>

## <span data-ttu-id="13054-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13054-130">OUTPUTS</span></span>

### <span data-ttu-id="13054-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="13054-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="13054-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="13054-132">NOTES</span></span>

## <span data-ttu-id="13054-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13054-133">RELATED LINKS</span></span>
