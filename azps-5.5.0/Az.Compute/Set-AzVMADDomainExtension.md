---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 1ea90503c1d022aa5a1925fa489e2ee63f4560ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244050"
---
# <span data-ttu-id="baf6e-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="baf6e-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="baf6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baf6e-102">SYNOPSIS</span></span>
<span data-ttu-id="baf6e-103">Dodaje rozszerzenie domeny usługi AD do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baf6e-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="baf6e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="baf6e-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baf6e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="baf6e-105">DESCRIPTION</span></span>
<span data-ttu-id="baf6e-106">Polecenie **cmdlet Set-AzVMADDomainExtension** dodaje do maszyny wirtualnej rozszerzenie domeny usługi Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="baf6e-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="baf6e-107">To rozszerzenie umożliwia twojej maszynie wirtualnej dołączenie do domeny.</span><span class="sxs-lookup"><span data-stu-id="baf6e-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="baf6e-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="baf6e-108">EXAMPLES</span></span>

## <span data-ttu-id="baf6e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baf6e-109">PARAMETERS</span></span>

### <span data-ttu-id="baf6e-110">- Credential</span><span class="sxs-lookup"><span data-stu-id="baf6e-110">-Credential</span></span>
<span data-ttu-id="baf6e-111">Określa nazwę użytkownika i hasło dla maszyny wirtualnej jako **obiekt PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="baf6e-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="baf6e-112">Aby uzyskać poświadczenia, użyj Get-Credential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baf6e-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="baf6e-113">Aby uzyskać więcej informacji, wpisz `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="baf6e-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="baf6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf6e-114">-DefaultProfile</span></span>
<span data-ttu-id="baf6e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="baf6e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baf6e-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="baf6e-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="baf6e-117">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie wersji pomocniczej rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="baf6e-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="baf6e-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="baf6e-118">-DomainName</span></span>
<span data-ttu-id="baf6e-119">Określa nazwę domeny.</span><span class="sxs-lookup"><span data-stu-id="baf6e-119">Specifies the name of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf6e-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="baf6e-120">-ForceRerun</span></span>
<span data-ttu-id="baf6e-121">Wskazuje, że to polecenie cmdlet wymusza ponowne uruchomić tę samą konfigurację rozszerzenia na komputerze wirtualnym bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="baf6e-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="baf6e-122">Wartość może być dowolnym ciągiem innym niż bieżąca wartość.</span><span class="sxs-lookup"><span data-stu-id="baf6e-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="baf6e-123">Jeśli forceUpdateTag nie zostanie zmieniony, program obsługi nadal stosuje aktualizacje ustawień publicznych lub chronionych.</span><span class="sxs-lookup"><span data-stu-id="baf6e-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="baf6e-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="baf6e-124">-JoinOption</span></span>
<span data-ttu-id="baf6e-125">Określa opcję sprzężenia.</span><span class="sxs-lookup"><span data-stu-id="baf6e-125">Specifies the join option.</span></span> <span data-ttu-id="baf6e-126">Aby uzyskać informacje na temat opcji [sprzężenia, zobacz fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="baf6e-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf6e-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="baf6e-127">-Location</span></span>
<span data-ttu-id="baf6e-128">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baf6e-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="baf6e-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="baf6e-129">-Name</span></span>
<span data-ttu-id="baf6e-130">Określa nazwę rozszerzenia domeny do dodania.</span><span class="sxs-lookup"><span data-stu-id="baf6e-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="baf6e-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="baf6e-131">-NoWait</span></span>
<span data-ttu-id="baf6e-132">Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem.</span><span class="sxs-lookup"><span data-stu-id="baf6e-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="baf6e-133">Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="baf6e-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="baf6e-134">— OUPath</span><span class="sxs-lookup"><span data-stu-id="baf6e-134">-OUPath</span></span>
<span data-ttu-id="baf6e-135">Określa jednostkę organizacyjną dla konta domeny.</span><span class="sxs-lookup"><span data-stu-id="baf6e-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="baf6e-136">Wprowadź pełną nazwę wyróżniającą użytkownika systemu operacyjnego w cudzysłowie.</span><span class="sxs-lookup"><span data-stu-id="baf6e-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="baf6e-137">Wartość domyślna to domyślna nazwa użytkownika obiektów komputerowych w domenie.</span><span class="sxs-lookup"><span data-stu-id="baf6e-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="baf6e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf6e-138">-ResourceGroupName</span></span>
<span data-ttu-id="baf6e-139">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="baf6e-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="baf6e-140">— Uruchom ponownie</span><span class="sxs-lookup"><span data-stu-id="baf6e-140">-Restart</span></span>
<span data-ttu-id="baf6e-141">Wskazuje, że to polecenie cmdlet powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baf6e-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="baf6e-142">Aby wprowadzić zmianę w życie, często jest wymagane ponowne uruchomienie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="baf6e-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="baf6e-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="baf6e-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="baf6e-144">Określa wersję rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="baf6e-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="baf6e-145">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="baf6e-145">-VMName</span></span>
<span data-ttu-id="baf6e-146">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="baf6e-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="baf6e-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="baf6e-147">-Confirm</span></span>
<span data-ttu-id="baf6e-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="baf6e-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baf6e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baf6e-149">-WhatIf</span></span>
<span data-ttu-id="baf6e-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baf6e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baf6e-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="baf6e-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baf6e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf6e-152">CommonParameters</span></span>
<span data-ttu-id="baf6e-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baf6e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf6e-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="baf6e-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf6e-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="baf6e-155">INPUTS</span></span>

### <span data-ttu-id="baf6e-156">System.String</span><span class="sxs-lookup"><span data-stu-id="baf6e-156">System.String</span></span>

### <span data-ttu-id="baf6e-157">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="baf6e-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="baf6e-158">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="baf6e-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="baf6e-159">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="baf6e-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="baf6e-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="baf6e-160">OUTPUTS</span></span>

### <span data-ttu-id="baf6e-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="baf6e-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="baf6e-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="baf6e-162">NOTES</span></span>

## <span data-ttu-id="baf6e-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="baf6e-163">RELATED LINKS</span></span>

[<span data-ttu-id="baf6e-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="baf6e-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
