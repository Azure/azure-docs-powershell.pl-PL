---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504098"
---
# <span data-ttu-id="849b6-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="849b6-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="849b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="849b6-102">SYNOPSIS</span></span>
<span data-ttu-id="849b6-103">Pobiera właściwości maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="849b6-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="849b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="849b6-104">SYNTAX</span></span>

### <span data-ttu-id="849b6-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="849b6-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="849b6-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="849b6-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="849b6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="849b6-107">DESCRIPTION</span></span>
<span data-ttu-id="849b6-108">Polecenie cmdlet **Get-AzVmssVM** pobiera widok modelu i widok wystąpienia maszyny wirtualnej zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="849b6-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="849b6-109">Widok modelu to określone przez użytkownika właściwości maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="849b6-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="849b6-110">Widok wystąpienia jest stanem poziomu wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="849b6-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="849b6-111">Określ parametr *status* , aby uzyskać dostęp tylko do widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="849b6-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="849b6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="849b6-112">EXAMPLES</span></span>

### <span data-ttu-id="849b6-113">Przykład 1: uzyskiwanie właściwości maszyny wirtualnej VMSS</span><span class="sxs-lookup"><span data-stu-id="849b6-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="849b6-114">To polecenie pobiera właściwości maszyny wirtualnej VMSS o nazwie VMSS001 należącej do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="849b6-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="849b6-115">Ponieważ polecenie nie określa parametru przełącznika *InstanceView* , funkcja cmdlet pobiera widok modelu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="849b6-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="849b6-116">Przykład 2: uzyskiwanie właściwości widoku modelu maszyny wirtualnej VMSS</span><span class="sxs-lookup"><span data-stu-id="849b6-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="849b6-117">To polecenie pobiera właściwości maszyny wirtualnej VMSS o nazwie VMSS004 należącej do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="849b6-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="849b6-118">Polecenie pobiera identyfikator wystąpienia zapisanego w zmiennej $ID, dla którego ma zostać wyświetlony widok model.</span><span class="sxs-lookup"><span data-stu-id="849b6-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="849b6-119">Przykład 3: uzyskiwanie właściwości widoku wystąpienia maszyny wirtualnej VMSS</span><span class="sxs-lookup"><span data-stu-id="849b6-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="849b6-120">To polecenie pobiera właściwości maszyny wirtualnej VMSS o nazwie VMSS004 należącej do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="849b6-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="849b6-121">Ponieważ polecenie określa parametr Switch *InstanceView* , polecenie cmdlet umożliwia wyświetlenie widoku wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="849b6-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="849b6-122">Polecenie pobiera identyfikator wystąpienia zapisanego w zmiennej $ID, dla którego ma zostać wyświetlony widok wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="849b6-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="849b6-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="849b6-123">PARAMETERS</span></span>

### <span data-ttu-id="849b6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849b6-124">-DefaultProfile</span></span>
<span data-ttu-id="849b6-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="849b6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="849b6-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="849b6-126">-InstanceId</span></span>
<span data-ttu-id="849b6-127">Określa identyfikator wystąpienia, dla którego ma zostać wyświetlony widok model.</span><span class="sxs-lookup"><span data-stu-id="849b6-127">Specifies the instance ID for which to get the model view.</span></span>

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

### <span data-ttu-id="849b6-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="849b6-128">-InstanceView</span></span>
<span data-ttu-id="849b6-129">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="849b6-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="849b6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="849b6-130">-ResourceGroupName</span></span>
<span data-ttu-id="849b6-131">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="849b6-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="849b6-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="849b6-132">-VMScaleSetName</span></span>
<span data-ttu-id="849b6-133">Gatunek nazwy VMSS.</span><span class="sxs-lookup"><span data-stu-id="849b6-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="849b6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849b6-134">CommonParameters</span></span>
<span data-ttu-id="849b6-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="849b6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849b6-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="849b6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849b6-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="849b6-137">INPUTS</span></span>

### <span data-ttu-id="849b6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="849b6-138">System.String</span></span>

## <span data-ttu-id="849b6-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="849b6-139">OUTPUTS</span></span>

### <span data-ttu-id="849b6-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="849b6-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="849b6-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="849b6-141">NOTES</span></span>

## <span data-ttu-id="849b6-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="849b6-142">RELATED LINKS</span></span>

[<span data-ttu-id="849b6-143">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="849b6-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="849b6-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="849b6-144">Get-AzVmss</span></span>](./Get-AzVmss.md)


