---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 741db1ddd4d2cce236d5a1d6787ea25179aa373f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978001"
---
# <span data-ttu-id="01443-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="01443-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="01443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01443-102">SYNOPSIS</span></span>
<span data-ttu-id="01443-103">Usuwa maszynę wirtualną sql.</span><span class="sxs-lookup"><span data-stu-id="01443-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="01443-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="01443-104">SYNTAX</span></span>

### <span data-ttu-id="01443-105">Nazwa (domyślna)</span><span class="sxs-lookup"><span data-stu-id="01443-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01443-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="01443-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01443-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="01443-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01443-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="01443-108">DESCRIPTION</span></span>
<span data-ttu-id="01443-109">Polecenie Remove-AzSqlVM cmdlet usuwa maszynę wirtualną sql.</span><span class="sxs-lookup"><span data-stu-id="01443-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="01443-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="01443-110">EXAMPLES</span></span>

### <span data-ttu-id="01443-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01443-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="01443-112">Usuwa maszynę wirtualną Azure SQL "maszyny wirtualnej" z grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="01443-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="01443-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01443-113">PARAMETERS</span></span>

### <span data-ttu-id="01443-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="01443-114">-AsJob</span></span>
<span data-ttu-id="01443-115">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="01443-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="01443-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01443-116">-DefaultProfile</span></span>
<span data-ttu-id="01443-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="01443-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01443-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01443-118">-InputObject</span></span>
<span data-ttu-id="01443-119">Obiekt maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="01443-119">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: InputObject
Aliases: SqlVM

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01443-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="01443-120">-Name</span></span>
<span data-ttu-id="01443-121">Nazwa maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="01443-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01443-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01443-122">-PassThru</span></span>
<span data-ttu-id="01443-123">Określa, czy usunięty zasób ma być wyprowadzony na koniec wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01443-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="01443-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01443-124">-ResourceGroupName</span></span>
<span data-ttu-id="01443-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="01443-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="01443-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01443-126">-ResourceId</span></span>
<span data-ttu-id="01443-127">Identyfikator zasobu maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="01443-127">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01443-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01443-128">-Confirm</span></span>
<span data-ttu-id="01443-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="01443-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01443-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01443-130">-WhatIf</span></span>
<span data-ttu-id="01443-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01443-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01443-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="01443-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01443-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01443-133">CommonParameters</span></span>
<span data-ttu-id="01443-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01443-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01443-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01443-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01443-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01443-136">INPUTS</span></span>

### <span data-ttu-id="01443-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="01443-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="01443-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01443-138">OUTPUTS</span></span>

### <span data-ttu-id="01443-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="01443-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="01443-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="01443-140">NOTES</span></span>

## <span data-ttu-id="01443-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01443-141">RELATED LINKS</span></span>
