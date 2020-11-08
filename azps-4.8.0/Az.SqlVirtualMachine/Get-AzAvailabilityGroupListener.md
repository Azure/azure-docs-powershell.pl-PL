---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222187"
---
# <span data-ttu-id="d40a9-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="d40a9-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="d40a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d40a9-102">SYNOPSIS</span></span>
<span data-ttu-id="d40a9-103">Uzyskaj jeden lub więcej detektorów grup dostępności w grupie maszyna wirtualna SQL.</span><span class="sxs-lookup"><span data-stu-id="d40a9-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="d40a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d40a9-104">SYNTAX</span></span>

### <span data-ttu-id="d40a9-105">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d40a9-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d40a9-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="d40a9-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d40a9-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="d40a9-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d40a9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d40a9-108">DESCRIPTION</span></span>
<span data-ttu-id="d40a9-109">Get-AzAvailabilityGroupListener pobiera jeden lub więcej detektorów grup dostępności z grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="d40a9-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="d40a9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d40a9-110">EXAMPLES</span></span>

### <span data-ttu-id="d40a9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d40a9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="d40a9-112">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="d40a9-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="d40a9-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="d40a9-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="d40a9-114">To polecenie pobiera informacje o AgListener01 odbiornika grup dostępności w grupie SqlVmGroup01 i grupie zasobów maszyny wirtualnej SQL ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d40a9-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="d40a9-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d40a9-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="d40a9-116">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="d40a9-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="d40a9-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="d40a9-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="d40a9-118">To polecenie pobiera informacje o wszystkich detektorach grup dostępności w grupie SqlVmGroup01 i grupie zasobów maszyny wirtualnej SQL ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d40a9-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="d40a9-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d40a9-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="d40a9-120">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="d40a9-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="d40a9-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="d40a9-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="d40a9-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d40a9-122">PARAMETERS</span></span>

### <span data-ttu-id="d40a9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d40a9-123">-DefaultProfile</span></span>
<span data-ttu-id="d40a9-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d40a9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d40a9-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d40a9-125">-Name</span></span>
<span data-ttu-id="d40a9-126">Nazwa odbiornika grupy dostępności.</span><span class="sxs-lookup"><span data-stu-id="d40a9-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="d40a9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d40a9-127">-ResourceGroupName</span></span>
<span data-ttu-id="d40a9-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d40a9-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="d40a9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d40a9-129">-ResourceId</span></span>
<span data-ttu-id="d40a9-130">Identyfikator zasobu odbiornika grupy dostępności</span><span class="sxs-lookup"><span data-stu-id="d40a9-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="d40a9-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="d40a9-131">-SqlVMGroupName</span></span>
<span data-ttu-id="d40a9-132">Nazwa grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="d40a9-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="d40a9-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="d40a9-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="d40a9-134">Obiekt grupy maszyny wirtualnej SQL.</span><span class="sxs-lookup"><span data-stu-id="d40a9-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="d40a9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d40a9-135">CommonParameters</span></span>
<span data-ttu-id="d40a9-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d40a9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d40a9-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d40a9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d40a9-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d40a9-138">INPUTS</span></span>

### <span data-ttu-id="d40a9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d40a9-139">System.String</span></span>

### <span data-ttu-id="d40a9-140">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="d40a9-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="d40a9-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d40a9-141">OUTPUTS</span></span>

### <span data-ttu-id="d40a9-142">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="d40a9-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="d40a9-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d40a9-143">NOTES</span></span>

## <span data-ttu-id="d40a9-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d40a9-144">RELATED LINKS</span></span>
