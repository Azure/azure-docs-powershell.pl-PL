---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: f18cb699df3bd96a6b5705e09f6cb9ea924f3f62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995058"
---
# <span data-ttu-id="e29d7-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="e29d7-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="e29d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e29d7-102">SYNOPSIS</span></span>
<span data-ttu-id="e29d7-103">Usuwa wirtualny klaster języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e29d7-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="e29d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e29d7-104">SYNTAX</span></span>

### <span data-ttu-id="e29d7-105">RemoveVirtualClusterFromInputParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e29d7-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e29d7-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="e29d7-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e29d7-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e29d7-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e29d7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e29d7-108">DESCRIPTION</span></span>
<span data-ttu-id="e29d7-109">Polecenie **cmdlet Remove-AzSqlVirtualCluster** usuwa klaster wirtualny języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e29d7-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="e29d7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e29d7-110">EXAMPLES</span></span>

### <span data-ttu-id="e29d7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e29d7-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="e29d7-112">To polecenie usuwa klaster wirtualny o nazwie VirtualCluster1 przypisany do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e29d7-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="e29d7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e29d7-113">PARAMETERS</span></span>

### <span data-ttu-id="e29d7-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e29d7-114">-AsJob</span></span>
<span data-ttu-id="e29d7-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e29d7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e29d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29d7-116">-DefaultProfile</span></span>
<span data-ttu-id="e29d7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e29d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e29d7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e29d7-118">-InputObject</span></span>
<span data-ttu-id="e29d7-119">Obiekt wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="e29d7-119">The instance object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel
Parameter Sets: RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition
Aliases: VirtualCluster

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e29d7-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e29d7-120">-Name</span></span>
<span data-ttu-id="e29d7-121">Nazwa klastru wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="e29d7-121">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29d7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e29d7-122">-ResourceGroupName</span></span>
<span data-ttu-id="e29d7-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e29d7-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29d7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e29d7-124">-ResourceId</span></span>
<span data-ttu-id="e29d7-125">Identyfikator zasobu obiektu wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="e29d7-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e29d7-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e29d7-126">-Confirm</span></span>
<span data-ttu-id="e29d7-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e29d7-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29d7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e29d7-128">-WhatIf</span></span>
<span data-ttu-id="e29d7-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e29d7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e29d7-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e29d7-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29d7-131">CommonParameters</span></span>
<span data-ttu-id="e29d7-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e29d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29d7-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e29d7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29d7-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e29d7-134">INPUTS</span></span>

### <span data-ttu-id="e29d7-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="e29d7-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="e29d7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e29d7-136">System.String</span></span>

## <span data-ttu-id="e29d7-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e29d7-137">OUTPUTS</span></span>

### <span data-ttu-id="e29d7-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="e29d7-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="e29d7-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e29d7-139">NOTES</span></span>

## <span data-ttu-id="e29d7-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e29d7-140">RELATED LINKS</span></span>
