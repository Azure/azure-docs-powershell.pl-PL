---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: 3f9b425574f8f6d1524d2a4fd9d36c0bb57784f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231965"
---
# <span data-ttu-id="3704d-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3704d-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="3704d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3704d-102">SYNOPSIS</span></span>
<span data-ttu-id="3704d-103">Modyfikowanie właściwości diagnostyki rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3704d-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="3704d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3704d-104">SYNTAX</span></span>

### <span data-ttu-id="3704d-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3704d-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3704d-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3704d-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3704d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3704d-107">DESCRIPTION</span></span>
<span data-ttu-id="3704d-108">Polecenie cmdlet **Set-AzVMBootDiagnostic** modyfikuje właściwości diagnostyki rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3704d-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="3704d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3704d-109">EXAMPLES</span></span>

### <span data-ttu-id="3704d-110">Przykład 1: Włączanie diagnostyki rozruchu</span><span class="sxs-lookup"><span data-stu-id="3704d-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzVM -VM $VM
```

<span data-ttu-id="3704d-111">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie ContosoVM07 przy użyciu polecenia **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="3704d-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="3704d-112">Polecenie zapisuje je w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="3704d-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="3704d-113">Drugie polecenie włącza diagnostykę rozruchu maszyny wirtualnej w $VM.</span><span class="sxs-lookup"><span data-stu-id="3704d-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="3704d-114">Dane diagnostyczne są przechowywane na określonym koncie.</span><span class="sxs-lookup"><span data-stu-id="3704d-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="3704d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3704d-115">PARAMETERS</span></span>

### <span data-ttu-id="3704d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3704d-116">-DefaultProfile</span></span>
<span data-ttu-id="3704d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3704d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3704d-118">-Disable</span><span class="sxs-lookup"><span data-stu-id="3704d-118">-Disable</span></span>
<span data-ttu-id="3704d-119">Wskazuje, że to polecenie cmdlet wyłącza diagnostykę rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3704d-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3704d-120">-Enable</span><span class="sxs-lookup"><span data-stu-id="3704d-120">-Enable</span></span>
<span data-ttu-id="3704d-121">Wskazuje, że to polecenie cmdlet włącza diagnostykę rozruchu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3704d-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3704d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3704d-122">-ResourceGroupName</span></span>
<span data-ttu-id="3704d-123">Określa nazwę grupy zasobów konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3704d-123">Specifies the name of the resource group of storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3704d-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3704d-124">-StorageAccountName</span></span>
<span data-ttu-id="3704d-125">Określa nazwę konta magazynu, w którym mają być zapisywane dane diagnostyczne rozruchu.</span><span class="sxs-lookup"><span data-stu-id="3704d-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3704d-126">-VM</span><span class="sxs-lookup"><span data-stu-id="3704d-126">-VM</span></span>
<span data-ttu-id="3704d-127">Określa maszynę wirtualną, dla której to polecenie cmdlet zmienia narzędzie diagnostyczne rozruchu.</span><span class="sxs-lookup"><span data-stu-id="3704d-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="3704d-128">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="3704d-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3704d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3704d-129">CommonParameters</span></span>
<span data-ttu-id="3704d-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3704d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3704d-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3704d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3704d-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3704d-132">INPUTS</span></span>

### <span data-ttu-id="3704d-133">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3704d-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="3704d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3704d-134">System.String</span></span>

## <span data-ttu-id="3704d-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3704d-135">OUTPUTS</span></span>

### <span data-ttu-id="3704d-136">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3704d-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3704d-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3704d-137">NOTES</span></span>

## <span data-ttu-id="3704d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3704d-138">RELATED LINKS</span></span>

[<span data-ttu-id="3704d-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3704d-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3704d-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="3704d-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


