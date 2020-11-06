---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: d035844046e238694cfec72feda9eab61b7714d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546839"
---
# <span data-ttu-id="ec2f0-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="ec2f0-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="ec2f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec2f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ec2f0-103">Modyfikuje stan wystąpienia VMSS.</span><span class="sxs-lookup"><span data-stu-id="ec2f0-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec2f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec2f0-104">SYNTAX</span></span>

### <span data-ttu-id="ec2f0-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ec2f0-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec2f0-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ec2f0-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec2f0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ec2f0-107">DESCRIPTION</span></span>
<span data-ttu-id="ec2f0-108">Polecenie cmdlet **Set-AzureRmVmssVM** modyfikuje stan wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ec2f0-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="ec2f0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec2f0-109">EXAMPLES</span></span>

## <span data-ttu-id="ec2f0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec2f0-110">PARAMETERS</span></span>

### <span data-ttu-id="ec2f0-111">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="ec2f0-111">-InstanceId</span></span>
<span data-ttu-id="ec2f0-112">Określa identyfikator wystąpienia VMSS, dla którego to polecenie cmdlet modyfikuje stan.</span><span class="sxs-lookup"><span data-stu-id="ec2f0-112">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f0-113">-Reimage</span><span class="sxs-lookup"><span data-stu-id="ec2f0-113">-Reimage</span></span>
<span data-ttu-id="ec2f0-114">Wskazuje, że to polecenie cmdlet reobrazuje wystąpienie VMSS.</span><span class="sxs-lookup"><span data-stu-id="ec2f0-114">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f0-115">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="ec2f0-115">-ReimageAll</span></span>
<span data-ttu-id="ec2f0-116">Wskazuje, że polecenie cmdlet powoduje odobrazowanie wszystkich dysków w wystąpieniu VMSS.</span><span class="sxs-lookup"><span data-stu-id="ec2f0-116">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec2f0-117">-ResourceGroupName</span></span>
<span data-ttu-id="ec2f0-118">Określa nazwę grupy zasobów zawierającej wystąpienie VMSS.</span><span class="sxs-lookup"><span data-stu-id="ec2f0-118">Specifies the name of the resource group that contains the VMSS instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f0-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ec2f0-119">-VMScaleSetName</span></span>
<span data-ttu-id="ec2f0-120">Określa nazwę wystąpienia VMSS, które jest modyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec2f0-120">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec2f0-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec2f0-121">-Confirm</span></span>
<span data-ttu-id="ec2f0-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec2f0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec2f0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec2f0-123">-WhatIf</span></span>
<span data-ttu-id="ec2f0-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec2f0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec2f0-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ec2f0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec2f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec2f0-126">CommonParameters</span></span>
<span data-ttu-id="ec2f0-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec2f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec2f0-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec2f0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec2f0-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec2f0-129">INPUTS</span></span>

### <span data-ttu-id="ec2f0-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ec2f0-130">None</span></span>
<span data-ttu-id="ec2f0-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ec2f0-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ec2f0-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec2f0-132">OUTPUTS</span></span>

## <span data-ttu-id="ec2f0-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec2f0-133">NOTES</span></span>

## <span data-ttu-id="ec2f0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec2f0-134">RELATED LINKS</span></span>

[<span data-ttu-id="ec2f0-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="ec2f0-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
