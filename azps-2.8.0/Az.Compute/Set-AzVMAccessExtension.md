---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: 8737801a798ac9d954d657db23f2500df028fa06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706197"
---
# <span data-ttu-id="eaca4-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="eaca4-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="eaca4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eaca4-102">SYNOPSIS</span></span>
<span data-ttu-id="eaca4-103">Dodaje rozszerzenie VMAccess do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eaca4-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="eaca4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eaca4-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eaca4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eaca4-105">DESCRIPTION</span></span>
<span data-ttu-id="eaca4-106">Polecenie cmdlet **Set-AzVMAccessExtension** dodaje rozszerzenie VMAccess maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess) do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eaca4-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="eaca4-107">Za pomocą rozszerzenia VMAccess można ustawić hasło tymczasowe i należy je natychmiast zmienić po zalogowaniu się do komputera.</span><span class="sxs-lookup"><span data-stu-id="eaca4-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="eaca4-108">Nie jest to obsługiwane na kontrolerach domeny systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="eaca4-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="eaca4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eaca4-109">EXAMPLES</span></span>

### <span data-ttu-id="eaca4-110">Przykład 1: Dodawanie rozszerzenia VMAccess</span><span class="sxs-lookup"><span data-stu-id="eaca4-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="eaca4-111">To polecenie umożliwia dodanie rozszerzenia VMAccess dla maszyny wirtualnej o nazwie VirtualMachine07 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="eaca4-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>
<span data-ttu-id="eaca4-112">To polecenie określa nazwę i typ programu obsługi VMAccess.</span><span class="sxs-lookup"><span data-stu-id="eaca4-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="eaca4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eaca4-113">PARAMETERS</span></span>

### <span data-ttu-id="eaca4-114">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="eaca4-114">-Credential</span></span>
<span data-ttu-id="eaca4-115">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="eaca4-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="eaca4-116">Jeśli wpiszesz inną nazwę niż bieżące konto administratora lokalnego na maszynie wirtualnej, rozszerzenie VMAccess doda konto administratora lokalnego z tą nazwą i przypiszesz określone hasło do tego konta.</span><span class="sxs-lookup"><span data-stu-id="eaca4-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="eaca4-117">Jeśli konto administratora lokalnego na maszynie wirtualnej już istnieje, hasło zostanie zresetowane i jeśli konto jest wyłączone, rozszerzenie VMAccess włącza je.</span><span class="sxs-lookup"><span data-stu-id="eaca4-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="eaca4-118">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="eaca4-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="eaca4-119">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="eaca4-119">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="eaca4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaca4-120">-DefaultProfile</span></span>
<span data-ttu-id="eaca4-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eaca4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaca4-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="eaca4-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="eaca4-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="eaca4-123">-ForceRerun</span></span>
<span data-ttu-id="eaca4-124">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="eaca4-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="eaca4-125">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="eaca4-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="eaca4-126">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="eaca4-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="eaca4-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="eaca4-127">-Location</span></span>
<span data-ttu-id="eaca4-128">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eaca4-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="eaca4-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eaca4-129">-Name</span></span>
<span data-ttu-id="eaca4-130">Określa nazwę rozszerzenia, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaca4-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="eaca4-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="eaca4-131">-NoWait</span></span>
<span data-ttu-id="eaca4-132">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="eaca4-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="eaca4-133">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="eaca4-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="eaca4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaca4-134">-ResourceGroupName</span></span>
<span data-ttu-id="eaca4-135">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eaca4-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="eaca4-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="eaca4-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="eaca4-137">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eaca4-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="eaca4-138">Aby uzyskać wersję, uruchom polecenie cmdlet Get-AzVMExtensionImage z wartością argumentu Microsoft. COMPUTE dla parametru *wydawcy* i VMAccessAgent dla parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="eaca4-138">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="eaca4-139">TypeHandlerVersion musi być równy 2,0 lub większy, ponieważ wersja 1 jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="eaca4-139">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="eaca4-140">-VMName</span><span class="sxs-lookup"><span data-stu-id="eaca4-140">-VMName</span></span>
<span data-ttu-id="eaca4-141">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eaca4-141">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="eaca4-142">To polecenie cmdlet umożliwia dodanie VMAccess dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="eaca4-142">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="eaca4-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eaca4-143">-Confirm</span></span>
<span data-ttu-id="eaca4-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaca4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaca4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaca4-145">-WhatIf</span></span>
<span data-ttu-id="eaca4-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaca4-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaca4-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eaca4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaca4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaca4-148">CommonParameters</span></span>
<span data-ttu-id="eaca4-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaca4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaca4-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eaca4-150">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaca4-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eaca4-151">INPUTS</span></span>

### <span data-ttu-id="eaca4-152">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="eaca4-152">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="eaca4-153">System. String</span><span class="sxs-lookup"><span data-stu-id="eaca4-153">System.String</span></span>

### <span data-ttu-id="eaca4-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eaca4-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eaca4-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eaca4-155">OUTPUTS</span></span>

### <span data-ttu-id="eaca4-156">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eaca4-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="eaca4-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eaca4-157">NOTES</span></span>

## <span data-ttu-id="eaca4-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eaca4-158">RELATED LINKS</span></span>

[<span data-ttu-id="eaca4-159">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="eaca4-159">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="eaca4-160">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="eaca4-160">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="eaca4-161">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="eaca4-161">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="eaca4-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="eaca4-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

