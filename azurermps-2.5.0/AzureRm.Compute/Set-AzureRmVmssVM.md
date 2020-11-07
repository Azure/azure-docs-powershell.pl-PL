---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: ffce87e30fb5bffa78cb10a85b1ac8a143deeaad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899364"
---
# <span data-ttu-id="0eb5f-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="0eb5f-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="0eb5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0eb5f-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb5f-103">Modyfikuje stan wystąpienia VMSS.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eb5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0eb5f-104">SYNTAX</span></span>

### <span data-ttu-id="0eb5f-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0eb5f-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb5f-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="0eb5f-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb5f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0eb5f-107">DESCRIPTION</span></span>
<span data-ttu-id="0eb5f-108">Polecenie cmdlet **Set-AzureRmVmssVM** modyfikuje stan wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0eb5f-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="0eb5f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0eb5f-109">EXAMPLES</span></span>

## <span data-ttu-id="0eb5f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0eb5f-110">PARAMETERS</span></span>

### <span data-ttu-id="0eb5f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0eb5f-111">-AsJob</span></span>
<span data-ttu-id="0eb5f-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0eb5f-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb5f-113">-DefaultProfile</span></span>
<span data-ttu-id="0eb5f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eb5f-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="0eb5f-115">-InstanceId</span></span>
<span data-ttu-id="0eb5f-116">Określa identyfikator wystąpienia VMSS, dla którego to polecenie cmdlet modyfikuje stan.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="0eb5f-117">-Reimage</span><span class="sxs-lookup"><span data-stu-id="0eb5f-117">-Reimage</span></span>
<span data-ttu-id="0eb5f-118">Wskazuje, że to polecenie cmdlet reobrazuje wystąpienie VMSS.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb5f-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="0eb5f-119">-ReimageAll</span></span>
<span data-ttu-id="0eb5f-120">Wskazuje, że polecenie cmdlet powoduje odobrazowanie wszystkich dysków w wystąpieniu VMSS.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb5f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb5f-121">-ResourceGroupName</span></span>
<span data-ttu-id="0eb5f-122">Określa nazwę grupy zasobów zawierającej wystąpienie VMSS.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="0eb5f-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0eb5f-123">-VMScaleSetName</span></span>
<span data-ttu-id="0eb5f-124">Określa nazwę wystąpienia VMSS, które jest modyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0eb5f-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0eb5f-125">-Confirm</span></span>
<span data-ttu-id="0eb5f-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb5f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb5f-127">-WhatIf</span></span>
<span data-ttu-id="0eb5f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0eb5f-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb5f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb5f-130">CommonParameters</span></span>
<span data-ttu-id="0eb5f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb5f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eb5f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb5f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0eb5f-133">INPUTS</span></span>

### <span data-ttu-id="0eb5f-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0eb5f-134">None</span></span>
<span data-ttu-id="0eb5f-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0eb5f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0eb5f-136">OUTPUTS</span></span>

### <span data-ttu-id="0eb5f-137">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0eb5f-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0eb5f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0eb5f-138">NOTES</span></span>

## <span data-ttu-id="0eb5f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0eb5f-139">RELATED LINKS</span></span>

[<span data-ttu-id="0eb5f-140">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="0eb5f-140">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
