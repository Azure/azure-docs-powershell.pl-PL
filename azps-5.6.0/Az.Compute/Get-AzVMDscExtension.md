---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: 307dccf0d5bb137ba83a6acf3a9b5db0b4606f7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013850"
---
# <span data-ttu-id="852d7-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="852d7-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="852d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="852d7-102">SYNOPSIS</span></span>
<span data-ttu-id="852d7-103">Pobiera ustawienia rozszerzenia DSC na określonej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="852d7-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="852d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="852d7-104">SYNTAX</span></span>

### <span data-ttu-id="852d7-105">GetDscExtension (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="852d7-105">GetDscExtension (Default)</span></span>
```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="852d7-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="852d7-106">VMParameterSet</span></span>
```
Get-AzVMDscExtension [-Status] [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="852d7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="852d7-107">DESCRIPTION</span></span>
<span data-ttu-id="852d7-108">Polecenie **cmdlet Get-AzVMDscExtension** pobiera ustawienia rozszerzenia Desired State Configuration (DSC) na określonej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="852d7-108">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="852d7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="852d7-109">EXAMPLES</span></span>

### <span data-ttu-id="852d7-110">Przykład 1. Uzyskiwanie ustawień rozszerzenia DSC</span><span class="sxs-lookup"><span data-stu-id="852d7-110">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="852d7-111">To polecenie pobiera ustawienia rozszerzenia o nazwie DSC na maszyny wirtualnej o nazwie MASZYNY WIRTUALNEJ07.</span><span class="sxs-lookup"><span data-stu-id="852d7-111">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="852d7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="852d7-112">PARAMETERS</span></span>

### <span data-ttu-id="852d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="852d7-113">-DefaultProfile</span></span>
<span data-ttu-id="852d7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="852d7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="852d7-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="852d7-115">-Name</span></span>
<span data-ttu-id="852d7-116">Określa nazwę zasobu usługi Azure Resource Manager reprezentującą to rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="852d7-116">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="852d7-117">Polecenie Set-AzVMDscExtension ustawia tę nazwę na Microsoft.Powershell.DSC, która jest tą samą wartością używaną przez polecenie **Get-AzVMDscExtension.**</span><span class="sxs-lookup"><span data-stu-id="852d7-117">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="852d7-118">Określ ten parametr tylko w przypadku zmiany domyślnej nazwy w cmdlet **Set-AzVMDscExtension** lub użycia innej nazwy zasobu w szablonie Menedżer zasobów.</span><span class="sxs-lookup"><span data-stu-id="852d7-118">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="852d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="852d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="852d7-120">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="852d7-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="852d7-121">— Status</span><span class="sxs-lookup"><span data-stu-id="852d7-121">-Status</span></span>
<span data-ttu-id="852d7-122">Wskazuje, że to polecenie cmdlet uzyskuje widok wystąpienia rozszerzenia DSC.</span><span class="sxs-lookup"><span data-stu-id="852d7-122">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="852d7-123">— MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="852d7-123">-VM</span></span>
<span data-ttu-id="852d7-124">Określa obiekt maszyny wirtualnej, dla których rozszerzenie jest wł.</span><span class="sxs-lookup"><span data-stu-id="852d7-124">Specifies the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="852d7-125">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="852d7-125">-VMName</span></span>
<span data-ttu-id="852d7-126">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet uzyskuje rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="852d7-126">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="852d7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="852d7-127">CommonParameters</span></span>
<span data-ttu-id="852d7-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="852d7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="852d7-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="852d7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="852d7-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="852d7-130">INPUTS</span></span>

### <span data-ttu-id="852d7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="852d7-131">System.String</span></span>

### <span data-ttu-id="852d7-132">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="852d7-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="852d7-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="852d7-133">OUTPUTS</span></span>

### <span data-ttu-id="852d7-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="852d7-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="852d7-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="852d7-135">NOTES</span></span>

## <span data-ttu-id="852d7-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="852d7-136">RELATED LINKS</span></span>

[<span data-ttu-id="852d7-137">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="852d7-137">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="852d7-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="852d7-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


