---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: ca9693f715d72366a6cc78030d0a8328bf0abc50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238870"
---
# <span data-ttu-id="8a3f1-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="8a3f1-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="8a3f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="8a3f1-103">Pobiera właściwości rozszerzeń maszyn wirtualnych zainstalowanych na maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="8a3f1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8a3f1-104">SYNTAX</span></span>

### <span data-ttu-id="8a3f1-105">GetExtensionParameterSet (ustawienie domyślne)</span><span class="sxs-lookup"><span data-stu-id="8a3f1-105">GetExtensionParameterSet (Default)</span></span>
```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a3f1-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a3f1-106">VMParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-VMObject <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a3f1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a3f1-107">ResourceIdParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-ResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a3f1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8a3f1-108">DESCRIPTION</span></span>
<span data-ttu-id="8a3f1-109">Polecenie **cmdlet Get-AzVMExtension** pobiera właściwości rozszerzeń maszyn wirtualnych zainstalowanych na maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-109">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="8a3f1-110">Określ nazwę rozszerzenia, dla którego mają być właściwości.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-110">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="8a3f1-111">Aby uzyskać tylko widok wystąpienia rozszerzenia, określ parametr Status.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-111">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="8a3f1-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8a3f1-112">EXAMPLES</span></span>

### <span data-ttu-id="8a3f1-113">Przykład 1. Uzyskiwanie właściwości rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="8a3f1-113">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="8a3f1-114">To polecenie pobiera właściwości rozszerzenia o nazwie CustomScriptExtension na komputerze wirtualnym o nazwie VirtualMachine22 w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-114">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="8a3f1-115">Przykład 2. Wyświetlanie widoku wystąpienia rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="8a3f1-115">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                : {Microsoft.Azure.Management.Compute.Models.InstanceViewStatus}
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="8a3f1-116">To polecenie pobiera widok wystąpienia dla rozszerzenia o nazwie CustomScriptExtension na komputerze wirtualnym o nazwie VirtualMachine22 w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-116">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="8a3f1-117">Przykład 3. Uzyskiwanie wszystkich rozszerzeń zainstalowanych na maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8a3f1-117">Example 3: Get all extensions installed on a VM</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

### <span data-ttu-id="8a3f1-118">Przykład 4. Uzyskiwanie właściwości rozszerzenia przy użyciu parametru MASZYNY WIRTUALNEj</span><span class="sxs-lookup"><span data-stu-id="8a3f1-118">Example 4: Get properties of an extension using the VM parameter</span></span>
```
PS C:\> $vm = Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine22"
PS C:\> Get-AzVMExtension -VM $vm

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="8a3f1-119">To polecenie pobiera listę rozszerzeń zainstalowanych na maszyny wirtualnej o nazwie VirtualMachine22 w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-119">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="8a3f1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a3f1-120">PARAMETERS</span></span>

### <span data-ttu-id="8a3f1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a3f1-121">-DefaultProfile</span></span>
<span data-ttu-id="8a3f1-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a3f1-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8a3f1-123">-Name</span></span>
<span data-ttu-id="8a3f1-124">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-124">Specifies the name of an extension.</span></span>
<span data-ttu-id="8a3f1-125">To polecenie cmdlet pobiera właściwości dla rozszerzenia, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-125">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a3f1-126">-ResourceGroupName</span></span>
<span data-ttu-id="8a3f1-127">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a3f1-128">-ResourceId</span></span>
<span data-ttu-id="8a3f1-129">Identyfikator zasobu określający obiekt maszyny wirtualnej, dla których ma być rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-129">Resource Id specifying the virtual machine object the extension is on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f1-130">— Status</span><span class="sxs-lookup"><span data-stu-id="8a3f1-130">-Status</span></span>
<span data-ttu-id="8a3f1-131">Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-131">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f1-132">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="8a3f1-132">-VMName</span></span>
<span data-ttu-id="8a3f1-133">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="8a3f1-134">To polecenie cmdlet pobiera właściwości rozszerzenia z maszyny wirtualnej, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-134">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f1-135">-VMObject</span><span class="sxs-lookup"><span data-stu-id="8a3f1-135">-VMObject</span></span>
<span data-ttu-id="8a3f1-136">Określa obiekt maszyny wirtualnej, dla których rozszerzenie jest wł.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-136">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a3f1-137">CommonParameters</span></span>
<span data-ttu-id="8a3f1-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a3f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a3f1-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a3f1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a3f1-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a3f1-140">INPUTS</span></span>

### <span data-ttu-id="8a3f1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8a3f1-141">System.String</span></span>

### <span data-ttu-id="8a3f1-142">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="8a3f1-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8a3f1-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a3f1-143">OUTPUTS</span></span>

### <span data-ttu-id="8a3f1-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="8a3f1-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="8a3f1-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8a3f1-145">NOTES</span></span>

## <span data-ttu-id="8a3f1-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a3f1-146">RELATED LINKS</span></span>

[<span data-ttu-id="8a3f1-147">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="8a3f1-147">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="8a3f1-148">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="8a3f1-148">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


