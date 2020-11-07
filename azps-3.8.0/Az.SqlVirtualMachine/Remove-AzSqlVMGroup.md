---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: fec35992f96940dc69cdb6d1777d43ca151688bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895550"
---
# <span data-ttu-id="bceb0-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="bceb0-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="bceb0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bceb0-102">SYNOPSIS</span></span>
<span data-ttu-id="bceb0-103">Usuwa grupę maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="bceb0-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="bceb0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bceb0-104">SYNTAX</span></span>

### <span data-ttu-id="bceb0-105">ParamaterList (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bceb0-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bceb0-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="bceb0-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bceb0-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="bceb0-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bceb0-108">Nazwę</span><span class="sxs-lookup"><span data-stu-id="bceb0-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bceb0-109">Opis</span><span class="sxs-lookup"><span data-stu-id="bceb0-109">DESCRIPTION</span></span>
<span data-ttu-id="bceb0-110">Polecenie cmdlet Remove-AzSqlVMGroup usuwa grupę maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="bceb0-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="bceb0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bceb0-111">EXAMPLES</span></span>

### <span data-ttu-id="bceb0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bceb0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="bceb0-113">Usuwa grupę maszyn wirtualnych SQL Azure "test-Group" w ResourceGroup01 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bceb0-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="bceb0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bceb0-114">PARAMETERS</span></span>

### <span data-ttu-id="bceb0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bceb0-115">-AsJob</span></span>
<span data-ttu-id="bceb0-116">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="bceb0-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="bceb0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bceb0-117">-DefaultProfile</span></span>
<span data-ttu-id="bceb0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bceb0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bceb0-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bceb0-119">-InputObject</span></span>
<span data-ttu-id="bceb0-120">Obiekt maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="bceb0-120">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="bceb0-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bceb0-121">-Name</span></span>
<span data-ttu-id="bceb0-122">Nazwa grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="bceb0-122">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="bceb0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bceb0-123">-PassThru</span></span>
<span data-ttu-id="bceb0-124">Określa, czy usunięty zasób ma być wyprowadzany na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bceb0-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="bceb0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bceb0-125">-ResourceGroupName</span></span>
<span data-ttu-id="bceb0-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bceb0-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="bceb0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bceb0-127">-ResourceId</span></span>
<span data-ttu-id="bceb0-128">Identyfikator zasobu grupy maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="bceb0-128">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="bceb0-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bceb0-129">-Confirm</span></span>
<span data-ttu-id="bceb0-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bceb0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bceb0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bceb0-131">-WhatIf</span></span>
<span data-ttu-id="bceb0-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bceb0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bceb0-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bceb0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bceb0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bceb0-134">CommonParameters</span></span>
<span data-ttu-id="bceb0-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bceb0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bceb0-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bceb0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bceb0-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bceb0-137">INPUTS</span></span>

### <span data-ttu-id="bceb0-138">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="bceb0-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="bceb0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bceb0-139">System.String</span></span>

## <span data-ttu-id="bceb0-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bceb0-140">OUTPUTS</span></span>

### <span data-ttu-id="bceb0-141">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="bceb0-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="bceb0-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bceb0-142">NOTES</span></span>

## <span data-ttu-id="bceb0-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bceb0-143">RELATED LINKS</span></span>
