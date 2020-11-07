---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 069b98f585d606ade255cfecd223be4a074d8316
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898761"
---
# <span data-ttu-id="1ee0b-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1ee0b-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="1ee0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ee0b-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee0b-103">Dodaje rozszerzenie VMAccess do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ee0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ee0b-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ee0b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ee0b-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee0b-106">Polecenie cmdlet **Set-AzureRmVMAccessExtension** dodaje rozszerzenie VMAccess maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess) do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="1ee0b-107">Za pomocą rozszerzenia VMAccess można ustawić hasło tymczasowe i należy je natychmiast zmienić po zalogowaniu się do komputera.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="1ee0b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ee0b-108">EXAMPLES</span></span>

### <span data-ttu-id="1ee0b-109">Przykład 1: Dodawanie rozszerzenia VMAccess</span><span class="sxs-lookup"><span data-stu-id="1ee0b-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="1ee0b-110">To polecenie umożliwia dodanie rozszerzenia VMAccess dla maszyny wirtualnej o nazwie VirtualMachine07 w ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="1ee0b-111">To polecenie określa nazwę i typ programu obsługi VMAccess.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="1ee0b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ee0b-112">PARAMETERS</span></span>

### <span data-ttu-id="1ee0b-113">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="1ee0b-113">-Credential</span></span>
<span data-ttu-id="1ee0b-114">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="1ee0b-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="1ee0b-115">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="1ee0b-116">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1ee0b-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee0b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee0b-117">-DefaultProfile</span></span>
<span data-ttu-id="1ee0b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ee0b-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1ee0b-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="1ee0b-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1ee0b-120">-ForceRerun</span></span>
<span data-ttu-id="1ee0b-121">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="1ee0b-122">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="1ee0b-123">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="1ee0b-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1ee0b-124">-Location</span></span>
<span data-ttu-id="1ee0b-125">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="1ee0b-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ee0b-126">-Name</span></span>
<span data-ttu-id="1ee0b-127">Określa nazwę rozszerzenia, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-127">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="1ee0b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ee0b-128">-ResourceGroupName</span></span>
<span data-ttu-id="1ee0b-129">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1ee0b-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1ee0b-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="1ee0b-131">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="1ee0b-132">Aby uzyskać wersję, uruchom polecenie cmdlet Get-AzureRmVMExtensionImage z wartością argumentu Microsoft. COMPUTE dla parametru *wydawcy* i VMAccessAgent dla parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="1ee0b-132">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="1ee0b-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="1ee0b-133">-VMName</span></span>
<span data-ttu-id="1ee0b-134">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1ee0b-135">To polecenie cmdlet umożliwia dodanie VMAccess dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1ee0b-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ee0b-136">-Confirm</span></span>
<span data-ttu-id="1ee0b-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ee0b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ee0b-138">-WhatIf</span></span>
<span data-ttu-id="1ee0b-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1ee0b-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ee0b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee0b-141">CommonParameters</span></span>
<span data-ttu-id="1ee0b-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee0b-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee0b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee0b-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ee0b-144">INPUTS</span></span>

### <span data-ttu-id="1ee0b-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1ee0b-145">None</span></span>
<span data-ttu-id="1ee0b-146">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1ee0b-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ee0b-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ee0b-147">OUTPUTS</span></span>

### <span data-ttu-id="1ee0b-148">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1ee0b-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1ee0b-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ee0b-149">NOTES</span></span>

## <span data-ttu-id="1ee0b-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ee0b-150">RELATED LINKS</span></span>

[<span data-ttu-id="1ee0b-151">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1ee0b-151">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="1ee0b-152">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1ee0b-152">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="1ee0b-153">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="1ee0b-153">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="1ee0b-154">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1ee0b-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


