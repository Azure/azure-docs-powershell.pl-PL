---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 908405de847526682d8526ef2e576e6a07893c3a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181554"
---
# <span data-ttu-id="a7a4b-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="a7a4b-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="a7a4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a4b-103">Usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a7a4b-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="a7a4b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a7a4b-104">SYNTAX</span></span>

### <span data-ttu-id="a7a4b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7a4b-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7a4b-106">ŚleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7a4b-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7a4b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a7a4b-107">DESCRIPTION</span></span>
<span data-ttu-id="a7a4b-108">Polecenie **cmdlet Remove-AzVmssDataData Można** usunąć z wystąpienia zestawu skal maszyn wirtualnych (VIRTUAL Machine Scale Set) dysku danych.</span><span class="sxs-lookup"><span data-stu-id="a7a4b-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="a7a4b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a7a4b-109">EXAMPLES</span></span>

### <span data-ttu-id="a7a4b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a7a4b-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="a7a4b-111">To polecenie usuwa dysk danych o nazwie "Data Jednak1" z obiektu MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="a7a4b-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="a7a4b-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a7a4b-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="a7a4b-113">To polecenie usuwa dysk danych DEFRAGMENT 0 z obiektu MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="a7a4b-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="a7a4b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7a4b-114">PARAMETERS</span></span>

### <span data-ttu-id="a7a4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a4b-115">-DefaultProfile</span></span>
<span data-ttu-id="a7a4b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7a4b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7a4b-117">-Logicznej</span><span class="sxs-lookup"><span data-stu-id="a7a4b-117">-Lun</span></span>
<span data-ttu-id="a7a4b-118">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="a7a4b-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7a4b-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a7a4b-119">-Name</span></span>
<span data-ttu-id="a7a4b-120">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="a7a4b-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="a7a4b-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a7a4b-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a7a4b-122">Określanie obiektu MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="a7a4b-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="a7a4b-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7a4b-123">-Confirm</span></span>
<span data-ttu-id="a7a4b-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a7a4b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7a4b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7a4b-125">-WhatIf</span></span>
<span data-ttu-id="a7a4b-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7a4b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7a4b-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a7a4b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7a4b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a4b-128">CommonParameters</span></span>
<span data-ttu-id="a7a4b-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7a4b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a4b-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7a4b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a4b-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7a4b-131">INPUTS</span></span>

### <span data-ttu-id="a7a4b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a7a4b-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a7a4b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a7a4b-133">System.String</span></span>

### <span data-ttu-id="a7a4b-134">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a7a4b-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a7a4b-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7a4b-135">OUTPUTS</span></span>

### <span data-ttu-id="a7a4b-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a7a4b-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a7a4b-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a7a4b-137">NOTES</span></span>

## <span data-ttu-id="a7a4b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7a4b-138">RELATED LINKS</span></span>
