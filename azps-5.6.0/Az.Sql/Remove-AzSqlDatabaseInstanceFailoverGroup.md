---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 0e3bfc112ee8c80d08b0b5a87eb574a4c5bdb29e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957937"
---
# <span data-ttu-id="627b4-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="627b4-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="627b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="627b4-102">SYNOPSIS</span></span>
<span data-ttu-id="627b4-103">Usuwa grupę trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="627b4-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="627b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="627b4-104">SYNTAX</span></span>

### <span data-ttu-id="627b4-105">RemoveIFGDefaultSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="627b4-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="627b4-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="627b4-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="627b4-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="627b4-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="627b4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="627b4-108">DESCRIPTION</span></span>
<span data-ttu-id="627b4-109">To polecenie usuwa grupę wystąpienia trybu failover o określonej nazwie, pozostawiając wszystkie bazy danych bez zmian.</span><span class="sxs-lookup"><span data-stu-id="627b4-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="627b4-110">Punkt końcowy słuchacza nie zostanie wyrejestrowany z systemu DNS.</span><span class="sxs-lookup"><span data-stu-id="627b4-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="627b4-111">Do wykonania polecenia należy użyć podstawowego obszaru grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="627b4-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="627b4-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="627b4-112">EXAMPLES</span></span>

### <span data-ttu-id="627b4-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="627b4-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="627b4-114">Usuwanie grupy trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="627b4-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="627b4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="627b4-115">PARAMETERS</span></span>

### <span data-ttu-id="627b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627b4-116">-DefaultProfile</span></span>
<span data-ttu-id="627b4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="627b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="627b4-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="627b4-118">-Force</span></span>
<span data-ttu-id="627b4-119">Pomiń komunikat potwierdzenia wykonania akcji.</span><span class="sxs-lookup"><span data-stu-id="627b4-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="627b4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="627b4-120">-InputObject</span></span>
<span data-ttu-id="627b4-121">Obiekt Grupy trybu failover wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="627b4-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="627b4-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="627b4-122">-Location</span></span>
<span data-ttu-id="627b4-123">Nazwa regionu lokalnego, z którego ma zostać pobrana grupa trybu failover wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="627b4-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet, RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b4-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="627b4-124">-Name</span></span>
<span data-ttu-id="627b4-125">Nazwa grupy trybu failover wystąpienia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="627b4-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="627b4-126">-PassThru</span></span>
<span data-ttu-id="627b4-127">Określa, czy dane wyjściowe wykonywania polecenia cmdlet mają być przechodzą przez ten proces.</span><span class="sxs-lookup"><span data-stu-id="627b4-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="627b4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="627b4-128">-ResourceGroupName</span></span>
<span data-ttu-id="627b4-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="627b4-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="627b4-130">-ResourceId</span></span>
<span data-ttu-id="627b4-131">Identyfikator zasobu grupy trybu failover wystąpienia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="627b4-131">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="627b4-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="627b4-132">-Confirm</span></span>
<span data-ttu-id="627b4-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="627b4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="627b4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="627b4-134">-WhatIf</span></span>
<span data-ttu-id="627b4-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="627b4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="627b4-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="627b4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="627b4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627b4-137">CommonParameters</span></span>
<span data-ttu-id="627b4-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="627b4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627b4-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="627b4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627b4-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="627b4-140">INPUTS</span></span>

### <span data-ttu-id="627b4-141">Microsoft.Azure.Commands.sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="627b4-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="627b4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="627b4-142">System.String</span></span>

## <span data-ttu-id="627b4-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="627b4-143">OUTPUTS</span></span>

### <span data-ttu-id="627b4-144">Microsoft.Azure.Commands.sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="627b4-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="627b4-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="627b4-145">NOTES</span></span>

## <span data-ttu-id="627b4-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="627b4-146">RELATED LINKS</span></span>
