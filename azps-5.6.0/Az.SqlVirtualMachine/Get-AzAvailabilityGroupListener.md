---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: be20b280dccccae6f6afcc1a18514ad3dfb89ba2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008337"
---
# <span data-ttu-id="38d86-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="38d86-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="38d86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38d86-102">SYNOPSIS</span></span>
<span data-ttu-id="38d86-103">Pobierz co najmniej jednego słuchacza grupy dostępności w grupie maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="38d86-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="38d86-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="38d86-104">SYNTAX</span></span>

### <span data-ttu-id="38d86-105">Nazwa (domyślna)</span><span class="sxs-lookup"><span data-stu-id="38d86-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38d86-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="38d86-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38d86-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38d86-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38d86-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="38d86-108">DESCRIPTION</span></span>
<span data-ttu-id="38d86-109">Grupa Get-AzAvailabilityGroupListener pobiera co najmniej jednego słuchacza grupy dostępności z grupy maszyn wirtualnych języka SQL.</span><span class="sxs-lookup"><span data-stu-id="38d86-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="38d86-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="38d86-110">EXAMPLES</span></span>

### <span data-ttu-id="38d86-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="38d86-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="38d86-112">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="38d86-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="38d86-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="38d86-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="38d86-114">To polecenie pobiera informacje o słuchaczu grupy dostępności AgListener01 w grupie maszyn wirtualnych SQL SQLVmGroup01 i Resource Group ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="38d86-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="38d86-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="38d86-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="38d86-116">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="38d86-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="38d86-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="38d86-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="38d86-118">To polecenie pobiera informacje o wszystkich słuchaczach grupy dostępności w grupie sql virtual machine, SqlVmGroup01 i Resource Group ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="38d86-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="38d86-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="38d86-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="38d86-120">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="38d86-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="38d86-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="38d86-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="38d86-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38d86-122">PARAMETERS</span></span>

### <span data-ttu-id="38d86-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d86-123">-DefaultProfile</span></span>
<span data-ttu-id="38d86-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="38d86-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38d86-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="38d86-125">-Name</span></span>
<span data-ttu-id="38d86-126">Nazwa słuchacza grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="38d86-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d86-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d86-127">-ResourceGroupName</span></span>
<span data-ttu-id="38d86-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="38d86-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="38d86-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38d86-129">-ResourceId</span></span>
<span data-ttu-id="38d86-130">Identyfikator zasobu słuchacza grupy dostępności</span><span class="sxs-lookup"><span data-stu-id="38d86-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d86-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="38d86-131">-SqlVMGroupName</span></span>
<span data-ttu-id="38d86-132">Nazwa grupy maszyn wirtualnych JĘZYKA SQL.</span><span class="sxs-lookup"><span data-stu-id="38d86-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d86-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="38d86-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="38d86-134">Obiekt sql virtual machine Group.</span><span class="sxs-lookup"><span data-stu-id="38d86-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38d86-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d86-135">CommonParameters</span></span>
<span data-ttu-id="38d86-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d86-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d86-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38d86-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d86-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38d86-138">INPUTS</span></span>

### <span data-ttu-id="38d86-139">System.String</span><span class="sxs-lookup"><span data-stu-id="38d86-139">System.String</span></span>

### <span data-ttu-id="38d86-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="38d86-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="38d86-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38d86-141">OUTPUTS</span></span>

### <span data-ttu-id="38d86-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="38d86-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="38d86-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="38d86-143">NOTES</span></span>

## <span data-ttu-id="38d86-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38d86-144">RELATED LINKS</span></span>
