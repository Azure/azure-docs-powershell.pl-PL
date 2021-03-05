---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: f89260b083d07ca717e1e302c2fb0bb747005d43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981041"
---
# <span data-ttu-id="0745a-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="0745a-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="0745a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0745a-102">SYNOPSIS</span></span>
<span data-ttu-id="0745a-103">Pobiera informacje o rozszerzeniu PROGRAMU VMAccess.</span><span class="sxs-lookup"><span data-stu-id="0745a-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="0745a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0745a-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0745a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0745a-105">DESCRIPTION</span></span>
<span data-ttu-id="0745a-106">Polecenie **cmdlet Get-AzVMAccessExtension** pobiera informacje o rozszerzeniu maszyny wirtualnej programu Virtual Machine Access (MACHINEAccess).</span><span class="sxs-lookup"><span data-stu-id="0745a-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="0745a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0745a-107">EXAMPLES</span></span>

### <span data-ttu-id="0745a-108">Przykład 1. Uzyskiwanie rozszerzenia PROGRAMU VMAccess</span><span class="sxs-lookup"><span data-stu-id="0745a-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="0745a-109">To polecenie otrzymuje rozszerzenie MACHINEAccess o nazwie ContosoTest dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="0745a-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="0745a-110">Przykład 2. Uzyskiwanie widoku wystąpienia rozszerzenia VMAccess</span><span class="sxs-lookup"><span data-stu-id="0745a-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="0745a-111">To polecenie pobiera widok wystąpienia rozszerzenia MACHINEAccess o nazwie ContosoTest dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="0745a-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="0745a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0745a-112">PARAMETERS</span></span>

### <span data-ttu-id="0745a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0745a-113">-DefaultProfile</span></span>
<span data-ttu-id="0745a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0745a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0745a-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0745a-115">-Name</span></span>
<span data-ttu-id="0745a-116">Określa nazwę rozszerzenia, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0745a-116">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0745a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0745a-117">-ResourceGroupName</span></span>
<span data-ttu-id="0745a-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0745a-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0745a-119">— Status</span><span class="sxs-lookup"><span data-stu-id="0745a-119">-Status</span></span>
<span data-ttu-id="0745a-120">Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0745a-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="0745a-121">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="0745a-121">-VMName</span></span>
<span data-ttu-id="0745a-122">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0745a-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0745a-123">To polecenie cmdlet pobiera informacje o programie MACHINEAccess dla maszyny wirtualnej, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0745a-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0745a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0745a-124">CommonParameters</span></span>
<span data-ttu-id="0745a-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0745a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0745a-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0745a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0745a-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0745a-127">INPUTS</span></span>

### <span data-ttu-id="0745a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0745a-128">System.String</span></span>

### <span data-ttu-id="0745a-129">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="0745a-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0745a-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0745a-130">OUTPUTS</span></span>

### <span data-ttu-id="0745a-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="0745a-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="0745a-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0745a-132">NOTES</span></span>

## <span data-ttu-id="0745a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0745a-133">RELATED LINKS</span></span>

[<span data-ttu-id="0745a-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="0745a-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="0745a-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="0745a-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="0745a-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0745a-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


