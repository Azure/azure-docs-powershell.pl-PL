---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201450"
---
# <span data-ttu-id="e84be-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="e84be-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="e84be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e84be-102">SYNOPSIS</span></span>
<span data-ttu-id="e84be-103">Usuwa pulę wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e84be-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="e84be-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e84be-104">SYNTAX</span></span>

### <span data-ttu-id="e84be-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e84be-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e84be-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e84be-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e84be-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e84be-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e84be-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e84be-108">DESCRIPTION</span></span>
<span data-ttu-id="e84be-109">Polecenie **cmdlet Remove-AzSqlInstancePool** usuwa pulę wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e84be-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="e84be-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e84be-110">EXAMPLES</span></span>

### <span data-ttu-id="e84be-111">Przykład 1. Usuwanie puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="e84be-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="e84be-112">Przykład 2. Usuwanie puli wystąpień za pomocą identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="e84be-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="e84be-113">Przykład 3. Usuwanie puli wystąpień przez obiekt puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="e84be-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="e84be-114">To polecenie usuwa pulę wystąpień o nazwie instancePool0.</span><span class="sxs-lookup"><span data-stu-id="e84be-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="e84be-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e84be-115">PARAMETERS</span></span>

### <span data-ttu-id="e84be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e84be-116">-DefaultProfile</span></span>
<span data-ttu-id="e84be-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e84be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e84be-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e84be-118">-InputObject</span></span>
<span data-ttu-id="e84be-119">Obiekt puli wystąpień do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e84be-119">The instance pool object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e84be-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e84be-120">-Name</span></span>
<span data-ttu-id="e84be-121">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="e84be-121">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e84be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e84be-122">-ResourceGroupName</span></span>
<span data-ttu-id="e84be-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e84be-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e84be-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e84be-124">-ResourceId</span></span>
<span data-ttu-id="e84be-125">Identyfikator zasobu puli wystąpienia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e84be-125">The instance pool resource id to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e84be-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e84be-126">-Confirm</span></span>
<span data-ttu-id="e84be-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e84be-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e84be-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e84be-128">-WhatIf</span></span>
<span data-ttu-id="e84be-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e84be-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e84be-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e84be-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e84be-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e84be-131">CommonParameters</span></span>
<span data-ttu-id="e84be-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e84be-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e84be-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e84be-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e84be-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e84be-134">INPUTS</span></span>

### <span data-ttu-id="e84be-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="e84be-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="e84be-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e84be-136">System.String</span></span>

## <span data-ttu-id="e84be-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e84be-137">OUTPUTS</span></span>

### <span data-ttu-id="e84be-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="e84be-138">System.Object</span></span>
## <span data-ttu-id="e84be-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e84be-139">NOTES</span></span>

## <span data-ttu-id="e84be-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e84be-140">RELATED LINKS</span></span>
