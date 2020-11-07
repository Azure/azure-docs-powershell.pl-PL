---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: ea86c4e0a016ae2b33c7853ba9851762a7d8ca54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887625"
---
# <span data-ttu-id="b450f-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="b450f-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="b450f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b450f-102">SYNOPSIS</span></span>
<span data-ttu-id="b450f-103">Umożliwia zaktualizowanie grupy maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="b450f-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="b450f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b450f-104">SYNTAX</span></span>

### <span data-ttu-id="b450f-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b450f-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b450f-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="b450f-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b450f-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="b450f-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b450f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b450f-108">DESCRIPTION</span></span>
<span data-ttu-id="b450f-109">Polecenie cmdlet Update-AzSqlVMGroup aktualizuje grupę maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="b450f-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="b450f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b450f-110">EXAMPLES</span></span>

### <span data-ttu-id="b450f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b450f-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="b450f-112">Aktualizuje znaczniki grupy maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="b450f-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="b450f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b450f-113">PARAMETERS</span></span>

### <span data-ttu-id="b450f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b450f-114">-AsJob</span></span>
<span data-ttu-id="b450f-115">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="b450f-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b450f-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="b450f-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="b450f-117">Nazwa używana do tworzenia klastra</span><span class="sxs-lookup"><span data-stu-id="b450f-117">Name used for creating cluster</span></span>

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

### <span data-ttu-id="b450f-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="b450f-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="b450f-119">Nazwa używana przez klaster operacyjny</span><span class="sxs-lookup"><span data-stu-id="b450f-119">Name used for operating cluster</span></span>

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

### <span data-ttu-id="b450f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b450f-120">-DefaultProfile</span></span>
<span data-ttu-id="b450f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b450f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b450f-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="b450f-122">-DomainFqdn</span></span>
<span data-ttu-id="b450f-123">W pełni kwalifikowana nazwa domeny</span><span class="sxs-lookup"><span data-stu-id="b450f-123">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="b450f-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="b450f-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="b450f-125">Opcjonalna ścieżka monitora</span><span class="sxs-lookup"><span data-stu-id="b450f-125">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="b450f-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b450f-126">-InputObject</span></span>
<span data-ttu-id="b450f-127">Obiekt maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="b450f-127">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="b450f-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b450f-128">-Name</span></span>
<span data-ttu-id="b450f-129">Nazwa grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="b450f-129">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="b450f-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="b450f-130">-OuPath</span></span>
<span data-ttu-id="b450f-131">Ścieżka jednostki organizacyjnej, w której znajdują się węzły i klaster</span><span class="sxs-lookup"><span data-stu-id="b450f-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="b450f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b450f-132">-ResourceGroupName</span></span>
<span data-ttu-id="b450f-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b450f-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="b450f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b450f-134">-ResourceId</span></span>
<span data-ttu-id="b450f-135">Identyfikator zasobu grupy maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="b450f-135">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="b450f-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="b450f-136">-SqlServiceAccount</span></span>
<span data-ttu-id="b450f-137">Nazwa, pod którą usługa SQL będzie uruchamiana na wszystkich uczestniczących maszynach wirtualnych SQL w klastrze</span><span class="sxs-lookup"><span data-stu-id="b450f-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="b450f-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b450f-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="b450f-139">Klucz podstawowy konta magazynu monitora</span><span class="sxs-lookup"><span data-stu-id="b450f-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="b450f-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="b450f-140">-StorageAccountUrl</span></span>
<span data-ttu-id="b450f-141">Klucz podstawowy konta magazynu monitora</span><span class="sxs-lookup"><span data-stu-id="b450f-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="b450f-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="b450f-142">-Tag</span></span>
<span data-ttu-id="b450f-143">Tagi, które mają zostać skojarzone z grupą maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="b450f-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="b450f-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b450f-144">-Confirm</span></span>
<span data-ttu-id="b450f-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b450f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b450f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b450f-146">-WhatIf</span></span>
<span data-ttu-id="b450f-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b450f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b450f-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b450f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b450f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b450f-149">CommonParameters</span></span>
<span data-ttu-id="b450f-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b450f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b450f-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b450f-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b450f-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b450f-152">INPUTS</span></span>

### <span data-ttu-id="b450f-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="b450f-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="b450f-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b450f-154">System.String</span></span>

## <span data-ttu-id="b450f-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b450f-155">OUTPUTS</span></span>

### <span data-ttu-id="b450f-156">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="b450f-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="b450f-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b450f-157">NOTES</span></span>

## <span data-ttu-id="b450f-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b450f-158">RELATED LINKS</span></span>
