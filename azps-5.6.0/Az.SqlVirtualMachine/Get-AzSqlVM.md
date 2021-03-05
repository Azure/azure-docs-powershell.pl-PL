---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b3678b52f55e09fdcad8c1d116cd349b2cc5ab45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992223"
---
# <span data-ttu-id="44299-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="44299-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="44299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44299-102">SYNOPSIS</span></span>
<span data-ttu-id="44299-103">Pobiera co najmniej jedną maszynę wirtualną sql.</span><span class="sxs-lookup"><span data-stu-id="44299-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="44299-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="44299-104">SYNTAX</span></span>

### <span data-ttu-id="44299-105">ResourceGroupOnly (Default)</span><span class="sxs-lookup"><span data-stu-id="44299-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44299-106">Nazwa</span><span class="sxs-lookup"><span data-stu-id="44299-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44299-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="44299-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44299-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="44299-108">DESCRIPTION</span></span>
<span data-ttu-id="44299-109">Polecenie Get-AzSqlVM cmdlet pobiera jedną lub więcej maszyn wirtualnych sql.</span><span class="sxs-lookup"><span data-stu-id="44299-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="44299-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="44299-110">EXAMPLES</span></span>

### <span data-ttu-id="44299-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="44299-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="44299-112">To polecenie pobiera informacje o wszystkich komputerach wirtualnych języka Azure SQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="44299-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="44299-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="44299-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="44299-114">To polecenie pobiera informacje na temat wszystkich maszyn wirtualnych języka Azure SQL w bieżącej subskrypcji przypisanej do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="44299-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="44299-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="44299-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="44299-116">To polecenie pobiera informacje o maszynce wirtualnej SQL "maszyny wirtualnej" przypisanej do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="44299-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="44299-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44299-117">PARAMETERS</span></span>

### <span data-ttu-id="44299-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44299-118">-DefaultProfile</span></span>
<span data-ttu-id="44299-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="44299-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44299-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="44299-120">-Name</span></span>
<span data-ttu-id="44299-121">Nazwa maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="44299-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="44299-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44299-122">-ResourceGroupName</span></span>
<span data-ttu-id="44299-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="44299-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="44299-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44299-124">-ResourceId</span></span>
<span data-ttu-id="44299-125">Identyfikator zasobu maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="44299-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="44299-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44299-126">CommonParameters</span></span>
<span data-ttu-id="44299-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44299-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44299-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44299-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44299-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44299-129">INPUTS</span></span>

### <span data-ttu-id="44299-130">Brak</span><span class="sxs-lookup"><span data-stu-id="44299-130">None</span></span>

## <span data-ttu-id="44299-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44299-131">OUTPUTS</span></span>

### <span data-ttu-id="44299-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="44299-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="44299-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="44299-133">NOTES</span></span>

## <span data-ttu-id="44299-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44299-134">RELATED LINKS</span></span>
