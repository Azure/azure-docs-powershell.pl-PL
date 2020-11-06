---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: 0a2d3ce354a5039db21fdd336f6f2d64efdb56fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553607"
---
# <span data-ttu-id="d5d61-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d5d61-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="d5d61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5d61-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d61-103">Dodaje rozszerzenie VMAccess do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d5d61-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5d61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5d61-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5d61-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5d61-105">DESCRIPTION</span></span>
<span data-ttu-id="d5d61-106">Polecenie cmdlet **Set-AzureRmVMAccessExtension** dodaje rozszerzenie VMAccess maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess) do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d5d61-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="d5d61-107">Za pomocą rozszerzenia VMAccess można ustawić hasło tymczasowe i należy je natychmiast zmienić po zalogowaniu się do komputera.</span><span class="sxs-lookup"><span data-stu-id="d5d61-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="d5d61-108">Nie jest to obsługiwane na kontrolerach domeny systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="d5d61-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="d5d61-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5d61-109">EXAMPLES</span></span>

### <span data-ttu-id="d5d61-110">Przykład 1: Dodawanie rozszerzenia VMAccess</span><span class="sxs-lookup"><span data-stu-id="d5d61-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="d5d61-111">To polecenie umożliwia dodanie rozszerzenia VMAccess dla maszyny wirtualnej o nazwie VirtualMachine07 w ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d5d61-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="d5d61-112">To polecenie określa nazwę i typ programu obsługi VMAccess.</span><span class="sxs-lookup"><span data-stu-id="d5d61-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="d5d61-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5d61-113">PARAMETERS</span></span>

### <span data-ttu-id="d5d61-114">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="d5d61-114">-Credential</span></span>
<span data-ttu-id="d5d61-115">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="d5d61-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="d5d61-116">Jeśli wpiszesz inną nazwę niż bieżące konto administratora lokalnego na maszynie wirtualnej, rozszerzenie VMAccess doda konto administratora lokalnego z tą nazwą i przypiszesz określone hasło do tego konta.</span><span class="sxs-lookup"><span data-stu-id="d5d61-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="d5d61-117">Jeśli konto administratora lokalnego na maszynie wirtualnej już istnieje, hasło zostanie zresetowane i jeśli konto jest wyłączone, rozszerzenie VMAccess włącza je.</span><span class="sxs-lookup"><span data-stu-id="d5d61-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="d5d61-118">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="d5d61-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="d5d61-119">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="d5d61-119">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d61-120">-DefaultProfile</span></span>
<span data-ttu-id="d5d61-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d61-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5d61-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d5d61-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="d5d61-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d5d61-123">-ForceRerun</span></span>
<span data-ttu-id="d5d61-124">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d5d61-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="d5d61-125">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="d5d61-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="d5d61-126">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="d5d61-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="d5d61-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d5d61-127">-Location</span></span>
<span data-ttu-id="d5d61-128">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d5d61-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d5d61-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d5d61-129">-Name</span></span>
<span data-ttu-id="d5d61-130">Określa nazwę rozszerzenia, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5d61-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="d5d61-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d61-131">-ResourceGroupName</span></span>
<span data-ttu-id="d5d61-132">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d5d61-132">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d5d61-133">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d5d61-133">-TypeHandlerVersion</span></span>
<span data-ttu-id="d5d61-134">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d5d61-134">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="d5d61-135">Aby uzyskać wersję, uruchom polecenie cmdlet Get-AzureRmVMExtensionImage z wartością argumentu Microsoft. COMPUTE dla parametru *wydawcy* i VMAccessAgent dla parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="d5d61-135">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="d5d61-136">TypeHandlerVersion musi być równy 2,0 lub większy, ponieważ wersja 1 jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="d5d61-136">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="d5d61-137">-VMName</span><span class="sxs-lookup"><span data-stu-id="d5d61-137">-VMName</span></span>
<span data-ttu-id="d5d61-138">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d5d61-138">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d5d61-139">To polecenie cmdlet umożliwia dodanie VMAccess dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d5d61-139">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d5d61-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d5d61-140">-Confirm</span></span>
<span data-ttu-id="d5d61-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5d61-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5d61-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5d61-142">-WhatIf</span></span>
<span data-ttu-id="d5d61-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5d61-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5d61-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d5d61-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5d61-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d61-145">CommonParameters</span></span>
<span data-ttu-id="d5d61-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5d61-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d61-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5d61-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d61-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5d61-148">INPUTS</span></span>

### <span data-ttu-id="d5d61-149">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="d5d61-149">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="d5d61-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d5d61-150">System.String</span></span>

### <span data-ttu-id="d5d61-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d5d61-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d5d61-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5d61-152">OUTPUTS</span></span>

### <span data-ttu-id="d5d61-153">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d5d61-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d5d61-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5d61-154">NOTES</span></span>

## <span data-ttu-id="d5d61-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5d61-155">RELATED LINKS</span></span>

[<span data-ttu-id="d5d61-156">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d5d61-156">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="d5d61-157">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d5d61-157">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="d5d61-158">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="d5d61-158">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="d5d61-159">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="d5d61-159">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


