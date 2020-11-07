---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: 21b8b73d1063881104b799c016c2cfab618a9705
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893398"
---
# <span data-ttu-id="f5f4f-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="f5f4f-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="f5f4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f4f-103">Dodaje rozszerzenie BGInfo do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="f5f4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5f4f-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5f4f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f5f4f-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f4f-106">Polecenie cmdlet **Set-AzVMBGInfoExtension** dodaje rozszerzenie BgInfo do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="f5f4f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5f4f-107">EXAMPLES</span></span>

### <span data-ttu-id="f5f4f-108">Przykład 1: Dodawanie rozszerzenia BGInfo dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f5f4f-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -ResrouceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="f5f4f-109">To polecenie umożliwia dodanie rozszerzenia BGInfo do maszyny wirtualnej o nazwie ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="f5f4f-110">To polecenie określa grupę zasobów i lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="f5f4f-111">Polecenie określa nazwę i wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="f5f4f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5f4f-112">PARAMETERS</span></span>

### <span data-ttu-id="f5f4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f4f-113">-DefaultProfile</span></span>
<span data-ttu-id="f5f4f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5f4f-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f5f4f-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f5f4f-116">Wskazuje, że to polecenie cmdlet uniemożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="f5f4f-117">Domyślnie to polecenie cmdlet umożliwia agentowi gościa aktualizowanie rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="f5f4f-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f5f4f-118">-ForceRerun</span></span>
<span data-ttu-id="f5f4f-119">Określa, że rozszerzenie powinno być ponownie uruchomione z tymi samymi ustawieniami publicznymi lub chronionymi.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="f5f4f-120">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="f5f4f-121">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="f5f4f-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f5f4f-122">-Location</span></span>
<span data-ttu-id="f5f4f-123">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="f5f4f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5f4f-124">-Name</span></span>
<span data-ttu-id="f5f4f-125">Określa nazwę rozszerzenia BGInfo, które to polecenie cmdlet dodaje do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="f5f4f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f4f-126">-ResourceGroupName</span></span>
<span data-ttu-id="f5f4f-127">Określa nazwę grupy zasobów maszyny wirtualnej, z którą to polecenie cmdlet dodaje rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="f5f4f-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f5f4f-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="f5f4f-129">Określa wersję rozszerzenia, które to polecenie cmdlet dodaje do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="f5f4f-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="f5f4f-130">-VMName</span></span>
<span data-ttu-id="f5f4f-131">Określa nazwę maszyny wirtualnej, do której to polecenie cmdlet dodaje rozszerzenie BGInfo.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="f5f4f-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5f4f-132">-Confirm</span></span>
<span data-ttu-id="f5f4f-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5f4f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5f4f-134">-WhatIf</span></span>
<span data-ttu-id="f5f4f-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f5f4f-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5f4f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f4f-137">CommonParameters</span></span>
<span data-ttu-id="f5f4f-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f4f-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f4f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f4f-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5f4f-140">INPUTS</span></span>

### <span data-ttu-id="f5f4f-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f5f4f-141">None</span></span>
<span data-ttu-id="f5f4f-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f5f4f-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5f4f-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5f4f-143">OUTPUTS</span></span>

### <span data-ttu-id="f5f4f-144">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f5f4f-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f5f4f-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5f4f-145">NOTES</span></span>

## <span data-ttu-id="f5f4f-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5f4f-146">RELATED LINKS</span></span>

