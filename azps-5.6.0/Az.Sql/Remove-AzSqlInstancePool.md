---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: 0a7874079b7de782fa7471e9087f04fdc3a9e754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967409"
---
# <span data-ttu-id="aaf2f-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="aaf2f-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="aaf2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaf2f-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf2f-103">Usuwa pulę wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="aaf2f-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="aaf2f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aaf2f-104">SYNTAX</span></span>

### <span data-ttu-id="aaf2f-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="aaf2f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaf2f-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaf2f-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaf2f-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaf2f-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aaf2f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="aaf2f-108">DESCRIPTION</span></span>
<span data-ttu-id="aaf2f-109">Polecenie **cmdlet Remove-AzSqlInstancePool** usuwa pulę wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="aaf2f-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="aaf2f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aaf2f-110">EXAMPLES</span></span>

### <span data-ttu-id="aaf2f-111">Przykład 1. Usuwanie puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="aaf2f-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="aaf2f-112">Przykład 2. Usuwanie puli wystąpień za pomocą identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="aaf2f-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="aaf2f-113">Przykład 3. Usuwanie puli wystąpień przez obiekt puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="aaf2f-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="aaf2f-114">To polecenie usuwa pulę wystąpień o nazwie instancePool0.</span><span class="sxs-lookup"><span data-stu-id="aaf2f-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="aaf2f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaf2f-115">PARAMETERS</span></span>

### <span data-ttu-id="aaf2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf2f-116">-DefaultProfile</span></span>
<span data-ttu-id="aaf2f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf2f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaf2f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaf2f-118">-InputObject</span></span>
<span data-ttu-id="aaf2f-119">Obiekt puli wystąpień do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="aaf2f-119">The instance pool object to remove.</span></span>

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

### <span data-ttu-id="aaf2f-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="aaf2f-120">-Name</span></span>
<span data-ttu-id="aaf2f-121">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="aaf2f-121">The name of the instance pool.</span></span>

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

### <span data-ttu-id="aaf2f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf2f-122">-ResourceGroupName</span></span>
<span data-ttu-id="aaf2f-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aaf2f-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="aaf2f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaf2f-124">-ResourceId</span></span>
<span data-ttu-id="aaf2f-125">Identyfikator zasobu puli wystąpienia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="aaf2f-125">The instance pool resource id to remove.</span></span>

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

### <span data-ttu-id="aaf2f-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aaf2f-126">-Confirm</span></span>
<span data-ttu-id="aaf2f-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aaf2f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaf2f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaf2f-128">-WhatIf</span></span>
<span data-ttu-id="aaf2f-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaf2f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaf2f-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="aaf2f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaf2f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf2f-131">CommonParameters</span></span>
<span data-ttu-id="aaf2f-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf2f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf2f-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aaf2f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf2f-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aaf2f-134">INPUTS</span></span>

### <span data-ttu-id="aaf2f-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="aaf2f-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="aaf2f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="aaf2f-136">System.String</span></span>

## <span data-ttu-id="aaf2f-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aaf2f-137">OUTPUTS</span></span>

### <span data-ttu-id="aaf2f-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="aaf2f-138">System.Object</span></span>
## <span data-ttu-id="aaf2f-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aaf2f-139">NOTES</span></span>

## <span data-ttu-id="aaf2f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aaf2f-140">RELATED LINKS</span></span>
