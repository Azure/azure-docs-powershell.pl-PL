---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: e4c3199218294e1a75a2bc62dd148c3409159ed7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527710"
---
# <span data-ttu-id="1528d-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="1528d-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="1528d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1528d-102">SYNOPSIS</span></span>
<span data-ttu-id="1528d-103">Modyfikuje stan wystąpienia VMSS.</span><span class="sxs-lookup"><span data-stu-id="1528d-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1528d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1528d-104">SYNTAX</span></span>

### <span data-ttu-id="1528d-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1528d-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1528d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="1528d-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1528d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1528d-107">DESCRIPTION</span></span>
<span data-ttu-id="1528d-108">Polecenie cmdlet **Set-AzureRmVmssVM** modyfikuje stan wystąpienia zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1528d-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="1528d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1528d-109">EXAMPLES</span></span>

## <span data-ttu-id="1528d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1528d-110">PARAMETERS</span></span>

### <span data-ttu-id="1528d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1528d-111">-DefaultProfile</span></span>
<span data-ttu-id="1528d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1528d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1528d-113">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1528d-113">-InstanceId</span></span>
<span data-ttu-id="1528d-114">Określa identyfikator wystąpienia VMSS, dla którego to polecenie cmdlet modyfikuje stan.</span><span class="sxs-lookup"><span data-stu-id="1528d-114">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1528d-115">-Reimage</span><span class="sxs-lookup"><span data-stu-id="1528d-115">-Reimage</span></span>
<span data-ttu-id="1528d-116">Wskazuje, że to polecenie cmdlet reobrazuje wystąpienie VMSS.</span><span class="sxs-lookup"><span data-stu-id="1528d-116">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1528d-117">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="1528d-117">-ReimageAll</span></span>
<span data-ttu-id="1528d-118">Wskazuje, że polecenie cmdlet powoduje odobrazowanie wszystkich dysków w wystąpieniu VMSS.</span><span class="sxs-lookup"><span data-stu-id="1528d-118">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1528d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1528d-119">-ResourceGroupName</span></span>
<span data-ttu-id="1528d-120">Określa nazwę grupy zasobów zawierającej wystąpienie VMSS.</span><span class="sxs-lookup"><span data-stu-id="1528d-120">Specifies the name of the resource group that contains the VMSS instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1528d-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1528d-121">-VMScaleSetName</span></span>
<span data-ttu-id="1528d-122">Określa nazwę wystąpienia VMSS, które jest modyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1528d-122">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1528d-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1528d-123">-Confirm</span></span>
<span data-ttu-id="1528d-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1528d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1528d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1528d-125">-WhatIf</span></span>
<span data-ttu-id="1528d-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1528d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1528d-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1528d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1528d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1528d-128">CommonParameters</span></span>
<span data-ttu-id="1528d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1528d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1528d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1528d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1528d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1528d-131">INPUTS</span></span>

## <span data-ttu-id="1528d-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1528d-132">OUTPUTS</span></span>

## <span data-ttu-id="1528d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1528d-133">NOTES</span></span>

## <span data-ttu-id="1528d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1528d-134">RELATED LINKS</span></span>

[<span data-ttu-id="1528d-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="1528d-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
