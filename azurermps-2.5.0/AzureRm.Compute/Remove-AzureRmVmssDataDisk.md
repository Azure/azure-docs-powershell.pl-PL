---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: 411e822153c0b95bbf30829f8da915039d01ea32
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897485"
---
# <span data-ttu-id="8a7c5-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="8a7c5-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="8a7c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a7c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8a7c5-103">Usuwa dysk danych z VMSS.</span><span class="sxs-lookup"><span data-stu-id="8a7c5-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a7c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a7c5-104">SYNTAX</span></span>

### <span data-ttu-id="8a7c5-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a7c5-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a7c5-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a7c5-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a7c5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8a7c5-107">DESCRIPTION</span></span>
<span data-ttu-id="8a7c5-108">Polecenie cmdlet **Remove-AzureRmVmssDataDisk** usuwa dysk danych z wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8a7c5-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="8a7c5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a7c5-109">EXAMPLES</span></span>

### <span data-ttu-id="8a7c5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a7c5-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="8a7c5-111">To polecenie usuwa dysk danych o nazwie "DataDisk1" z obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="8a7c5-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="8a7c5-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8a7c5-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="8a7c5-113">To polecenie usuwa dysk danych jednostki LUN 0 z obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="8a7c5-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="8a7c5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a7c5-114">PARAMETERS</span></span>

### <span data-ttu-id="8a7c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a7c5-115">-DefaultProfile</span></span>
<span data-ttu-id="8a7c5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a7c5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a7c5-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="8a7c5-117">-Lun</span></span>
<span data-ttu-id="8a7c5-118">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="8a7c5-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="8a7c5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8a7c5-119">-Name</span></span>
<span data-ttu-id="8a7c5-120">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="8a7c5-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="8a7c5-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a7c5-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8a7c5-122">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="8a7c5-122">Specify the VMSS object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a7c5-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a7c5-123">-Confirm</span></span>
<span data-ttu-id="8a7c5-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a7c5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a7c5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a7c5-125">-WhatIf</span></span>
<span data-ttu-id="8a7c5-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a7c5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a7c5-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8a7c5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a7c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a7c5-128">CommonParameters</span></span>
<span data-ttu-id="8a7c5-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a7c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a7c5-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a7c5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a7c5-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a7c5-131">INPUTS</span></span>

### <span data-ttu-id="8a7c5-132">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a7c5-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="8a7c5-133">System. String. Nullable. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8a7c5-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8a7c5-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a7c5-134">OUTPUTS</span></span>

### <span data-ttu-id="8a7c5-135">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a7c5-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="8a7c5-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a7c5-136">NOTES</span></span>

## <span data-ttu-id="8a7c5-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a7c5-137">RELATED LINKS</span></span>

