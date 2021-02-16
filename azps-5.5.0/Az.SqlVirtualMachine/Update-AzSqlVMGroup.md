---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195882"
---
# <span data-ttu-id="80c6d-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="80c6d-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="80c6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="80c6d-103">Aktualizuje grupę maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="80c6d-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="80c6d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="80c6d-104">SYNTAX</span></span>

### <span data-ttu-id="80c6d-105">Nazwa (domyślna)</span><span class="sxs-lookup"><span data-stu-id="80c6d-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80c6d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="80c6d-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80c6d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="80c6d-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c6d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="80c6d-108">DESCRIPTION</span></span>
<span data-ttu-id="80c6d-109">Polecenie Update-AzSqlVMGroup aktualizuje grupę maszyn wirtualnych sql.</span><span class="sxs-lookup"><span data-stu-id="80c6d-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="80c6d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="80c6d-110">EXAMPLES</span></span>

### <span data-ttu-id="80c6d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="80c6d-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="80c6d-112">Aktualizuje tagi grupy maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="80c6d-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="80c6d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80c6d-113">PARAMETERS</span></span>

### <span data-ttu-id="80c6d-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="80c6d-114">-AsJob</span></span>
<span data-ttu-id="80c6d-115">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="80c6d-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="80c6d-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="80c6d-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="80c6d-117">Nazwa używana do tworzenia klastrów</span><span class="sxs-lookup"><span data-stu-id="80c6d-117">Name used for creating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c6d-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="80c6d-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="80c6d-119">Nazwa używana dla klastrów operacyjnych</span><span class="sxs-lookup"><span data-stu-id="80c6d-119">Name used for operating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c6d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c6d-120">-DefaultProfile</span></span>
<span data-ttu-id="80c6d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="80c6d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80c6d-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="80c6d-122">-DomainFqdn</span></span>
<span data-ttu-id="80c6d-123">W pełni kwalifikowana nazwa domeny</span><span class="sxs-lookup"><span data-stu-id="80c6d-123">Fully qualified name of the domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c6d-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="80c6d-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="80c6d-125">Opcjonalna ścieżka dla zdarzenia z udostępnianiem plików</span><span class="sxs-lookup"><span data-stu-id="80c6d-125">Optional path for fileshare witness</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c6d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80c6d-126">-InputObject</span></span>
<span data-ttu-id="80c6d-127">Obiekt maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="80c6d-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="80c6d-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="80c6d-128">-Name</span></span>
<span data-ttu-id="80c6d-129">Nazwa grupy maszyn wirtualnych JĘZYKA SQL.</span><span class="sxs-lookup"><span data-stu-id="80c6d-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="80c6d-130">— OuPath</span><span class="sxs-lookup"><span data-stu-id="80c6d-130">-OuPath</span></span>
<span data-ttu-id="80c6d-131">Ścieżka jednostki organizacyjnej, w której będą obecne węzły i klaster</span><span class="sxs-lookup"><span data-stu-id="80c6d-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c6d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c6d-132">-ResourceGroupName</span></span>
<span data-ttu-id="80c6d-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="80c6d-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="80c6d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80c6d-134">-ResourceId</span></span>
<span data-ttu-id="80c6d-135">Identyfikator zasobu grupy maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="80c6d-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="80c6d-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="80c6d-136">-SqlServiceAccount</span></span>
<span data-ttu-id="80c6d-137">Nazwa, pod którą usługa SQL będzie działać na wszystkich komputerach wirtualnych SQL uczestniczących w klastrze</span><span class="sxs-lookup"><span data-stu-id="80c6d-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c6d-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="80c6d-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="80c6d-139">Klucz podstawowy konta magazynu dla chętnych</span><span class="sxs-lookup"><span data-stu-id="80c6d-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c6d-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="80c6d-140">-StorageAccountUrl</span></span>
<span data-ttu-id="80c6d-141">Klucz podstawowy konta magazynu dla chętnych</span><span class="sxs-lookup"><span data-stu-id="80c6d-141">Primary key of the witness storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c6d-142">— Tag</span><span class="sxs-lookup"><span data-stu-id="80c6d-142">-Tag</span></span>
<span data-ttu-id="80c6d-143">Tagi, które należy skojarzyć z grupą maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="80c6d-143">The tags to associate with the SQL virtual machine group.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c6d-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80c6d-144">-Confirm</span></span>
<span data-ttu-id="80c6d-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="80c6d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c6d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c6d-146">-WhatIf</span></span>
<span data-ttu-id="80c6d-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c6d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c6d-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="80c6d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c6d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c6d-149">CommonParameters</span></span>
<span data-ttu-id="80c6d-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80c6d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c6d-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80c6d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c6d-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80c6d-152">INPUTS</span></span>

### <span data-ttu-id="80c6d-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="80c6d-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="80c6d-154">System.String</span><span class="sxs-lookup"><span data-stu-id="80c6d-154">System.String</span></span>

## <span data-ttu-id="80c6d-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="80c6d-155">OUTPUTS</span></span>

### <span data-ttu-id="80c6d-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="80c6d-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="80c6d-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="80c6d-157">NOTES</span></span>

## <span data-ttu-id="80c6d-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80c6d-158">RELATED LINKS</span></span>
