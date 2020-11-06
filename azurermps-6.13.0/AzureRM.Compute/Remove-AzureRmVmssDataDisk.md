---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 1e0c04bd7283bc2a741b5e2a7130e83b35d00133
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551344"
---
# <span data-ttu-id="ef459-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="ef459-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="ef459-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef459-102">SYNOPSIS</span></span>
<span data-ttu-id="ef459-103">Usuwa dysk danych z VMSS.</span><span class="sxs-lookup"><span data-stu-id="ef459-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef459-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef459-104">SYNTAX</span></span>

### <span data-ttu-id="ef459-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef459-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef459-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef459-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef459-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ef459-107">DESCRIPTION</span></span>
<span data-ttu-id="ef459-108">Polecenie cmdlet **Remove-AzureRmVmssDataDisk** usuwa dysk danych z wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ef459-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="ef459-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef459-109">EXAMPLES</span></span>

### <span data-ttu-id="ef459-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ef459-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="ef459-111">To polecenie usuwa dysk danych o nazwie "DataDisk1" z obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="ef459-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="ef459-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ef459-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="ef459-113">To polecenie usuwa dysk danych jednostki LUN 0 z obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="ef459-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="ef459-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef459-114">PARAMETERS</span></span>

### <span data-ttu-id="ef459-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef459-115">-DefaultProfile</span></span>
<span data-ttu-id="ef459-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef459-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef459-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="ef459-117">-Lun</span></span>
<span data-ttu-id="ef459-118">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="ef459-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="ef459-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ef459-119">-Name</span></span>
<span data-ttu-id="ef459-120">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="ef459-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="ef459-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ef459-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ef459-122">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="ef459-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="ef459-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef459-123">-Confirm</span></span>
<span data-ttu-id="ef459-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef459-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef459-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef459-125">-WhatIf</span></span>
<span data-ttu-id="ef459-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef459-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef459-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef459-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef459-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef459-128">CommonParameters</span></span>
<span data-ttu-id="ef459-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef459-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef459-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef459-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef459-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef459-131">INPUTS</span></span>

### <span data-ttu-id="ef459-132">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ef459-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ef459-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ef459-133">System.String</span></span>

### <span data-ttu-id="ef459-134">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ef459-134">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ef459-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef459-135">OUTPUTS</span></span>

### <span data-ttu-id="ef459-136">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ef459-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ef459-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef459-137">NOTES</span></span>

## <span data-ttu-id="ef459-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef459-138">RELATED LINKS</span></span>
