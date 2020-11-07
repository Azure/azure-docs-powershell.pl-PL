---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 5b590bf882acc373b4219069f8feff4c5060cf59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710207"
---
# <span data-ttu-id="d8c15-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="d8c15-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="d8c15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8c15-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c15-103">Dodaje rozszerzenie domeny usługi AD do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d8c15-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="d8c15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8c15-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8c15-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8c15-105">DESCRIPTION</span></span>
<span data-ttu-id="d8c15-106">Polecenie cmdlet **Set-AzVMADDomainExtension** dodaje rozszerzenie maszyny wirtualnej domeny usługi Azure Active Directory (AD) do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d8c15-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="d8c15-107">To rozszerzenie umożliwia dołączenie maszyny wirtualnej do domeny.</span><span class="sxs-lookup"><span data-stu-id="d8c15-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="d8c15-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8c15-108">EXAMPLES</span></span>

## <span data-ttu-id="d8c15-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8c15-109">PARAMETERS</span></span>

### <span data-ttu-id="d8c15-110">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="d8c15-110">-Credential</span></span>
<span data-ttu-id="d8c15-111">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="d8c15-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="d8c15-112">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="d8c15-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="d8c15-113">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="d8c15-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="d8c15-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c15-114">-DefaultProfile</span></span>
<span data-ttu-id="d8c15-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8c15-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8c15-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d8c15-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d8c15-117">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d8c15-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="d8c15-118">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="d8c15-118">-DomainName</span></span>
<span data-ttu-id="d8c15-119">Określa nazwę domeny.</span><span class="sxs-lookup"><span data-stu-id="d8c15-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="d8c15-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d8c15-120">-ForceRerun</span></span>
<span data-ttu-id="d8c15-121">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="d8c15-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="d8c15-122">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="d8c15-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="d8c15-123">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="d8c15-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="d8c15-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="d8c15-124">-JoinOption</span></span>
<span data-ttu-id="d8c15-125">Określa opcję sprzężenia.</span><span class="sxs-lookup"><span data-stu-id="d8c15-125">Specifies the join option.</span></span> <span data-ttu-id="d8c15-126">Opcje dołączania zobacz [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="d8c15-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="d8c15-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d8c15-127">-Location</span></span>
<span data-ttu-id="d8c15-128">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d8c15-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d8c15-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d8c15-129">-Name</span></span>
<span data-ttu-id="d8c15-130">Określa nazwę rozszerzenia domeny, które należy dodać.</span><span class="sxs-lookup"><span data-stu-id="d8c15-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="d8c15-131">-OUPath</span><span class="sxs-lookup"><span data-stu-id="d8c15-131">-OUPath</span></span>
<span data-ttu-id="d8c15-132">Określa jednostkę organizacyjną (OU) dla konta domeny.</span><span class="sxs-lookup"><span data-stu-id="d8c15-132">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="d8c15-133">Wprowadź pełną nazwę wyróżniającą jednostki organizacyjnej w cudzysłowie.</span><span class="sxs-lookup"><span data-stu-id="d8c15-133">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="d8c15-134">Wartość domyślna to domyślna jednostka organizacyjna dla obiektów komputera w domenie.</span><span class="sxs-lookup"><span data-stu-id="d8c15-134">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="d8c15-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8c15-135">-ResourceGroupName</span></span>
<span data-ttu-id="d8c15-136">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8c15-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d8c15-137">-Restart</span><span class="sxs-lookup"><span data-stu-id="d8c15-137">-Restart</span></span>
<span data-ttu-id="d8c15-138">Wskazuje, że to polecenie cmdlet powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d8c15-138">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="d8c15-139">Ponowne uruchomienie jest często wymagane do wprowadzenia zmiany.</span><span class="sxs-lookup"><span data-stu-id="d8c15-139">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="d8c15-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d8c15-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="d8c15-141">Określa wersję rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="d8c15-141">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="d8c15-142">-VMName</span><span class="sxs-lookup"><span data-stu-id="d8c15-142">-VMName</span></span>
<span data-ttu-id="d8c15-143">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d8c15-143">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="d8c15-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8c15-144">-Confirm</span></span>
<span data-ttu-id="d8c15-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8c15-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8c15-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c15-146">-WhatIf</span></span>
<span data-ttu-id="d8c15-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8c15-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8c15-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d8c15-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8c15-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c15-149">CommonParameters</span></span>
<span data-ttu-id="d8c15-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8c15-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c15-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8c15-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c15-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8c15-152">INPUTS</span></span>

### <span data-ttu-id="d8c15-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d8c15-153">System.String</span></span>

### <span data-ttu-id="d8c15-154">System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d8c15-154">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d8c15-155">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="d8c15-155">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="d8c15-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d8c15-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d8c15-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8c15-157">OUTPUTS</span></span>

### <span data-ttu-id="d8c15-158">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d8c15-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d8c15-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8c15-159">NOTES</span></span>

## <span data-ttu-id="d8c15-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8c15-160">RELATED LINKS</span></span>

[<span data-ttu-id="d8c15-161">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="d8c15-161">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
