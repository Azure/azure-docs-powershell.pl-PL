---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 30836628d6be41e06eaf8982fcc59646fb5b5e89
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893502"
---
# <span data-ttu-id="46b3e-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="46b3e-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="46b3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="46b3e-103">Usuwa dysk danych z VMSS.</span><span class="sxs-lookup"><span data-stu-id="46b3e-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="46b3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46b3e-104">SYNTAX</span></span>

### <span data-ttu-id="46b3e-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="46b3e-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46b3e-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="46b3e-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46b3e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="46b3e-107">DESCRIPTION</span></span>
<span data-ttu-id="46b3e-108">Polecenie cmdlet **Remove-AzVmssDataDisk** usuwa dysk danych z wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="46b3e-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="46b3e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46b3e-109">EXAMPLES</span></span>

### <span data-ttu-id="46b3e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46b3e-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="46b3e-111">To polecenie usuwa dysk danych o nazwie "DataDisk1" z obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="46b3e-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="46b3e-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="46b3e-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="46b3e-113">To polecenie usuwa dysk danych jednostki LUN 0 z obiektu VMSS.</span><span class="sxs-lookup"><span data-stu-id="46b3e-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="46b3e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46b3e-114">PARAMETERS</span></span>

### <span data-ttu-id="46b3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b3e-115">-DefaultProfile</span></span>
<span data-ttu-id="46b3e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46b3e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46b3e-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="46b3e-117">-Lun</span></span>
<span data-ttu-id="46b3e-118">Określa numer jednostki logicznej dysku.</span><span class="sxs-lookup"><span data-stu-id="46b3e-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="46b3e-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46b3e-119">-Name</span></span>
<span data-ttu-id="46b3e-120">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="46b3e-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="46b3e-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="46b3e-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="46b3e-122">Określ obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="46b3e-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="46b3e-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46b3e-123">-Confirm</span></span>
<span data-ttu-id="46b3e-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46b3e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46b3e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46b3e-125">-WhatIf</span></span>
<span data-ttu-id="46b3e-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46b3e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46b3e-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46b3e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46b3e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b3e-128">CommonParameters</span></span>
<span data-ttu-id="46b3e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b3e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b3e-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46b3e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b3e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46b3e-131">INPUTS</span></span>

### <span data-ttu-id="46b3e-132">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="46b3e-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="46b3e-133">System. String. Nullable. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="46b3e-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="46b3e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46b3e-134">OUTPUTS</span></span>

### <span data-ttu-id="46b3e-135">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="46b3e-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="46b3e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46b3e-136">NOTES</span></span>

## <span data-ttu-id="46b3e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46b3e-137">RELATED LINKS</span></span>

