---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188923"
---
# <span data-ttu-id="c9b84-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c9b84-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="c9b84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9b84-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b84-103">Usuwa wystąpienie zarządzanej bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c9b84-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="c9b84-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9b84-104">SYNTAX</span></span>

### <span data-ttu-id="c9b84-105">RemoveInstanceFromInputParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c9b84-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9b84-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="c9b84-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9b84-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="c9b84-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9b84-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9b84-108">DESCRIPTION</span></span>
<span data-ttu-id="c9b84-109">Polecenie **cmdlet Remove-AzSqlInstance** usuwa wystąpienie zarządzane usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="c9b84-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="c9b84-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9b84-110">EXAMPLES</span></span>

### <span data-ttu-id="c9b84-111">Przykład 1. Usuwanie wystąpienia</span><span class="sxs-lookup"><span data-stu-id="c9b84-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c9b84-112">To polecenie usuwa wystąpienie o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="c9b84-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="c9b84-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9b84-113">PARAMETERS</span></span>

### <span data-ttu-id="c9b84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b84-114">-DefaultProfile</span></span>
<span data-ttu-id="c9b84-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b84-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9b84-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c9b84-116">-Force</span></span>
<span data-ttu-id="c9b84-117">Pomiń komunikat z potwierdzeniem wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="c9b84-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c9b84-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9b84-118">-InputObject</span></span>
<span data-ttu-id="c9b84-119">Obiekt AzureSqlManagedInstanceModel do usunięcia</span><span class="sxs-lookup"><span data-stu-id="c9b84-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9b84-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c9b84-120">-Name</span></span>
<span data-ttu-id="c9b84-121">Nazwa wystąpienia języka SQL.</span><span class="sxs-lookup"><span data-stu-id="c9b84-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b84-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b84-122">-ResourceGroupName</span></span>
<span data-ttu-id="c9b84-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9b84-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b84-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9b84-124">-ResourceId</span></span>
<span data-ttu-id="c9b84-125">Identyfikator zasobu obiektu wystąpienia do usunięcia</span><span class="sxs-lookup"><span data-stu-id="c9b84-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9b84-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9b84-126">-Confirm</span></span>
<span data-ttu-id="c9b84-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9b84-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9b84-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9b84-128">-WhatIf</span></span>
<span data-ttu-id="c9b84-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9b84-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9b84-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c9b84-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9b84-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b84-131">CommonParameters</span></span>
<span data-ttu-id="c9b84-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b84-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b84-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9b84-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b84-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9b84-134">INPUTS</span></span>

### <span data-ttu-id="c9b84-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c9b84-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="c9b84-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c9b84-136">System.String</span></span>

## <span data-ttu-id="c9b84-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9b84-137">OUTPUTS</span></span>

### <span data-ttu-id="c9b84-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c9b84-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="c9b84-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9b84-139">NOTES</span></span>

## <span data-ttu-id="c9b84-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9b84-140">RELATED LINKS</span></span>
