---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183251"
---
# <span data-ttu-id="23ae3-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="23ae3-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="23ae3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="23ae3-103">Pobiera jedną lub więcej grup maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="23ae3-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="23ae3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="23ae3-104">SYNTAX</span></span>

### <span data-ttu-id="23ae3-105">ResourceGroupOnly (Default)</span><span class="sxs-lookup"><span data-stu-id="23ae3-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23ae3-106">Nazwa</span><span class="sxs-lookup"><span data-stu-id="23ae3-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23ae3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="23ae3-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23ae3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="23ae3-108">DESCRIPTION</span></span>
<span data-ttu-id="23ae3-109">Polecenie Get-AzSqlVMGroup cmdlet pobiera jedną lub więcej grup maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="23ae3-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="23ae3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="23ae3-110">EXAMPLES</span></span>

### <span data-ttu-id="23ae3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23ae3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="23ae3-112">To polecenie pobiera informacje o wszystkich grupach maszyn wirtualnych języka Azure SQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="23ae3-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="23ae3-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="23ae3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="23ae3-114">To polecenie pobiera informacje o wszystkich grupach maszyn wirtualnych języka Azure SQL w bieżącej subskrypcji przypisanej do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="23ae3-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="23ae3-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="23ae3-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="23ae3-116">To polecenie pobiera informacje o grupie maszyn wirtualnych JĘZYKA SQL "test-grupa" przypisanej do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="23ae3-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="23ae3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23ae3-117">PARAMETERS</span></span>

### <span data-ttu-id="23ae3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ae3-118">-DefaultProfile</span></span>
<span data-ttu-id="23ae3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="23ae3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23ae3-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="23ae3-120">-Name</span></span>
<span data-ttu-id="23ae3-121">Nazwa grupy maszyn wirtualnych JĘZYKA SQL.</span><span class="sxs-lookup"><span data-stu-id="23ae3-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="23ae3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23ae3-122">-ResourceGroupName</span></span>
<span data-ttu-id="23ae3-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23ae3-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="23ae3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23ae3-124">-ResourceId</span></span>
<span data-ttu-id="23ae3-125">Identyfikator zasobu grupy maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="23ae3-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="23ae3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ae3-126">CommonParameters</span></span>
<span data-ttu-id="23ae3-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23ae3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ae3-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23ae3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ae3-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23ae3-129">INPUTS</span></span>

### <span data-ttu-id="23ae3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="23ae3-130">System.String</span></span>

## <span data-ttu-id="23ae3-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23ae3-131">OUTPUTS</span></span>

### <span data-ttu-id="23ae3-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="23ae3-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="23ae3-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="23ae3-133">NOTES</span></span>

## <span data-ttu-id="23ae3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23ae3-134">RELATED LINKS</span></span>
