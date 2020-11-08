---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220251"
---
# <span data-ttu-id="4a931-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="4a931-101">New-AzSqlVM</span></span>

## <span data-ttu-id="4a931-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a931-102">SYNOPSIS</span></span>
<span data-ttu-id="4a931-103">Tworzy nową maszynę wirtualną SQL.</span><span class="sxs-lookup"><span data-stu-id="4a931-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="4a931-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a931-104">SYNTAX</span></span>

### <span data-ttu-id="4a931-105">NameParamaterList (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4a931-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a931-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="4a931-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a931-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4a931-107">DESCRIPTION</span></span>
<span data-ttu-id="4a931-108">Polecenie cmdlet New-AzSqlVM Tworzenie maszyny wirtualnej Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4a931-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="4a931-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a931-109">EXAMPLES</span></span>

### <span data-ttu-id="4a931-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a931-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="4a931-111">Tworzy nową maszynę wirtualną SQL Azure o nazwie VM w grupie zasobów ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="4a931-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="4a931-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a931-112">PARAMETERS</span></span>

### <span data-ttu-id="4a931-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a931-113">-AsJob</span></span>
<span data-ttu-id="4a931-114">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="4a931-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="4a931-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a931-115">-DefaultProfile</span></span>
<span data-ttu-id="4a931-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a931-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a931-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4a931-117">-LicenseType</span></span>
<span data-ttu-id="4a931-118">Typ licencji maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="4a931-118">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="4a931-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4a931-119">-Location</span></span>
<span data-ttu-id="4a931-120">Lokalizacja maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="4a931-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="4a931-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4a931-121">-Name</span></span>
<span data-ttu-id="4a931-122">Nazwa maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="4a931-122">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="4a931-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="4a931-123">-Offer</span></span>
<span data-ttu-id="4a931-124">Oferta maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="4a931-124">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="4a931-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a931-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a931-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4a931-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a931-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="4a931-127">-Sku</span></span>
<span data-ttu-id="4a931-128">Typ wydania maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="4a931-128">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="4a931-129">-Sqlmanagementtype</span><span class="sxs-lookup"><span data-stu-id="4a931-129">-SqlManagementType</span></span>
<span data-ttu-id="4a931-130">Typ zarządzania maszyną wirtualną SQL.</span><span class="sxs-lookup"><span data-stu-id="4a931-130">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="4a931-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="4a931-131">-SqlVM</span></span>
<span data-ttu-id="4a931-132">Obiekt maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="4a931-132">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="4a931-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a931-133">-Tag</span></span>
<span data-ttu-id="4a931-134">Tagi, które mają zostać skojarzone z maszyną wirtualną SQL</span><span class="sxs-lookup"><span data-stu-id="4a931-134">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="4a931-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a931-135">-Confirm</span></span>
<span data-ttu-id="4a931-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a931-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a931-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a931-137">-WhatIf</span></span>
<span data-ttu-id="4a931-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a931-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a931-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4a931-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a931-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a931-140">CommonParameters</span></span>
<span data-ttu-id="4a931-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a931-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a931-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a931-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a931-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a931-143">INPUTS</span></span>

### <span data-ttu-id="4a931-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="4a931-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="4a931-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a931-145">OUTPUTS</span></span>

### <span data-ttu-id="4a931-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="4a931-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="4a931-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a931-147">NOTES</span></span>

## <span data-ttu-id="4a931-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a931-148">RELATED LINKS</span></span>
