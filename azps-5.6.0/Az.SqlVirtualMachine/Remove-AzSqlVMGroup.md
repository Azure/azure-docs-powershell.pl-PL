---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: d9d5ee7159f5a7f237bd9194051c99801481f1d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977994"
---
# <span data-ttu-id="34843-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="34843-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="34843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34843-102">SYNOPSIS</span></span>
<span data-ttu-id="34843-103">Usuwa grupę maszyn wirtualnych sql.</span><span class="sxs-lookup"><span data-stu-id="34843-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="34843-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="34843-104">SYNTAX</span></span>

### <span data-ttu-id="34843-105">Lista paramaterów (domyślna)</span><span class="sxs-lookup"><span data-stu-id="34843-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34843-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="34843-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34843-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="34843-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34843-108">Nazwa</span><span class="sxs-lookup"><span data-stu-id="34843-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34843-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="34843-109">DESCRIPTION</span></span>
<span data-ttu-id="34843-110">Polecenie Remove-AzSqlVMGroup cmdlet usuwa grupę maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="34843-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="34843-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="34843-111">EXAMPLES</span></span>

### <span data-ttu-id="34843-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34843-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="34843-113">Usuwa grupę maszyn wirtualnych języka Azure SQL "test-group" w grupie zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="34843-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="34843-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34843-114">PARAMETERS</span></span>

### <span data-ttu-id="34843-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="34843-115">-AsJob</span></span>
<span data-ttu-id="34843-116">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="34843-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="34843-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34843-117">-DefaultProfile</span></span>
<span data-ttu-id="34843-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="34843-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34843-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34843-119">-InputObject</span></span>
<span data-ttu-id="34843-120">Obiekt maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="34843-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34843-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="34843-121">-Name</span></span>
<span data-ttu-id="34843-122">Nazwa grupy maszyn wirtualnych JĘZYKA SQL.</span><span class="sxs-lookup"><span data-stu-id="34843-122">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34843-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34843-123">-PassThru</span></span>
<span data-ttu-id="34843-124">Określa, czy usunięty zasób ma być wyprowadzony na koniec wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34843-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="34843-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34843-125">-ResourceGroupName</span></span>
<span data-ttu-id="34843-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34843-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34843-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34843-127">-ResourceId</span></span>
<span data-ttu-id="34843-128">Identyfikator zasobu grupy maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="34843-128">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34843-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34843-129">-Confirm</span></span>
<span data-ttu-id="34843-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="34843-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34843-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34843-131">-WhatIf</span></span>
<span data-ttu-id="34843-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34843-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34843-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="34843-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34843-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34843-134">CommonParameters</span></span>
<span data-ttu-id="34843-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34843-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34843-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34843-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34843-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34843-137">INPUTS</span></span>

### <span data-ttu-id="34843-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="34843-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="34843-139">System.String</span><span class="sxs-lookup"><span data-stu-id="34843-139">System.String</span></span>

## <span data-ttu-id="34843-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34843-140">OUTPUTS</span></span>

### <span data-ttu-id="34843-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="34843-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="34843-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="34843-142">NOTES</span></span>

## <span data-ttu-id="34843-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34843-143">RELATED LINKS</span></span>
