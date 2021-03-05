---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: a7ff8df963f7d1d58256ab40cf5788e81b49a23c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992195"
---
# <span data-ttu-id="21163-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="21163-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="21163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21163-102">SYNOPSIS</span></span>
<span data-ttu-id="21163-103">Pobiera jedną lub więcej grup maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="21163-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="21163-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="21163-104">SYNTAX</span></span>

### <span data-ttu-id="21163-105">ResourceGroupOnly (Default)</span><span class="sxs-lookup"><span data-stu-id="21163-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21163-106">Nazwa</span><span class="sxs-lookup"><span data-stu-id="21163-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21163-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="21163-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21163-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="21163-108">DESCRIPTION</span></span>
<span data-ttu-id="21163-109">Polecenie Get-AzSqlVMGroup cmdlet pobiera jedną lub więcej grup maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="21163-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="21163-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="21163-110">EXAMPLES</span></span>

### <span data-ttu-id="21163-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21163-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="21163-112">To polecenie pobiera informacje o wszystkich grupach maszyn wirtualnych języka Azure SQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="21163-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="21163-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="21163-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="21163-114">To polecenie pobiera informacje o wszystkich grupach maszyn wirtualnych języka Azure SQL w bieżącej subskrypcji przypisanej do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="21163-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="21163-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="21163-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="21163-116">To polecenie pobiera informacje o grupie maszyn wirtualnych JĘZYKA SQL "grupa testowa" przypisanej do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="21163-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="21163-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21163-117">PARAMETERS</span></span>

### <span data-ttu-id="21163-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21163-118">-DefaultProfile</span></span>
<span data-ttu-id="21163-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="21163-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21163-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="21163-120">-Name</span></span>
<span data-ttu-id="21163-121">Nazwa grupy maszyn wirtualnych JĘZYKA SQL.</span><span class="sxs-lookup"><span data-stu-id="21163-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="21163-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21163-122">-ResourceGroupName</span></span>
<span data-ttu-id="21163-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21163-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="21163-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21163-124">-ResourceId</span></span>
<span data-ttu-id="21163-125">Identyfikator zasobu grupy maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="21163-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="21163-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21163-126">CommonParameters</span></span>
<span data-ttu-id="21163-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21163-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21163-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21163-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21163-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21163-129">INPUTS</span></span>

### <span data-ttu-id="21163-130">System.String</span><span class="sxs-lookup"><span data-stu-id="21163-130">System.String</span></span>

## <span data-ttu-id="21163-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21163-131">OUTPUTS</span></span>

### <span data-ttu-id="21163-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="21163-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="21163-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="21163-133">NOTES</span></span>

## <span data-ttu-id="21163-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21163-134">RELATED LINKS</span></span>
