---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052163"
---
# <span data-ttu-id="4e797-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4e797-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="4e797-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e797-102">SYNOPSIS</span></span>
<span data-ttu-id="4e797-103">Usuwa grupę wystąpień awaryjnych.</span><span class="sxs-lookup"><span data-stu-id="4e797-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="4e797-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e797-104">SYNTAX</span></span>

### <span data-ttu-id="4e797-105">RemoveIFGDefaultSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4e797-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e797-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e797-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e797-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="4e797-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e797-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4e797-108">DESCRIPTION</span></span>
<span data-ttu-id="4e797-109">To polecenie usuwa grupę awaryjną wystąpienia o określonej nazwie, pozostawiając wszystkie bazy danych nienaruszone.</span><span class="sxs-lookup"><span data-stu-id="4e797-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="4e797-110">Punkt końcowy odbiornika zostanie wyrejestrowany z systemu DNS.</span><span class="sxs-lookup"><span data-stu-id="4e797-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="4e797-111">Aby wykonać polecenie, należy użyć głównego regionu grupy tryb failover.</span><span class="sxs-lookup"><span data-stu-id="4e797-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="4e797-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e797-112">EXAMPLES</span></span>

### <span data-ttu-id="4e797-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4e797-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="4e797-114">Usuwanie grupy wystąpień awaryjnych.</span><span class="sxs-lookup"><span data-stu-id="4e797-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="4e797-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e797-115">PARAMETERS</span></span>

### <span data-ttu-id="4e797-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e797-116">-DefaultProfile</span></span>
<span data-ttu-id="4e797-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e797-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e797-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4e797-118">-Force</span></span>
<span data-ttu-id="4e797-119">Pomiń komunikat potwierdzający wykonanie akcji.</span><span class="sxs-lookup"><span data-stu-id="4e797-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="4e797-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4e797-120">-InputObject</span></span>
<span data-ttu-id="4e797-121">Obiekt grupy trybu failover wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="4e797-121">The Instance Failover Group object to remove</span></span>

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

### <span data-ttu-id="4e797-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4e797-122">-Location</span></span>
<span data-ttu-id="4e797-123">Nazwa regionu lokalnego, z którego ma zostać pobrana Grupa wystąpienie trybu failover.</span><span class="sxs-lookup"><span data-stu-id="4e797-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4e797-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4e797-124">-Name</span></span>
<span data-ttu-id="4e797-125">Nazwa grupy tryb failover wystąpienia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="4e797-125">The name of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="4e797-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e797-126">-PassThru</span></span>
<span data-ttu-id="4e797-127">Określa, czy dane wyjściowe wykonania polecenia cmdlet mają być przekazywane.</span><span class="sxs-lookup"><span data-stu-id="4e797-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="4e797-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e797-128">-ResourceGroupName</span></span>
<span data-ttu-id="4e797-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4e797-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e797-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e797-130">-ResourceId</span></span>
<span data-ttu-id="4e797-131">Identyfikator zasobu grupy trybu failover wystąpienia do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="4e797-131">The Resource ID of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="4e797-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e797-132">-Confirm</span></span>
<span data-ttu-id="4e797-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e797-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e797-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e797-134">-WhatIf</span></span>
<span data-ttu-id="4e797-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e797-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e797-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4e797-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e797-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e797-137">CommonParameters</span></span>
<span data-ttu-id="4e797-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e797-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e797-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e797-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e797-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e797-140">INPUTS</span></span>

### <span data-ttu-id="4e797-141">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4e797-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="4e797-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4e797-142">System.String</span></span>

## <span data-ttu-id="4e797-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e797-143">OUTPUTS</span></span>

### <span data-ttu-id="4e797-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4e797-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="4e797-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e797-145">NOTES</span></span>

## <span data-ttu-id="4e797-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e797-146">RELATED LINKS</span></span>
