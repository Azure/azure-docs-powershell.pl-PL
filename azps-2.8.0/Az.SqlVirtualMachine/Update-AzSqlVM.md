---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
ms.openlocfilehash: bfc64aeb344e9913bf72ae7b51559bb613209994
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887626"
---
# <span data-ttu-id="61018-101">Update-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="61018-101">Update-AzSqlVM</span></span>

## <span data-ttu-id="61018-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61018-102">SYNOPSIS</span></span>
<span data-ttu-id="61018-103">Umożliwia zaktualizowanie maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="61018-103">Updates a sql virtual machine.</span></span>

## <span data-ttu-id="61018-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61018-104">SYNTAX</span></span>

### <span data-ttu-id="61018-105">NameParamaterList (domyślny)</span><span class="sxs-lookup"><span data-stu-id="61018-105">NameParamaterList (Default)</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Offer <String>]
 [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61018-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="61018-106">NameInputObject</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <AzureSqlVMModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61018-107">ResourceIdParamaterList</span><span class="sxs-lookup"><span data-stu-id="61018-107">ResourceIdParamaterList</span></span>
```
Update-AzSqlVM [-LicenseType <String>] [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61018-108">ResourceIdInputObject</span><span class="sxs-lookup"><span data-stu-id="61018-108">ResourceIdInputObject</span></span>
```
Update-AzSqlVM [-InputObject] <AzureSqlVMModel> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61018-109">Opis</span><span class="sxs-lookup"><span data-stu-id="61018-109">DESCRIPTION</span></span>
<span data-ttu-id="61018-110">Polecenie cmdlet Update-AzSqlVM umożliwia zaktualizowanie maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="61018-110">The Update-AzSqlVM cmdlet updates a sql virtual machine.</span></span>

## <span data-ttu-id="61018-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61018-111">EXAMPLES</span></span>

### <span data-ttu-id="61018-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="61018-112">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $vm = Update-AzSqlVM -InputObject $vm -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="61018-113">Aktualizuje znaczniki maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="61018-113">Updates the tags of a sql virtual machine.</span></span>

## <span data-ttu-id="61018-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61018-114">PARAMETERS</span></span>

### <span data-ttu-id="61018-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61018-115">-AsJob</span></span>
<span data-ttu-id="61018-116">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="61018-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="61018-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61018-117">-DefaultProfile</span></span>
<span data-ttu-id="61018-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61018-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61018-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="61018-119">-InputObject</span></span>
<span data-ttu-id="61018-120">Obiekt maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="61018-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject, ResourceIdInputObject
Aliases: SqlVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61018-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="61018-121">-LicenseType</span></span>
<span data-ttu-id="61018-122">Typ licencji maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="61018-122">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61018-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61018-123">-Name</span></span>
<span data-ttu-id="61018-124">Nazwa maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="61018-124">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61018-125">-Offer</span><span class="sxs-lookup"><span data-stu-id="61018-125">-Offer</span></span>
<span data-ttu-id="61018-126">Oferta maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="61018-126">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61018-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61018-127">-ResourceGroupName</span></span>
<span data-ttu-id="61018-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61018-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61018-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61018-129">-ResourceId</span></span>
<span data-ttu-id="61018-130">Identyfikator zasobu maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="61018-130">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParamaterList, ResourceIdInputObject
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61018-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="61018-131">-Sku</span></span>
<span data-ttu-id="61018-132">Typ wydania maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="61018-132">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61018-133">-Sqlmanagementtype</span><span class="sxs-lookup"><span data-stu-id="61018-133">-SqlManagementType</span></span>
<span data-ttu-id="61018-134">Typ zarządzania maszyną wirtualną SQL.</span><span class="sxs-lookup"><span data-stu-id="61018-134">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61018-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="61018-135">-Tag</span></span>
<span data-ttu-id="61018-136">Tagi, które mają zostać skojarzone z maszyną wirtualną SQL</span><span class="sxs-lookup"><span data-stu-id="61018-136">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61018-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61018-137">-Confirm</span></span>
<span data-ttu-id="61018-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61018-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61018-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61018-139">-WhatIf</span></span>
<span data-ttu-id="61018-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61018-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61018-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61018-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61018-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61018-142">CommonParameters</span></span>
<span data-ttu-id="61018-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61018-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61018-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61018-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61018-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61018-145">INPUTS</span></span>

### <span data-ttu-id="61018-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="61018-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="61018-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61018-147">OUTPUTS</span></span>

### <span data-ttu-id="61018-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="61018-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="61018-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61018-149">NOTES</span></span>

## <span data-ttu-id="61018-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61018-150">RELATED LINKS</span></span>
