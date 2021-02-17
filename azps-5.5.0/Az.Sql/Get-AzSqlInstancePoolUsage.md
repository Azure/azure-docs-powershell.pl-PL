---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepoolusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
ms.openlocfilehash: c2acc357e53a57060f7ba1ff3e19a5344ceee412
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191059"
---
# <span data-ttu-id="7d7ca-101">Get-AzSqlInstancePoolUsage</span><span class="sxs-lookup"><span data-stu-id="7d7ca-101">Get-AzSqlInstancePoolUsage</span></span>

## <span data-ttu-id="7d7ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="7d7ca-103">Zwraca informacje o użyciu puli wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-103">Returns information about an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="7d7ca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7d7ca-104">SYNTAX</span></span>

### <span data-ttu-id="7d7ca-105">InstancePoolUsageDefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7d7ca-105">InstancePoolUsageDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceGroupName] <String> [-Name] <String> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d7ca-106">InstancePoolUsageParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d7ca-106">InstancePoolUsageParentObjectParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-InstancePool] <AzureSqlInstancePoolModel> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d7ca-107">InstancePoolUsageResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d7ca-107">InstancePoolUsageResourceIdParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceId] <String> [-ExpandChildren] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d7ca-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7d7ca-108">DESCRIPTION</span></span>
<span data-ttu-id="7d7ca-109">Polecenie **cmdlet Get-AzSqlInstancePoolUsage** zwraca informacje o użyciu puli wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-109">The **Get-AzSqlInstancePoolUsage** cmdlet returns information an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="7d7ca-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7d7ca-110">EXAMPLES</span></span>

### <span data-ttu-id="7d7ca-111">Przykład 1. Pobiera użycie puli wystąpień języka Azure SQL</span><span class="sxs-lookup"><span data-stu-id="7d7ca-111">Example 1 : Gets the usage of an Azure SQL Instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="7d7ca-112">Pobiera użycie puli wystąpień wystąpienia języka Azure SQL Instance0.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-112">Gets the usage for the Azure SQL Instance pool instancepool0.</span></span>

### <span data-ttu-id="7d7ca-113">Przykład 2. Pobiera użycie puli wystąpień języka Azure SQL przy użyciu obiektu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="7d7ca-113">Example 2: Gets the usage of an Azure SQL Instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> Get-AzSqlInstancePoolUsage -InstancePool $instancePool

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="7d7ca-114">Pobiera użycie dla puli wystąpień wystąpienia języka Azure SQL przy użyciu obiektu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-114">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool object.</span></span>

### <span data-ttu-id="7d7ca-115">Przykład 3. Pobiera użycie puli wystąpień języka Azure SQL przy użyciu identyfikatora zasobu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="7d7ca-115">Example 3: Gets the usage of an Azure SQL Instance pool using an instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="7d7ca-116">Pobiera użycie dla puli wystąpień wystąpienia języka Azure SQL przy użyciu identyfikatora zasobu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-116">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool resource identifier.</span></span>

### <span data-ttu-id="7d7ca-117">Przykład 3. Pobiera użycie puli wystąpień języka Azure SQL z podziałem użycia wystąpień zarządzanych w puli.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-117">Example 3: Gets the usage of an Azure SQL Instance pool with a breakdown of the managed instance usages within the pool.</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0 -ExpandChildren

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/vcore_utilization
CurrentValue   :
Limit          : 2
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/storage_utilization
CurrentValue   :
Limit          : 32
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages
```

<span data-ttu-id="7d7ca-118">Pobiera użycie dla puli wystąpień wystąpienia języka Azure SQL wraz z użyciami zarządzanych wystąpień w ramach instancepool0.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-118">Gets the usage for the Azure SQL Instance pool instancepool0 along with the usages of the managed instances within instancepool0.</span></span>

## <span data-ttu-id="7d7ca-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d7ca-119">PARAMETERS</span></span>

### <span data-ttu-id="7d7ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d7ca-120">-DefaultProfile</span></span>
<span data-ttu-id="7d7ca-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d7ca-122">-Expand Zszybki</span><span class="sxs-lookup"><span data-stu-id="7d7ca-122">-ExpandChildren</span></span>
<span data-ttu-id="7d7ca-123">Flaga wskazująca, czy należy rozszerzyć użycie tej puli wystąpień wraz z użyciem dzieci.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-123">Flag indicating whether to expand this instance pool's usage with its children's usage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d7ca-124">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="7d7ca-124">-InstancePool</span></span>
<span data-ttu-id="7d7ca-125">Obiekt puli wystąpienia nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-125">The parent instance pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InstancePoolUsageParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d7ca-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7d7ca-126">-Name</span></span>
<span data-ttu-id="7d7ca-127">Nazwa puli zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-127">The managed instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d7ca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d7ca-128">-ResourceGroupName</span></span>
<span data-ttu-id="7d7ca-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d7ca-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d7ca-130">-ResourceId</span></span>
<span data-ttu-id="7d7ca-131">Identyfikator zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-131">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageResourceIdParameterSet
Aliases: InstancePoolResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d7ca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d7ca-132">CommonParameters</span></span>
<span data-ttu-id="7d7ca-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d7ca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d7ca-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d7ca-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d7ca-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d7ca-135">INPUTS</span></span>

### <span data-ttu-id="7d7ca-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="7d7ca-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="7d7ca-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7d7ca-137">System.String</span></span>

## <span data-ttu-id="7d7ca-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d7ca-138">OUTPUTS</span></span>

### <span data-ttu-id="7d7ca-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span><span class="sxs-lookup"><span data-stu-id="7d7ca-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span></span>

## <span data-ttu-id="7d7ca-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7d7ca-140">NOTES</span></span>

## <span data-ttu-id="7d7ca-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d7ca-141">RELATED LINKS</span></span>
