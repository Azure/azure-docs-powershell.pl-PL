---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: fed235e3c628ab245ae74299cf395e4501b141f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706199"
---
# <span data-ttu-id="f0e0b-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f0e0b-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="f0e0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e0b-103">Dodaje rozszerzenie domeny usługi AD do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="f0e0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0e0b-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0e0b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f0e0b-105">DESCRIPTION</span></span>
<span data-ttu-id="f0e0b-106">Polecenie cmdlet **Set-AzVMADDomainExtension** dodaje rozszerzenie maszyny wirtualnej domeny usługi Azure Active Directory (AD) do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="f0e0b-107">To rozszerzenie umożliwia dołączenie maszyny wirtualnej do domeny.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="f0e0b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0e0b-108">EXAMPLES</span></span>

## <span data-ttu-id="f0e0b-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0e0b-109">PARAMETERS</span></span>

### <span data-ttu-id="f0e0b-110">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="f0e0b-110">-Credential</span></span>
<span data-ttu-id="f0e0b-111">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="f0e0b-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="f0e0b-112">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="f0e0b-113">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="f0e0b-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="f0e0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e0b-114">-DefaultProfile</span></span>
<span data-ttu-id="f0e0b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0e0b-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f0e0b-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f0e0b-117">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="f0e0b-118">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="f0e0b-118">-DomainName</span></span>
<span data-ttu-id="f0e0b-119">Określa nazwę domeny.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="f0e0b-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f0e0b-120">-ForceRerun</span></span>
<span data-ttu-id="f0e0b-121">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="f0e0b-122">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="f0e0b-123">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="f0e0b-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="f0e0b-124">-JoinOption</span></span>
<span data-ttu-id="f0e0b-125">Określa opcję sprzężenia.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-125">Specifies the join option.</span></span> <span data-ttu-id="f0e0b-126">Opcje dołączania zobacz [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="f0e0b-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="f0e0b-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f0e0b-127">-Location</span></span>
<span data-ttu-id="f0e0b-128">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="f0e0b-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f0e0b-129">-Name</span></span>
<span data-ttu-id="f0e0b-130">Określa nazwę rozszerzenia domeny, które należy dodać.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="f0e0b-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f0e0b-131">-NoWait</span></span>
<span data-ttu-id="f0e0b-132">Rozpoczyna operację i wraca natychmiast, zanim operacja zostanie ukończona.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f0e0b-133">W celu ustalenia, czy operacja została wykonana pomyślnie, użyj innego mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f0e0b-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="f0e0b-134">-OUPath</span></span>
<span data-ttu-id="f0e0b-135">Określa jednostkę organizacyjną (OU) dla konta domeny.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="f0e0b-136">Wprowadź pełną nazwę wyróżniającą jednostki organizacyjnej w cudzysłowie.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="f0e0b-137">Wartość domyślna to domyślna jednostka organizacyjna dla obiektów komputera w domenie.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="f0e0b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0e0b-138">-ResourceGroupName</span></span>
<span data-ttu-id="f0e0b-139">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f0e0b-140">-Restart</span><span class="sxs-lookup"><span data-stu-id="f0e0b-140">-Restart</span></span>
<span data-ttu-id="f0e0b-141">Wskazuje, że to polecenie cmdlet powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="f0e0b-142">Ponowne uruchomienie jest często wymagane do wprowadzenia zmiany.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="f0e0b-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f0e0b-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="f0e0b-144">Określa wersję rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="f0e0b-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="f0e0b-145">-VMName</span></span>
<span data-ttu-id="f0e0b-146">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="f0e0b-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0e0b-147">-Confirm</span></span>
<span data-ttu-id="f0e0b-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0e0b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0e0b-149">-WhatIf</span></span>
<span data-ttu-id="f0e0b-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0e0b-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0e0b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e0b-152">CommonParameters</span></span>
<span data-ttu-id="f0e0b-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0e0b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e0b-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0e0b-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e0b-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0e0b-155">INPUTS</span></span>

### <span data-ttu-id="f0e0b-156">System. String</span><span class="sxs-lookup"><span data-stu-id="f0e0b-156">System.String</span></span>

### <span data-ttu-id="f0e0b-157">System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f0e0b-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f0e0b-158">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="f0e0b-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="f0e0b-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f0e0b-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f0e0b-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0e0b-160">OUTPUTS</span></span>

### <span data-ttu-id="f0e0b-161">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f0e0b-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f0e0b-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0e0b-162">NOTES</span></span>

## <span data-ttu-id="f0e0b-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0e0b-163">RELATED LINKS</span></span>

[<span data-ttu-id="f0e0b-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f0e0b-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)