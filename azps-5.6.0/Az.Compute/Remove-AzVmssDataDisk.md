---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: abdef821862976a3bffb0b39bc48a3619e17d64f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998873"
---
# <span data-ttu-id="97c02-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="97c02-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="97c02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97c02-102">SYNOPSIS</span></span>
<span data-ttu-id="97c02-103">Usuwa dysk danych z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97c02-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="97c02-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="97c02-104">SYNTAX</span></span>

### <span data-ttu-id="97c02-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="97c02-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c02-106">ŚleParameterSet</span><span class="sxs-lookup"><span data-stu-id="97c02-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97c02-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="97c02-107">DESCRIPTION</span></span>
<span data-ttu-id="97c02-108">Polecenie **cmdlet Remove-AzVmssDataDataS** usuwa dysk danych z wystąpienia zestawu skal maszyny wirtualnej (VIRTUAL Machine Scale Set, VIRTUALSS).</span><span class="sxs-lookup"><span data-stu-id="97c02-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="97c02-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="97c02-109">EXAMPLES</span></span>

### <span data-ttu-id="97c02-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97c02-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="97c02-111">To polecenie usuwa dysk danych o nazwie "Data Jednak1" z obiektu MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="97c02-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="97c02-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="97c02-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="97c02-113">To polecenie usuwa dysk danych DEFRAGMENT 0 z obiektu MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="97c02-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="97c02-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97c02-114">PARAMETERS</span></span>

### <span data-ttu-id="97c02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c02-115">-DefaultProfile</span></span>
<span data-ttu-id="97c02-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="97c02-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97c02-117">-Logicznej</span><span class="sxs-lookup"><span data-stu-id="97c02-117">-Lun</span></span>
<span data-ttu-id="97c02-118">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="97c02-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="97c02-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="97c02-119">-Name</span></span>
<span data-ttu-id="97c02-120">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="97c02-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="97c02-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="97c02-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="97c02-122">Określanie obiektu MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="97c02-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="97c02-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97c02-123">-Confirm</span></span>
<span data-ttu-id="97c02-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="97c02-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97c02-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97c02-125">-WhatIf</span></span>
<span data-ttu-id="97c02-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97c02-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97c02-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="97c02-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97c02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c02-128">CommonParameters</span></span>
<span data-ttu-id="97c02-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c02-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97c02-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c02-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97c02-131">INPUTS</span></span>

### <span data-ttu-id="97c02-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="97c02-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="97c02-133">System.String</span><span class="sxs-lookup"><span data-stu-id="97c02-133">System.String</span></span>

### <span data-ttu-id="97c02-134">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="97c02-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="97c02-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97c02-135">OUTPUTS</span></span>

### <span data-ttu-id="97c02-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="97c02-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="97c02-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="97c02-137">NOTES</span></span>

## <span data-ttu-id="97c02-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97c02-138">RELATED LINKS</span></span>
