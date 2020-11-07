---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 293bb0f314b82ed2318684996f9b18c79a3b81d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716503"
---
# <span data-ttu-id="37516-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="37516-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="37516-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37516-102">SYNOPSIS</span></span>
<span data-ttu-id="37516-103">Usuwa dysk danych z VMSS.</span><span class="sxs-lookup"><span data-stu-id="37516-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37516-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37516-104">SYNTAX</span></span>

### <span data-ttu-id="37516-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="37516-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37516-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="37516-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Lun] <Int32> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37516-107">Opis</span><span class="sxs-lookup"><span data-stu-id="37516-107">DESCRIPTION</span></span>
<span data-ttu-id="37516-108">Polecenie cmdlet **Remove-AzureRmVmssDataDisk** usuwa dysk danych z wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="37516-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="37516-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37516-109">EXAMPLES</span></span>

### <span data-ttu-id="37516-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37516-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="37516-111">To polecenie usuwa dysk danych o nazwie "DataDisk1" z obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="37516-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="37516-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="37516-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="37516-113">To polecenie usuwa dysk danych jednostki LUN 0 z obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="37516-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="37516-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37516-114">PARAMETERS</span></span>

### <span data-ttu-id="37516-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="37516-115">-Lun</span></span>
<span data-ttu-id="37516-116">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="37516-116">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37516-117">-Name</span></span>
<span data-ttu-id="37516-118">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="37516-118">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-119">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="37516-119">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="37516-120">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="37516-120">Specify the VMSS object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37516-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37516-121">-Confirm</span></span>
<span data-ttu-id="37516-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37516-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37516-123">-WhatIf</span></span>
<span data-ttu-id="37516-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37516-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37516-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="37516-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37516-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37516-126">CommonParameters</span></span>
<span data-ttu-id="37516-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37516-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37516-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37516-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37516-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37516-129">INPUTS</span></span>

### <span data-ttu-id="37516-130">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="37516-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="37516-131">System. String. Nullable. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="37516-131">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="37516-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37516-132">OUTPUTS</span></span>

### <span data-ttu-id="37516-133">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="37516-133">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="37516-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37516-134">NOTES</span></span>

## <span data-ttu-id="37516-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37516-135">RELATED LINKS</span></span>

