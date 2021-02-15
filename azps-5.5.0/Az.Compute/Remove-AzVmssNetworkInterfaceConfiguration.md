---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 1b8f9b7843cccf2475e17e1c5d8866972b5b9ee4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177491"
---
# <span data-ttu-id="17031-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="17031-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="17031-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17031-102">SYNOPSIS</span></span>
<span data-ttu-id="17031-103">Usuwa konfigurację interfejsu sieciowego z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17031-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="17031-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17031-104">SYNTAX</span></span>

### <span data-ttu-id="17031-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="17031-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17031-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17031-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17031-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="17031-107">DESCRIPTION</span></span>
<span data-ttu-id="17031-108">Polecenie **cmdlet Remove-AzVmssNetworkInterfaceConfiguration** usuwa konfigurację interfejsu sieciowego z zestawu skal maszyn wirtualnych (VIRTUAL Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="17031-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="17031-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17031-109">EXAMPLES</span></span>

### <span data-ttu-id="17031-110">Przykład 1. Usuwanie konfiguracji interfejsu</span><span class="sxs-lookup"><span data-stu-id="17031-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="17031-111">Pierwsze polecenie pobiera usługę VMSS przy użyciu Get-AzVmss cmdlet, a następnie zapisuje je w $VMSS zmienną.</span><span class="sxs-lookup"><span data-stu-id="17031-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="17031-112">Drugie polecenie usuwa konfigurację interfejsu sieciowego o nazwie ContosoVmssInterface02 z zestawu w programie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="17031-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="17031-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17031-113">PARAMETERS</span></span>

### <span data-ttu-id="17031-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17031-114">-DefaultProfile</span></span>
<span data-ttu-id="17031-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="17031-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17031-116">— Id</span><span class="sxs-lookup"><span data-stu-id="17031-116">-Id</span></span>
<span data-ttu-id="17031-117">Określa identyfikator konfiguracji interfejsu sieciowego, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17031-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17031-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="17031-118">-Name</span></span>
<span data-ttu-id="17031-119">Określa nazwę konfiguracji interfejsu sieciowego, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17031-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17031-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17031-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="17031-121">Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="17031-121">Specifies the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17031-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="17031-122">-Confirm</span></span>
<span data-ttu-id="17031-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="17031-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17031-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17031-124">-WhatIf</span></span>
<span data-ttu-id="17031-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17031-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17031-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="17031-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17031-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17031-127">CommonParameters</span></span>
<span data-ttu-id="17031-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17031-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17031-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17031-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17031-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17031-130">INPUTS</span></span>

### <span data-ttu-id="17031-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17031-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="17031-132">System.String</span><span class="sxs-lookup"><span data-stu-id="17031-132">System.String</span></span>

## <span data-ttu-id="17031-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17031-133">OUTPUTS</span></span>

### <span data-ttu-id="17031-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17031-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="17031-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17031-135">NOTES</span></span>

## <span data-ttu-id="17031-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17031-136">RELATED LINKS</span></span>

[<span data-ttu-id="17031-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="17031-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="17031-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="17031-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


