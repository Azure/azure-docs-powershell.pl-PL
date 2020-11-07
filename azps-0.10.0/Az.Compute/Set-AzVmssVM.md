---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 8dde17b43de9db13f1f61c909ee8c88b95761751
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891641"
---
# <span data-ttu-id="af891-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="af891-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="af891-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af891-102">SYNOPSIS</span></span>
<span data-ttu-id="af891-103">Modyfikuje stan wystąpienia VMSS.</span><span class="sxs-lookup"><span data-stu-id="af891-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="af891-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af891-104">SYNTAX</span></span>

### <span data-ttu-id="af891-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="af891-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af891-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="af891-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af891-107">Opis</span><span class="sxs-lookup"><span data-stu-id="af891-107">DESCRIPTION</span></span>
<span data-ttu-id="af891-108">Polecenie cmdlet **Set-AzVmssVM** modyfikuje stan wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="af891-108">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="af891-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af891-109">EXAMPLES</span></span>

## <span data-ttu-id="af891-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af891-110">PARAMETERS</span></span>

### <span data-ttu-id="af891-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af891-111">-AsJob</span></span>
<span data-ttu-id="af891-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="af891-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af891-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af891-113">-DefaultProfile</span></span>
<span data-ttu-id="af891-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af891-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af891-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="af891-115">-InstanceId</span></span>
<span data-ttu-id="af891-116">Określa identyfikator wystąpienia VMSS, dla którego to polecenie cmdlet modyfikuje stan.</span><span class="sxs-lookup"><span data-stu-id="af891-116">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="af891-117">-Reimage</span><span class="sxs-lookup"><span data-stu-id="af891-117">-Reimage</span></span>
<span data-ttu-id="af891-118">Wskazuje, że to polecenie cmdlet reobrazuje wystąpienie VMSS.</span><span class="sxs-lookup"><span data-stu-id="af891-118">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="af891-119">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="af891-119">-ReimageAll</span></span>
<span data-ttu-id="af891-120">Wskazuje, że polecenie cmdlet powoduje odobrazowanie wszystkich dysków w wystąpieniu VMSS.</span><span class="sxs-lookup"><span data-stu-id="af891-120">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="af891-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af891-121">-ResourceGroupName</span></span>
<span data-ttu-id="af891-122">Określa nazwę grupy zasobów zawierającej wystąpienie VMSS.</span><span class="sxs-lookup"><span data-stu-id="af891-122">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="af891-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="af891-123">-VMScaleSetName</span></span>
<span data-ttu-id="af891-124">Określa nazwę wystąpienia VMSS, które jest modyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af891-124">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="af891-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af891-125">-Confirm</span></span>
<span data-ttu-id="af891-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af891-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af891-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af891-127">-WhatIf</span></span>
<span data-ttu-id="af891-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af891-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af891-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="af891-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af891-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af891-130">CommonParameters</span></span>
<span data-ttu-id="af891-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af891-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af891-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af891-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af891-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af891-133">INPUTS</span></span>

### <span data-ttu-id="af891-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="af891-134">None</span></span>
<span data-ttu-id="af891-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="af891-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af891-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af891-136">OUTPUTS</span></span>

### <span data-ttu-id="af891-137">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="af891-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="af891-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af891-138">NOTES</span></span>

## <span data-ttu-id="af891-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af891-139">RELATED LINKS</span></span>

[<span data-ttu-id="af891-140">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="af891-140">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
