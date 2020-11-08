---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062904"
---
# <span data-ttu-id="ad614-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ad614-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="ad614-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad614-102">SYNOPSIS</span></span>
<span data-ttu-id="ad614-103">Pobiera informacje o rozszerzeniu VMAccess.</span><span class="sxs-lookup"><span data-stu-id="ad614-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="ad614-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad614-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad614-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad614-105">DESCRIPTION</span></span>
<span data-ttu-id="ad614-106">Polecenie cmdlet **Get-AzVMAccessExtension** pobiera informacje o rozszerzeniu maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="ad614-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="ad614-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad614-107">EXAMPLES</span></span>

### <span data-ttu-id="ad614-108">Przykład 1: uzyskiwanie rozszerzenia VMAccess</span><span class="sxs-lookup"><span data-stu-id="ad614-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="ad614-109">To polecenie uzyskuje rozszerzenie VMAccess o nazwie ContosoTest dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="ad614-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="ad614-110">Przykład 2: uzyskiwanie widoku wystąpienia rozszerzenia VMAccess</span><span class="sxs-lookup"><span data-stu-id="ad614-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="ad614-111">To polecenie pobiera widok wystąpienia rozszerzenia VMAccess o nazwie ContosoTest dla maszyny wirtualnej o nazwie VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="ad614-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="ad614-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad614-112">PARAMETERS</span></span>

### <span data-ttu-id="ad614-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad614-113">-DefaultProfile</span></span>
<span data-ttu-id="ad614-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad614-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad614-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad614-115">-Name</span></span>
<span data-ttu-id="ad614-116">Określa nazwę rozszerzenia, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad614-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ad614-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad614-117">-ResourceGroupName</span></span>
<span data-ttu-id="ad614-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ad614-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ad614-119">-Status</span><span class="sxs-lookup"><span data-stu-id="ad614-119">-Status</span></span>
<span data-ttu-id="ad614-120">Wskazuje, że ten aplet polecenia pobiera tylko widok wystąpienia rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ad614-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="ad614-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="ad614-121">-VMName</span></span>
<span data-ttu-id="ad614-122">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ad614-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ad614-123">To polecenie cmdlet umożliwia pobieranie informacji o VMAccess dla maszyny wirtualnej określanej przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="ad614-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ad614-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad614-124">CommonParameters</span></span>
<span data-ttu-id="ad614-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad614-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad614-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad614-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad614-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad614-127">INPUTS</span></span>

### <span data-ttu-id="ad614-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ad614-128">System.String</span></span>

### <span data-ttu-id="ad614-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ad614-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ad614-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad614-130">OUTPUTS</span></span>

### <span data-ttu-id="ad614-131">Microsoft. Azure. Commands. COMPUTE. models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="ad614-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="ad614-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad614-132">NOTES</span></span>

## <span data-ttu-id="ad614-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad614-133">RELATED LINKS</span></span>

[<span data-ttu-id="ad614-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ad614-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="ad614-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ad614-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="ad614-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ad614-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


