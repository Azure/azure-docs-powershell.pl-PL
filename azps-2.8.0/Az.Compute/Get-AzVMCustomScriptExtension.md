---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: add3437794430e0d5e41ab9330072db4ac3e1616
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706417"
---
# <span data-ttu-id="5ecb0-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="5ecb0-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="5ecb0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ecb0-102">SYNOPSIS</span></span>
<span data-ttu-id="5ecb0-103">Pobiera informacje o rozszerzeniu skryptu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="5ecb0-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="5ecb0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ecb0-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ecb0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ecb0-105">DESCRIPTION</span></span>
<span data-ttu-id="5ecb0-106">Polecenie cmdlet **Get-AzVMCustomScriptExtension** pobiera informacje na temat rozszerzenia maszyny wirtualnej skryptu niestandardowego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5ecb0-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="5ecb0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ecb0-107">EXAMPLES</span></span>

### <span data-ttu-id="5ecb0-108">Przykład 1: uzyskiwanie niestandardowego rozszerzenia skryptu</span><span class="sxs-lookup"><span data-stu-id="5ecb0-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="5ecb0-109">To polecenie pobiera niestandardowe rozszerzenie skryptu o nazwie ContosoCustomScript dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="5ecb0-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="5ecb0-110">Przykład 2: pobieranie widoku wystąpienia niestandardowego rozszerzenia skryptu</span><span class="sxs-lookup"><span data-stu-id="5ecb0-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="5ecb0-111">To polecenie pobiera widok wystąpienia niestandardowego rozszerzenia skryptu o nazwie ContosoCustomScript dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="5ecb0-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="5ecb0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ecb0-112">PARAMETERS</span></span>

### <span data-ttu-id="5ecb0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ecb0-113">-DefaultProfile</span></span>
<span data-ttu-id="5ecb0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ecb0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ecb0-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ecb0-115">-Name</span></span>
<span data-ttu-id="5ecb0-116">Określa nazwę niestandardowego rozszerzenia skryptu, w którym to polecenie cmdlet pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="5ecb0-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="5ecb0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ecb0-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ecb0-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5ecb0-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5ecb0-119">-Status</span><span class="sxs-lookup"><span data-stu-id="5ecb0-119">-Status</span></span>
<span data-ttu-id="5ecb0-120">Wskazuje, że to polecenie cmdlet uzyskuje widok wystąpienia niestandardowego rozszerzenia skryptu.</span><span class="sxs-lookup"><span data-stu-id="5ecb0-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="5ecb0-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="5ecb0-121">-VMName</span></span>
<span data-ttu-id="5ecb0-122">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera niestandardowe rozszerzenie skryptu.</span><span class="sxs-lookup"><span data-stu-id="5ecb0-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="5ecb0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ecb0-123">CommonParameters</span></span>
<span data-ttu-id="5ecb0-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ecb0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ecb0-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ecb0-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ecb0-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ecb0-126">INPUTS</span></span>

### <span data-ttu-id="5ecb0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5ecb0-127">System.String</span></span>

### <span data-ttu-id="5ecb0-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5ecb0-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5ecb0-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ecb0-129">OUTPUTS</span></span>

### <span data-ttu-id="5ecb0-130">Microsoft. Azure. Commands. COMPUTE. models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="5ecb0-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="5ecb0-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ecb0-131">NOTES</span></span>

## <span data-ttu-id="5ecb0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ecb0-132">RELATED LINKS</span></span>

[<span data-ttu-id="5ecb0-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5ecb0-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="5ecb0-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5ecb0-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="5ecb0-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="5ecb0-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

