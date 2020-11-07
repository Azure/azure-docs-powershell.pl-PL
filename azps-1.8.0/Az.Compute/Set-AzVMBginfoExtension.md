---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: d49fae13c69e194f0b31c702670639ce486dad81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710203"
---
# <span data-ttu-id="13867-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="13867-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="13867-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13867-102">SYNOPSIS</span></span>
<span data-ttu-id="13867-103">Dodaje rozszerzenie BGInfo do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="13867-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="13867-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13867-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13867-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13867-105">DESCRIPTION</span></span>
<span data-ttu-id="13867-106">Polecenie cmdlet **Set-AzVMBGInfoExtension** dodaje rozszerzenie BgInfo do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="13867-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="13867-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13867-107">EXAMPLES</span></span>

### <span data-ttu-id="13867-108">Przykład 1: Dodawanie rozszerzenia BGInfo dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="13867-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="13867-109">To polecenie umożliwia dodanie rozszerzenia BGInfo do maszyny wirtualnej o nazwie ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="13867-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="13867-110">To polecenie określa grupę zasobów i lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="13867-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="13867-111">Polecenie określa nazwę i wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="13867-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="13867-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13867-112">PARAMETERS</span></span>

### <span data-ttu-id="13867-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13867-113">-DefaultProfile</span></span>
<span data-ttu-id="13867-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13867-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13867-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="13867-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="13867-116">Wskazuje, że to polecenie cmdlet uniemożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="13867-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="13867-117">Domyślnie to polecenie cmdlet umożliwia agentowi gościa aktualizowanie rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="13867-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="13867-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="13867-118">-ForceRerun</span></span>
<span data-ttu-id="13867-119">Określa, że rozszerzenie powinno być ponownie uruchomione z tymi samymi ustawieniami publicznymi lub chronionymi.</span><span class="sxs-lookup"><span data-stu-id="13867-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="13867-120">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="13867-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="13867-121">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="13867-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="13867-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="13867-122">-Location</span></span>
<span data-ttu-id="13867-123">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="13867-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="13867-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13867-124">-Name</span></span>
<span data-ttu-id="13867-125">Określa nazwę rozszerzenia BGInfo, które to polecenie cmdlet dodaje do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="13867-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="13867-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13867-126">-ResourceGroupName</span></span>
<span data-ttu-id="13867-127">Określa nazwę grupy zasobów maszyny wirtualnej, z którą to polecenie cmdlet dodaje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="13867-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="13867-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="13867-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="13867-129">Określa wersję rozszerzenia, które to polecenie cmdlet dodaje do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="13867-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="13867-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="13867-130">-VMName</span></span>
<span data-ttu-id="13867-131">Określa nazwę maszyny wirtualnej, do której to polecenie cmdlet dodaje rozszerzenie BGInfo.</span><span class="sxs-lookup"><span data-stu-id="13867-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="13867-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13867-132">-Confirm</span></span>
<span data-ttu-id="13867-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13867-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13867-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13867-134">-WhatIf</span></span>
<span data-ttu-id="13867-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13867-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13867-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13867-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13867-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13867-137">CommonParameters</span></span>
<span data-ttu-id="13867-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13867-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13867-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13867-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13867-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13867-140">INPUTS</span></span>

### <span data-ttu-id="13867-141">System. String</span><span class="sxs-lookup"><span data-stu-id="13867-141">System.String</span></span>

### <span data-ttu-id="13867-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="13867-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="13867-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13867-143">OUTPUTS</span></span>

### <span data-ttu-id="13867-144">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="13867-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="13867-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13867-145">NOTES</span></span>

## <span data-ttu-id="13867-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13867-146">RELATED LINKS</span></span>
