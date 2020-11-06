---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: efb24aa4f8770e1911b9bf85a1fbf4dd366ea34d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525565"
---
# <span data-ttu-id="33598-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33598-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="33598-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33598-102">SYNOPSIS</span></span>
<span data-ttu-id="33598-103">Ustawia określone akcje na określonym VMSS.</span><span class="sxs-lookup"><span data-stu-id="33598-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33598-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33598-104">SYNTAX</span></span>

### <span data-ttu-id="33598-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="33598-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33598-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="33598-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33598-107">Opis</span><span class="sxs-lookup"><span data-stu-id="33598-107">DESCRIPTION</span></span>
<span data-ttu-id="33598-108">Polecenie cmdlet **Set-AzureRmVmss** ustawia określone akcje na zestawie skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="33598-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="33598-109">Jedyna akcja obsługiwana przez ten aplet polecenia to Reimage.</span><span class="sxs-lookup"><span data-stu-id="33598-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="33598-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33598-110">EXAMPLES</span></span>

### <span data-ttu-id="33598-111">Przykład 1: odobrazowanie VMSS</span><span class="sxs-lookup"><span data-stu-id="33598-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="33598-112">To polecenie powoduje ponowne zdjęcie VMSS o nazwie ContosoVMSS należącej do grupy zasobów o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="33598-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="33598-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33598-113">PARAMETERS</span></span>

### <span data-ttu-id="33598-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33598-114">-DefaultProfile</span></span>
<span data-ttu-id="33598-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33598-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33598-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="33598-116">-InstanceId</span></span>
<span data-ttu-id="33598-117">Identyfikator wystąpienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="33598-117">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33598-118">-Reimage</span><span class="sxs-lookup"><span data-stu-id="33598-118">-Reimage</span></span>
<span data-ttu-id="33598-119">Wskazuje, że polecenie cmdlet reobrazuje VMSS.</span><span class="sxs-lookup"><span data-stu-id="33598-119">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="33598-120">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="33598-120">-ReimageAll</span></span>
<span data-ttu-id="33598-121">Wskazuje, że polecenie cmdlet reobrazuje wszystkie dyski w VMSS.</span><span class="sxs-lookup"><span data-stu-id="33598-121">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="33598-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33598-122">-ResourceGroupName</span></span>
<span data-ttu-id="33598-123">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="33598-123">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="33598-124">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="33598-124">-VMScaleSetName</span></span>
<span data-ttu-id="33598-125">Gatunek nazwa VMSS, dla którego to polecenie cmdlet ustawia akcje.</span><span class="sxs-lookup"><span data-stu-id="33598-125">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="33598-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33598-126">-Confirm</span></span>
<span data-ttu-id="33598-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33598-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33598-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33598-128">-WhatIf</span></span>
<span data-ttu-id="33598-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33598-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33598-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="33598-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33598-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33598-131">CommonParameters</span></span>
<span data-ttu-id="33598-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33598-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33598-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33598-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33598-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33598-134">INPUTS</span></span>

## <span data-ttu-id="33598-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33598-135">OUTPUTS</span></span>

### <span data-ttu-id="33598-136">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="33598-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="33598-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33598-137">NOTES</span></span>

## <span data-ttu-id="33598-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33598-138">RELATED LINKS</span></span>

[<span data-ttu-id="33598-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33598-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="33598-140">Nowe — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33598-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="33598-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33598-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="33598-142">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33598-142">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="33598-143">Start — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33598-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="33598-144">Zatrzymaj — AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33598-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="33598-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33598-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


