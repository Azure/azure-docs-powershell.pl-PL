---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: 0cd409f530225b2fadf104f787a1e926b5f8fb16
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334441"
---
# <span data-ttu-id="e8d92-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="e8d92-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="e8d92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8d92-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d92-103">Tworzy nową grupę maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="e8d92-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="e8d92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8d92-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8d92-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8d92-105">DESCRIPTION</span></span>
<span data-ttu-id="e8d92-106">Polecenie cmdlet New-AzSqlVMGroup służy do tworzenia grupy maszyn wirtualnych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e8d92-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="e8d92-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8d92-107">EXAMPLES</span></span>

### <span data-ttu-id="e8d92-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8d92-108">Example 1</span></span>
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

<span data-ttu-id="e8d92-109">Tworzy nową grupę maszyn wirtualnych SQL Azure z maszyną wirtualną grupy testowej w ResourceGroup01 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8d92-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="e8d92-110">$profile to obiekt typu Microsoft. Azure. Management. SqlVirtualMachine. models. WsfcDomainProfile</span><span class="sxs-lookup"><span data-stu-id="e8d92-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="e8d92-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8d92-111">PARAMETERS</span></span>

### <span data-ttu-id="e8d92-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8d92-112">-AsJob</span></span>
<span data-ttu-id="e8d92-113">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="e8d92-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e8d92-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="e8d92-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="e8d92-115">Nazwa używana do tworzenia klastra</span><span class="sxs-lookup"><span data-stu-id="e8d92-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="e8d92-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="e8d92-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="e8d92-117">Nazwa używana przez klaster operacyjny</span><span class="sxs-lookup"><span data-stu-id="e8d92-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="e8d92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d92-118">-DefaultProfile</span></span>
<span data-ttu-id="e8d92-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8d92-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8d92-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="e8d92-120">-DomainFqdn</span></span>
<span data-ttu-id="e8d92-121">W pełni kwalifikowana nazwa domeny</span><span class="sxs-lookup"><span data-stu-id="e8d92-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="e8d92-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="e8d92-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="e8d92-123">Opcjonalna ścieżka monitora</span><span class="sxs-lookup"><span data-stu-id="e8d92-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="e8d92-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e8d92-124">-Location</span></span>
<span data-ttu-id="e8d92-125">Lokalizacja grupy maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="e8d92-125">SQL virtual machine group location.</span></span>

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

### <span data-ttu-id="e8d92-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8d92-126">-Name</span></span>
<span data-ttu-id="e8d92-127">Nazwa grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="e8d92-127">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="e8d92-128">-Offer</span><span class="sxs-lookup"><span data-stu-id="e8d92-128">-Offer</span></span>
<span data-ttu-id="e8d92-129">Oferta grupy maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="e8d92-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="e8d92-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="e8d92-130">-OuPath</span></span>
<span data-ttu-id="e8d92-131">Ścieżka jednostki organizacyjnej, w której znajdują się węzły i klaster</span><span class="sxs-lookup"><span data-stu-id="e8d92-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="e8d92-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8d92-132">-ResourceGroupName</span></span>
<span data-ttu-id="e8d92-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8d92-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="e8d92-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="e8d92-134">-Sku</span></span>
<span data-ttu-id="e8d92-135">Typ wydania Grupa maszyn wirtualnych SQL.</span><span class="sxs-lookup"><span data-stu-id="e8d92-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="e8d92-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="e8d92-136">-SqlServiceAccount</span></span>
<span data-ttu-id="e8d92-137">Nazwa, pod którą usługa SQL będzie uruchamiana na wszystkich uczestniczących maszynach wirtualnych SQL w klastrze</span><span class="sxs-lookup"><span data-stu-id="e8d92-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="e8d92-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e8d92-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="e8d92-139">Klucz podstawowy konta magazynu monitora</span><span class="sxs-lookup"><span data-stu-id="e8d92-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="e8d92-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="e8d92-140">-StorageAccountUrl</span></span>
<span data-ttu-id="e8d92-141">Klucz podstawowy konta magazynu monitora</span><span class="sxs-lookup"><span data-stu-id="e8d92-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="e8d92-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8d92-142">-Tag</span></span>
<span data-ttu-id="e8d92-143">Tagi, które mają zostać skojarzone z grupą maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="e8d92-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="e8d92-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8d92-144">-Confirm</span></span>
<span data-ttu-id="e8d92-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8d92-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8d92-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8d92-146">-WhatIf</span></span>
<span data-ttu-id="e8d92-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8d92-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8d92-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8d92-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8d92-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d92-149">CommonParameters</span></span>
<span data-ttu-id="e8d92-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8d92-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d92-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8d92-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d92-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8d92-152">INPUTS</span></span>

### <span data-ttu-id="e8d92-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e8d92-153">System.String</span></span>

## <span data-ttu-id="e8d92-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8d92-154">OUTPUTS</span></span>

### <span data-ttu-id="e8d92-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="e8d92-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="e8d92-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8d92-156">NOTES</span></span>

## <span data-ttu-id="e8d92-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8d92-157">RELATED LINKS</span></span>
