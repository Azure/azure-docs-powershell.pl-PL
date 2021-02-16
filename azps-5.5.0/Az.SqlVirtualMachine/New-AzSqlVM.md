---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201394"
---
# <span data-ttu-id="23449-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="23449-101">New-AzSqlVM</span></span>

## <span data-ttu-id="23449-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23449-102">SYNOPSIS</span></span>
<span data-ttu-id="23449-103">Tworzy nową maszynę wirtualną sql.</span><span class="sxs-lookup"><span data-stu-id="23449-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="23449-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="23449-104">SYNTAX</span></span>

### <span data-ttu-id="23449-105">NameParamaterList (Default)</span><span class="sxs-lookup"><span data-stu-id="23449-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23449-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="23449-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23449-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="23449-107">DESCRIPTION</span></span>
<span data-ttu-id="23449-108">Polecenie New-AzSqlVM cmdlet tworzy maszynę wirtualną języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="23449-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="23449-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="23449-109">EXAMPLES</span></span>

### <span data-ttu-id="23449-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23449-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="23449-111">Tworzy nową maszynę wirtualną azure SQL z nazwą maszyny wirtualnej w grupie zasobów ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="23449-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="23449-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23449-112">PARAMETERS</span></span>

### <span data-ttu-id="23449-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="23449-113">-AsJob</span></span>
<span data-ttu-id="23449-114">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="23449-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="23449-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23449-115">-DefaultProfile</span></span>
<span data-ttu-id="23449-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="23449-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23449-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="23449-117">-LicenseType</span></span>
<span data-ttu-id="23449-118">Typ licencji na maszynę wirtualną SQL.</span><span class="sxs-lookup"><span data-stu-id="23449-118">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23449-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="23449-119">-Location</span></span>
<span data-ttu-id="23449-120">Lokalizacja maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="23449-120">SQL virtual machine location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23449-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="23449-121">-Name</span></span>
<span data-ttu-id="23449-122">Nazwa maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="23449-122">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23449-123">— Oferta</span><span class="sxs-lookup"><span data-stu-id="23449-123">-Offer</span></span>
<span data-ttu-id="23449-124">Oferta na maszynę wirtualną SQL.</span><span class="sxs-lookup"><span data-stu-id="23449-124">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23449-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23449-125">-ResourceGroupName</span></span>
<span data-ttu-id="23449-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23449-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23449-127">- SKU</span><span class="sxs-lookup"><span data-stu-id="23449-127">-Sku</span></span>
<span data-ttu-id="23449-128">Typ wersji programu SQL Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="23449-128">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23449-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="23449-129">-SqlManagementType</span></span>
<span data-ttu-id="23449-130">Typ zarządzania maszynami wirtualnymi SQL.</span><span class="sxs-lookup"><span data-stu-id="23449-130">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23449-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="23449-131">-SqlVM</span></span>
<span data-ttu-id="23449-132">Obiekt maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="23449-132">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23449-133">— Tag</span><span class="sxs-lookup"><span data-stu-id="23449-133">-Tag</span></span>
<span data-ttu-id="23449-134">Tagi do skojarzenia z maszyną wirtualną SQL</span><span class="sxs-lookup"><span data-stu-id="23449-134">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23449-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23449-135">-Confirm</span></span>
<span data-ttu-id="23449-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="23449-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23449-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23449-137">-WhatIf</span></span>
<span data-ttu-id="23449-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23449-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23449-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="23449-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23449-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23449-140">CommonParameters</span></span>
<span data-ttu-id="23449-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23449-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23449-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23449-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23449-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23449-143">INPUTS</span></span>

### <span data-ttu-id="23449-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="23449-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="23449-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23449-145">OUTPUTS</span></span>

### <span data-ttu-id="23449-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="23449-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="23449-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="23449-147">NOTES</span></span>

## <span data-ttu-id="23449-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23449-148">RELATED LINKS</span></span>
