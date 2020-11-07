---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0b91e2892f087da6eb510d087980e6f31dd67ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710204"
---
# <span data-ttu-id="aea3f-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="aea3f-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="aea3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aea3f-102">SYNOPSIS</span></span>
<span data-ttu-id="aea3f-103">Dodaje rozszerzenie VMAccess do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aea3f-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="aea3f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aea3f-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aea3f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aea3f-105">DESCRIPTION</span></span>
<span data-ttu-id="aea3f-106">Polecenie cmdlet **Set-AzVMAccessExtension** dodaje rozszerzenie VMAccess maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess) do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aea3f-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="aea3f-107">Za pomocą rozszerzenia VMAccess można ustawić hasło tymczasowe i należy je natychmiast zmienić po zalogowaniu się do komputera.</span><span class="sxs-lookup"><span data-stu-id="aea3f-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="aea3f-108">Nie jest to obsługiwane na kontrolerach domeny systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="aea3f-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="aea3f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aea3f-109">EXAMPLES</span></span>

### <span data-ttu-id="aea3f-110">Przykład 1: Dodawanie rozszerzenia VMAccess</span><span class="sxs-lookup"><span data-stu-id="aea3f-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="aea3f-111">To polecenie umożliwia dodanie rozszerzenia VMAccess dla maszyny wirtualnej o nazwie VirtualMachine07 w ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="aea3f-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="aea3f-112">To polecenie określa nazwę i typ programu obsługi VMAccess.</span><span class="sxs-lookup"><span data-stu-id="aea3f-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="aea3f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aea3f-113">PARAMETERS</span></span>

### <span data-ttu-id="aea3f-114">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="aea3f-114">-Credential</span></span>
<span data-ttu-id="aea3f-115">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="aea3f-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="aea3f-116">Jeśli wpiszesz inną nazwę niż bieżące konto administratora lokalnego na maszynie wirtualnej, rozszerzenie VMAccess doda konto administratora lokalnego z tą nazwą i przypiszesz określone hasło do tego konta.</span><span class="sxs-lookup"><span data-stu-id="aea3f-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="aea3f-117">Jeśli konto administratora lokalnego na maszynie wirtualnej już istnieje, hasło zostanie zresetowane i jeśli konto jest wyłączone, rozszerzenie VMAccess włącza je.</span><span class="sxs-lookup"><span data-stu-id="aea3f-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="aea3f-118">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="aea3f-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="aea3f-119">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="aea3f-119">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="aea3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea3f-120">-DefaultProfile</span></span>
<span data-ttu-id="aea3f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aea3f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aea3f-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="aea3f-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="aea3f-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="aea3f-123">-ForceRerun</span></span>
<span data-ttu-id="aea3f-124">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="aea3f-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="aea3f-125">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="aea3f-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="aea3f-126">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="aea3f-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="aea3f-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="aea3f-127">-Location</span></span>
<span data-ttu-id="aea3f-128">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aea3f-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="aea3f-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aea3f-129">-Name</span></span>
<span data-ttu-id="aea3f-130">Określa nazwę rozszerzenia, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aea3f-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="aea3f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea3f-131">-ResourceGroupName</span></span>
<span data-ttu-id="aea3f-132">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aea3f-132">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="aea3f-133">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="aea3f-133">-TypeHandlerVersion</span></span>
<span data-ttu-id="aea3f-134">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aea3f-134">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="aea3f-135">Aby uzyskać wersję, uruchom polecenie cmdlet Get-AzVMExtensionImage z wartością argumentu Microsoft. COMPUTE dla parametru *wydawcy* i VMAccessAgent dla parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="aea3f-135">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="aea3f-136">TypeHandlerVersion musi być równy 2,0 lub większy, ponieważ wersja 1 jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="aea3f-136">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="aea3f-137">-VMName</span><span class="sxs-lookup"><span data-stu-id="aea3f-137">-VMName</span></span>
<span data-ttu-id="aea3f-138">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="aea3f-138">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="aea3f-139">To polecenie cmdlet umożliwia dodanie VMAccess dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="aea3f-139">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="aea3f-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aea3f-140">-Confirm</span></span>
<span data-ttu-id="aea3f-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aea3f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aea3f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aea3f-142">-WhatIf</span></span>
<span data-ttu-id="aea3f-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aea3f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aea3f-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aea3f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aea3f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea3f-145">CommonParameters</span></span>
<span data-ttu-id="aea3f-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea3f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea3f-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea3f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea3f-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aea3f-148">INPUTS</span></span>

### <span data-ttu-id="aea3f-149">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="aea3f-149">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="aea3f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="aea3f-150">System.String</span></span>

### <span data-ttu-id="aea3f-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aea3f-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aea3f-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aea3f-152">OUTPUTS</span></span>

### <span data-ttu-id="aea3f-153">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="aea3f-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="aea3f-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aea3f-154">NOTES</span></span>

## <span data-ttu-id="aea3f-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aea3f-155">RELATED LINKS</span></span>

[<span data-ttu-id="aea3f-156">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="aea3f-156">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="aea3f-157">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="aea3f-157">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="aea3f-158">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="aea3f-158">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="aea3f-159">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="aea3f-159">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


