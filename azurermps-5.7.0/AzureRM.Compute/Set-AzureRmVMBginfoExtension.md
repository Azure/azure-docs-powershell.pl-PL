---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: c52be698b216d206fe95ba5ea3aefc810f22fff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526925"
---
# <span data-ttu-id="9935e-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="9935e-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="9935e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9935e-102">SYNOPSIS</span></span>
<span data-ttu-id="9935e-103">Dodaje rozszerzenie BGInfo do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9935e-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9935e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9935e-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9935e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9935e-105">DESCRIPTION</span></span>
<span data-ttu-id="9935e-106">Polecenie cmdlet **Set-AzureRmVMBGInfoExtension** dodaje rozszerzenie BgInfo do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9935e-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="9935e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9935e-107">EXAMPLES</span></span>

### <span data-ttu-id="9935e-108">Przykład 1: Dodawanie rozszerzenia BGInfo do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9935e-108">Example 1: Add the BGInfo extension to a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM"
```
<span data-ttu-id="9935e-109">To polecenie powoduje dodanie rozszerzenia BGInfo do maszyny wirtualnej o nazwie ContosoVM w ContosoRG grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="9935e-109">This command adds the BGInfo extension to a virtual machine named ContosoVM in the resource group ContosoRG.</span></span>

### <span data-ttu-id="9935e-110">Przykład 2: dodawanie określonej wersji rozszerzenia BGInfo do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9935e-110">Example 2: Add a specific version of BGInfo extension to a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="9935e-111">To polecenie umożliwia dodanie rozszerzenia BGInfo do maszyny wirtualnej o nazwie ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="9935e-111">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="9935e-112">To polecenie określa grupę zasobów i lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9935e-112">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="9935e-113">Polecenie określa nazwę i wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="9935e-113">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="9935e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9935e-114">PARAMETERS</span></span>

### <span data-ttu-id="9935e-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9935e-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="9935e-116">Wskazuje, że to polecenie cmdlet uniemożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="9935e-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="9935e-117">Domyślnie to polecenie cmdlet umożliwia agentowi gościa aktualizowanie rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="9935e-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9935e-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="9935e-118">-ForceRerun</span></span>
<span data-ttu-id="9935e-119">Określa, że rozszerzenie powinno być ponownie uruchomione z tymi samymi ustawieniami publicznymi lub chronionymi.</span><span class="sxs-lookup"><span data-stu-id="9935e-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="9935e-120">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="9935e-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="9935e-121">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="9935e-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9935e-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9935e-122">-Location</span></span>
<span data-ttu-id="9935e-123">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9935e-123">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9935e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9935e-124">-Name</span></span>
<span data-ttu-id="9935e-125">Określa nazwę rozszerzenia BGInfo, które to polecenie cmdlet dodaje do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9935e-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9935e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9935e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9935e-127">Określa nazwę grupy zasobów maszyny wirtualnej, z którą to polecenie cmdlet dodaje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="9935e-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9935e-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9935e-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="9935e-129">Określa wersję rozszerzenia, które to polecenie cmdlet dodaje do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9935e-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9935e-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="9935e-130">-VMName</span></span>
<span data-ttu-id="9935e-131">Określa nazwę maszyny wirtualnej, do której to polecenie cmdlet dodaje rozszerzenie BGInfo.</span><span class="sxs-lookup"><span data-stu-id="9935e-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9935e-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9935e-132">-Confirm</span></span>
<span data-ttu-id="9935e-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9935e-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9935e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9935e-134">-WhatIf</span></span>
<span data-ttu-id="9935e-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9935e-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9935e-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9935e-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9935e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9935e-137">CommonParameters</span></span>
<span data-ttu-id="9935e-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9935e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9935e-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9935e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9935e-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9935e-140">INPUTS</span></span>

### <span data-ttu-id="9935e-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9935e-141">None</span></span>
<span data-ttu-id="9935e-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9935e-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9935e-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9935e-143">OUTPUTS</span></span>

## <span data-ttu-id="9935e-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9935e-144">NOTES</span></span>

## <span data-ttu-id="9935e-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9935e-145">RELATED LINKS</span></span>

