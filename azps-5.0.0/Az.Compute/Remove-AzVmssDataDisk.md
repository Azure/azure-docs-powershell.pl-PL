---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 908405de847526682d8526ef2e576e6a07893c3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233224"
---
# <span data-ttu-id="e2b09-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="e2b09-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="e2b09-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2b09-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b09-103">Usuwa dysk danych z VMSS.</span><span class="sxs-lookup"><span data-stu-id="e2b09-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="e2b09-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2b09-104">SYNTAX</span></span>

### <span data-ttu-id="e2b09-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b09-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2b09-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b09-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2b09-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e2b09-107">DESCRIPTION</span></span>
<span data-ttu-id="e2b09-108">Polecenie cmdlet **Remove-AzVmssDataDisk** usuwa dysk danych z wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e2b09-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="e2b09-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2b09-109">EXAMPLES</span></span>

### <span data-ttu-id="e2b09-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e2b09-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="e2b09-111">To polecenie usuwa dysk danych o nazwie "DataDisk1" z obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="e2b09-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="e2b09-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e2b09-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="e2b09-113">To polecenie usuwa dysk danych jednostki LUN 0 z obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="e2b09-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="e2b09-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2b09-114">PARAMETERS</span></span>

### <span data-ttu-id="e2b09-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b09-115">-DefaultProfile</span></span>
<span data-ttu-id="e2b09-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2b09-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2b09-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="e2b09-117">-Lun</span></span>
<span data-ttu-id="e2b09-118">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="e2b09-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="e2b09-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2b09-119">-Name</span></span>
<span data-ttu-id="e2b09-120">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="e2b09-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="e2b09-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e2b09-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e2b09-122">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="e2b09-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="e2b09-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2b09-123">-Confirm</span></span>
<span data-ttu-id="e2b09-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2b09-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2b09-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2b09-125">-WhatIf</span></span>
<span data-ttu-id="e2b09-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2b09-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2b09-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e2b09-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2b09-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b09-128">CommonParameters</span></span>
<span data-ttu-id="e2b09-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2b09-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b09-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2b09-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b09-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2b09-131">INPUTS</span></span>

### <span data-ttu-id="e2b09-132">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e2b09-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e2b09-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e2b09-133">System.String</span></span>

### <span data-ttu-id="e2b09-134">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e2b09-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e2b09-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2b09-135">OUTPUTS</span></span>

### <span data-ttu-id="e2b09-136">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e2b09-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e2b09-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2b09-137">NOTES</span></span>

## <span data-ttu-id="e2b09-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2b09-138">RELATED LINKS</span></span>
