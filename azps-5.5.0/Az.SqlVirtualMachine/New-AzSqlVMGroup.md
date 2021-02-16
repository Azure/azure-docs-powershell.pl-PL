---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: 0cd409f530225b2fadf104f787a1e926b5f8fb16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201387"
---
# <span data-ttu-id="11a17-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="11a17-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="11a17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11a17-102">SYNOPSIS</span></span>
<span data-ttu-id="11a17-103">Tworzy nową grupę maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="11a17-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="11a17-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11a17-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11a17-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="11a17-105">DESCRIPTION</span></span>
<span data-ttu-id="11a17-106">Polecenie New-AzSqlVMGroup cmdlet tworzy grupę maszyn wirtualnych języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="11a17-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="11a17-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11a17-107">EXAMPLES</span></span>

### <span data-ttu-id="11a17-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11a17-108">Example 1</span></span>
```powershell
PS C:\> $secureKey = ConvertTo-SecureString $profile.StorageAccountPrimaryKey -AsPlainText -Force
PS C:\> New-AzSqlVMGroup $resourceGroupName $groupName $location -ClusterOperatorAccount $profile.ClusterOperatorAccount `
>>         -SqlServiceAccount $profile.SqlServiceAccount -StorageAccountUrl $profile.StorageAccountUrl `
>>         -StorageAccountPrimaryKey $secureKey -DomainFqdn $profile.DomainFqdn `
>>         -Offer 'SQL2017-WS2016' -Sku 'Developer'
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="11a17-109">Tworzy nową grupę maszyn wirtualnych języka Azure SQL z maszyną wirtualnej grupy testowej w grupie zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="11a17-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="11a17-110">$profile obiekt typu Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span><span class="sxs-lookup"><span data-stu-id="11a17-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="11a17-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11a17-111">PARAMETERS</span></span>

### <span data-ttu-id="11a17-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="11a17-112">-AsJob</span></span>
<span data-ttu-id="11a17-113">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="11a17-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="11a17-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="11a17-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="11a17-115">Nazwa używana do tworzenia klastrów</span><span class="sxs-lookup"><span data-stu-id="11a17-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="11a17-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="11a17-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="11a17-117">Nazwa używana dla klastrów operacyjnych</span><span class="sxs-lookup"><span data-stu-id="11a17-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="11a17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a17-118">-DefaultProfile</span></span>
<span data-ttu-id="11a17-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11a17-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11a17-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="11a17-120">-DomainFqdn</span></span>
<span data-ttu-id="11a17-121">W pełni kwalifikowana nazwa domeny</span><span class="sxs-lookup"><span data-stu-id="11a17-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="11a17-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="11a17-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="11a17-123">Opcjonalna ścieżka dla zdarzenia z udostępnianiem plików</span><span class="sxs-lookup"><span data-stu-id="11a17-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="11a17-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="11a17-124">-Location</span></span>
<span data-ttu-id="11a17-125">Lokalizacja grupy maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="11a17-125">SQL virtual machine group location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a17-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11a17-126">-Name</span></span>
<span data-ttu-id="11a17-127">Nazwa grupy maszyn wirtualnych JĘZYKA SQL.</span><span class="sxs-lookup"><span data-stu-id="11a17-127">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a17-128">— Oferta</span><span class="sxs-lookup"><span data-stu-id="11a17-128">-Offer</span></span>
<span data-ttu-id="11a17-129">Oferta grupy maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="11a17-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="11a17-130">— OuPath</span><span class="sxs-lookup"><span data-stu-id="11a17-130">-OuPath</span></span>
<span data-ttu-id="11a17-131">Ścieżka jednostki organizacyjnej, w której będą obecne węzły i klaster</span><span class="sxs-lookup"><span data-stu-id="11a17-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="11a17-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11a17-132">-ResourceGroupName</span></span>
<span data-ttu-id="11a17-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11a17-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="11a17-134">- SKU</span><span class="sxs-lookup"><span data-stu-id="11a17-134">-Sku</span></span>
<span data-ttu-id="11a17-135">Typ wersji sql virtual machine group.</span><span class="sxs-lookup"><span data-stu-id="11a17-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="11a17-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="11a17-136">-SqlServiceAccount</span></span>
<span data-ttu-id="11a17-137">Nazwa, pod którą usługa SQL będzie działać na wszystkich komputerach wirtualnych SQL uczestniczących w klastrze</span><span class="sxs-lookup"><span data-stu-id="11a17-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="11a17-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="11a17-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="11a17-139">Klucz podstawowy konta magazynu dla chętnych</span><span class="sxs-lookup"><span data-stu-id="11a17-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11a17-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="11a17-140">-StorageAccountUrl</span></span>
<span data-ttu-id="11a17-141">Klucz podstawowy konta magazynu dla chętnych</span><span class="sxs-lookup"><span data-stu-id="11a17-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="11a17-142">— Tag</span><span class="sxs-lookup"><span data-stu-id="11a17-142">-Tag</span></span>
<span data-ttu-id="11a17-143">Tagi, które należy skojarzyć z grupą maszyn wirtualnych JĘZYKA SQL.</span><span class="sxs-lookup"><span data-stu-id="11a17-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="11a17-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11a17-144">-Confirm</span></span>
<span data-ttu-id="11a17-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11a17-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11a17-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11a17-146">-WhatIf</span></span>
<span data-ttu-id="11a17-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11a17-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11a17-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11a17-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11a17-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a17-149">CommonParameters</span></span>
<span data-ttu-id="11a17-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11a17-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a17-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11a17-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a17-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11a17-152">INPUTS</span></span>

### <span data-ttu-id="11a17-153">System.String</span><span class="sxs-lookup"><span data-stu-id="11a17-153">System.String</span></span>

## <span data-ttu-id="11a17-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11a17-154">OUTPUTS</span></span>

### <span data-ttu-id="11a17-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="11a17-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="11a17-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11a17-156">NOTES</span></span>

## <span data-ttu-id="11a17-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11a17-157">RELATED LINKS</span></span>
