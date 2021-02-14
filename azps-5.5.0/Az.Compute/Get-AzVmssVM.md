---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244139"
---
# <span data-ttu-id="264aa-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="264aa-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="264aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="264aa-102">SYNOPSIS</span></span>
<span data-ttu-id="264aa-103">Pobiera właściwości maszyny wirtualnej MASZYNY WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="264aa-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="264aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="264aa-104">SYNTAX</span></span>

### <span data-ttu-id="264aa-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="264aa-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="264aa-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="264aa-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="264aa-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="264aa-107">DESCRIPTION</span></span>
<span data-ttu-id="264aa-108">Polecenie **cmdlet Get-AzVmssVM** pobiera widok modelu i widok wystąpienia maszyny wirtualnej ( VIRTUAL Machine Scale Set) maszyny wirtualnej .</span><span class="sxs-lookup"><span data-stu-id="264aa-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="264aa-109">Widok modelu to właściwości maszyny wirtualnej określone przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="264aa-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="264aa-110">Widok wystąpienia jest stanem poziomu wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="264aa-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="264aa-111">Określ parametr *Status,* aby uzyskać tylko widok wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="264aa-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="264aa-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="264aa-112">EXAMPLES</span></span>

### <span data-ttu-id="264aa-113">Przykład 1. Uzyskiwanie właściwości maszyny wirtualnej MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="264aa-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="264aa-114">To polecenie pobiera właściwości maszyny wirtualnej MASZYNY WIRTUALNEJ o nazwie VIRTUALSS001, która należy do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="264aa-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="264aa-115">Ponieważ to polecenie nie określa *parametru przełącznika InstanceView,* polecenie cmdlet pobiera widok modelu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="264aa-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="264aa-116">Przykład 2. Uzyskiwanie właściwości widoku modelu maszyny wirtualnej MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="264aa-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="264aa-117">To polecenie pobiera właściwości maszyny wirtualnej MASZYNY WIRTUALNEJ o nazwie VIRTUALSS04, która należy do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="264aa-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="264aa-118">To polecenie pobiera identyfikator wystąpienia przechowywany w zmiennej $ID, dla której można uzyskać widok modelu.</span><span class="sxs-lookup"><span data-stu-id="264aa-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="264aa-119">Przykład 3. Uzyskiwanie właściwości widoku wystąpienia maszyny wirtualnej MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="264aa-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="264aa-120">To polecenie pobiera właściwości maszyny wirtualnej MASZYNY WIRTUALNEJ o nazwie VIRTUALSS04, która należy do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="264aa-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="264aa-121">Ponieważ to polecenie określa parametr *przełącznika InstanceView,* polecenie cmdlet pobiera widok wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="264aa-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="264aa-122">Polecenie pobiera identyfikator wystąpienia przechowywany w zmiennej $ID, dla której można uzyskać widok wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="264aa-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="264aa-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="264aa-123">PARAMETERS</span></span>

### <span data-ttu-id="264aa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="264aa-124">-DefaultProfile</span></span>
<span data-ttu-id="264aa-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="264aa-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="264aa-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="264aa-126">-InstanceId</span></span>
<span data-ttu-id="264aa-127">Określa identyfikator wystąpienia, dla którego ma być pobrać widok modelu.</span><span class="sxs-lookup"><span data-stu-id="264aa-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="264aa-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="264aa-128">-InstanceView</span></span>
<span data-ttu-id="264aa-129">Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="264aa-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264aa-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="264aa-130">-ResourceGroupName</span></span>
<span data-ttu-id="264aa-131">Określa nazwę grupy zasobów maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="264aa-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="264aa-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="264aa-132">-VMScaleSetName</span></span>
<span data-ttu-id="264aa-133">Nazwa maszyny wirtualnej to "gatunek".</span><span class="sxs-lookup"><span data-stu-id="264aa-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="264aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="264aa-134">CommonParameters</span></span>
<span data-ttu-id="264aa-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="264aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="264aa-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="264aa-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="264aa-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="264aa-137">INPUTS</span></span>

### <span data-ttu-id="264aa-138">System.String</span><span class="sxs-lookup"><span data-stu-id="264aa-138">System.String</span></span>

## <span data-ttu-id="264aa-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="264aa-139">OUTPUTS</span></span>

### <span data-ttu-id="264aa-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="264aa-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="264aa-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="264aa-141">NOTES</span></span>

## <span data-ttu-id="264aa-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="264aa-142">RELATED LINKS</span></span>

[<span data-ttu-id="264aa-143">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="264aa-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="264aa-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="264aa-144">Get-AzVmss</span></span>](./Get-AzVmss.md)


