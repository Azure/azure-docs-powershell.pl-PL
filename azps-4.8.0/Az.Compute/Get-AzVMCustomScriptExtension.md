---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 1d1ccb7f8e47ce34b798124d54fdd85aa18c7d69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062901"
---
# <span data-ttu-id="6a6af-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="6a6af-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="6a6af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a6af-102">SYNOPSIS</span></span>
<span data-ttu-id="6a6af-103">Pobiera informacje o rozszerzeniu skryptu niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="6a6af-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="6a6af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a6af-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a6af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a6af-105">DESCRIPTION</span></span>
<span data-ttu-id="6a6af-106">Polecenie cmdlet **Get-AzVMCustomScriptExtension** pobiera informacje na temat rozszerzenia maszyny wirtualnej skryptu niestandardowego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a6af-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="6a6af-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a6af-107">EXAMPLES</span></span>

### <span data-ttu-id="6a6af-108">Przykład 1: uzyskiwanie niestandardowego rozszerzenia skryptu</span><span class="sxs-lookup"><span data-stu-id="6a6af-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="6a6af-109">To polecenie pobiera niestandardowe rozszerzenie skryptu o nazwie ContosoCustomScript dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="6a6af-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="6a6af-110">Przykład 2: pobieranie widoku wystąpienia niestandardowego rozszerzenia skryptu</span><span class="sxs-lookup"><span data-stu-id="6a6af-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="6a6af-111">To polecenie pobiera widok wystąpienia niestandardowego rozszerzenia skryptu o nazwie ContosoCustomScript dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="6a6af-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="6a6af-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a6af-112">PARAMETERS</span></span>

### <span data-ttu-id="6a6af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a6af-113">-DefaultProfile</span></span>
<span data-ttu-id="6a6af-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a6af-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a6af-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a6af-115">-Name</span></span>
<span data-ttu-id="6a6af-116">Określa nazwę niestandardowego rozszerzenia skryptu, w którym to polecenie cmdlet pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="6a6af-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="6a6af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a6af-117">-ResourceGroupName</span></span>
<span data-ttu-id="6a6af-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6a6af-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6a6af-119">-Status</span><span class="sxs-lookup"><span data-stu-id="6a6af-119">-Status</span></span>
<span data-ttu-id="6a6af-120">Wskazuje, że to polecenie cmdlet uzyskuje widok wystąpienia niestandardowego rozszerzenia skryptu.</span><span class="sxs-lookup"><span data-stu-id="6a6af-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="6a6af-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="6a6af-121">-VMName</span></span>
<span data-ttu-id="6a6af-122">Określa nazwę maszyny wirtualnej, dla której to polecenie cmdlet pobiera niestandardowe rozszerzenie skryptu.</span><span class="sxs-lookup"><span data-stu-id="6a6af-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="6a6af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a6af-123">CommonParameters</span></span>
<span data-ttu-id="6a6af-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a6af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a6af-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a6af-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a6af-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a6af-126">INPUTS</span></span>

### <span data-ttu-id="6a6af-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6a6af-127">System.String</span></span>

### <span data-ttu-id="6a6af-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6a6af-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6a6af-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a6af-129">OUTPUTS</span></span>

### <span data-ttu-id="6a6af-130">Microsoft. Azure. Commands. COMPUTE. models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="6a6af-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="6a6af-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a6af-131">NOTES</span></span>

## <span data-ttu-id="6a6af-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a6af-132">RELATED LINKS</span></span>

[<span data-ttu-id="6a6af-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6a6af-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="6a6af-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="6a6af-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="6a6af-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="6a6af-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


