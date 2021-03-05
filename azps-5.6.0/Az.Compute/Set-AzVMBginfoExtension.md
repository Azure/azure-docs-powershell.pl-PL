---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: 9b8eafaead04c2e2f727676c78bd717b1c6e97c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995709"
---
# <span data-ttu-id="bb2ca-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="bb2ca-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="bb2ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb2ca-102">SYNOPSIS</span></span>
<span data-ttu-id="bb2ca-103">Dodaje rozszerzenie BGInfo do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="bb2ca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb2ca-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb2ca-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb2ca-105">DESCRIPTION</span></span>
<span data-ttu-id="bb2ca-106">Polecenie **cmdlet Set-AzVMBGInfoExtension** dodaje rozszerzenie BGInfo do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="bb2ca-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb2ca-107">EXAMPLES</span></span>

### <span data-ttu-id="bb2ca-108">Przykład 1. Dodawanie rozszerzenia BGInfo dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="bb2ca-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="bb2ca-109">To polecenie dodaje rozszerzenie BGInfo do maszyny wirtualnej o nazwie ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="bb2ca-110">To polecenie określa grupę zasobów i lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="bb2ca-111">To polecenie określa nazwę i wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="bb2ca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb2ca-112">PARAMETERS</span></span>

### <span data-ttu-id="bb2ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb2ca-113">-DefaultProfile</span></span>
<span data-ttu-id="bb2ca-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb2ca-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bb2ca-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bb2ca-116">Wskazuje, że to polecenie cmdlet uniemożliwia automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej przez agenta gościa platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="bb2ca-117">To polecenie cmdlet domyślnie umożliwia agentowi gościowi zaktualizowanie rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ca-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="bb2ca-118">-ForceRerun</span></span>
<span data-ttu-id="bb2ca-119">Określa, że rozszerzenie ma zostać uruchomione ponownie z tym samymi ustawieniami publicznymi lub chronionymi.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="bb2ca-120">Wartość może być dowolnym ciągiem innym niż bieżąca wartość.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="bb2ca-121">Jeśli forceUpdateTag nie zostanie zmieniony, program obsługi nadal stosuje aktualizacje ustawień publicznych lub chronionych.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ca-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bb2ca-122">-Location</span></span>
<span data-ttu-id="bb2ca-123">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-123">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ca-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bb2ca-124">-Name</span></span>
<span data-ttu-id="bb2ca-125">Określa nazwę rozszerzenia BGInfo, które to polecenie cmdlet dodaje do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ca-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bb2ca-126">-NoWait</span></span>
<span data-ttu-id="bb2ca-127">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="bb2ca-128">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ca-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb2ca-129">-ResourceGroupName</span></span>
<span data-ttu-id="bb2ca-130">Określa nazwę grupy zasobów maszyny wirtualnej, do której to polecenie cmdlet dodaje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ca-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bb2ca-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="bb2ca-132">Określa wersję rozszerzenia, które to polecenie cmdlet dodaje do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ca-133">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="bb2ca-133">-VMName</span></span>
<span data-ttu-id="bb2ca-134">Określa nazwę maszyny wirtualnej, do której to polecenie cmdlet dodaje rozszerzenie BGInfo.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ca-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb2ca-135">-Confirm</span></span>
<span data-ttu-id="bb2ca-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ca-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb2ca-137">-WhatIf</span></span>
<span data-ttu-id="bb2ca-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb2ca-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2ca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb2ca-140">CommonParameters</span></span>
<span data-ttu-id="bb2ca-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb2ca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb2ca-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb2ca-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb2ca-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb2ca-143">INPUTS</span></span>

### <span data-ttu-id="bb2ca-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bb2ca-144">System.String</span></span>

### <span data-ttu-id="bb2ca-145">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="bb2ca-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bb2ca-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb2ca-146">OUTPUTS</span></span>

### <span data-ttu-id="bb2ca-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bb2ca-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bb2ca-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb2ca-148">NOTES</span></span>

## <span data-ttu-id="bb2ca-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb2ca-149">RELATED LINKS</span></span>
