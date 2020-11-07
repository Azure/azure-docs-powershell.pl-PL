---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 99dd311adf976e100282da92db6a3147880feefb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893406"
---
# <span data-ttu-id="0210c-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0210c-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="0210c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0210c-102">SYNOPSIS</span></span>
<span data-ttu-id="0210c-103">Dodaje rozszerzenie domeny usługi AD do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0210c-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="0210c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0210c-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0210c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0210c-105">DESCRIPTION</span></span>
<span data-ttu-id="0210c-106">Polecenie cmdlet **Set-AzVMADDomainExtension** dodaje rozszerzenie maszyny wirtualnej domeny usługi Azure Active Directory (AD) do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0210c-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="0210c-107">To rozszerzenie umożliwia dołączenie maszyny wirtualnej do domeny.</span><span class="sxs-lookup"><span data-stu-id="0210c-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="0210c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0210c-108">EXAMPLES</span></span>

## <span data-ttu-id="0210c-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0210c-109">PARAMETERS</span></span>

### <span data-ttu-id="0210c-110">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="0210c-110">-Credential</span></span>
<span data-ttu-id="0210c-111">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="0210c-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="0210c-112">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="0210c-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="0210c-113">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="0210c-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="0210c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0210c-114">-DefaultProfile</span></span>
<span data-ttu-id="0210c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0210c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0210c-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0210c-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0210c-117">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0210c-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="0210c-118">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="0210c-118">-DomainName</span></span>
<span data-ttu-id="0210c-119">Określa nazwę domeny.</span><span class="sxs-lookup"><span data-stu-id="0210c-119">Specifies the name of the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0210c-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="0210c-120">-ForceRerun</span></span>
<span data-ttu-id="0210c-121">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="0210c-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="0210c-122">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="0210c-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="0210c-123">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="0210c-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="0210c-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="0210c-124">-JoinOption</span></span>
<span data-ttu-id="0210c-125">Określa opcję sprzężenia.</span><span class="sxs-lookup"><span data-stu-id="0210c-125">Specifies the join option.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0210c-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0210c-126">-Location</span></span>
<span data-ttu-id="0210c-127">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0210c-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="0210c-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0210c-128">-Name</span></span>
<span data-ttu-id="0210c-129">Określa nazwę rozszerzenia domeny, które należy dodać.</span><span class="sxs-lookup"><span data-stu-id="0210c-129">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="0210c-130">-OUPath</span><span class="sxs-lookup"><span data-stu-id="0210c-130">-OUPath</span></span>
<span data-ttu-id="0210c-131">Określa jednostkę organizacyjną (OU) dla konta domeny.</span><span class="sxs-lookup"><span data-stu-id="0210c-131">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="0210c-132">Wprowadź pełną nazwę wyróżniającą jednostki organizacyjnej w cudzysłowie.</span><span class="sxs-lookup"><span data-stu-id="0210c-132">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="0210c-133">Wartość domyślna to domyślna jednostka organizacyjna dla obiektów komputera w domenie.</span><span class="sxs-lookup"><span data-stu-id="0210c-133">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="0210c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0210c-134">-ResourceGroupName</span></span>
<span data-ttu-id="0210c-135">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0210c-135">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0210c-136">-Restart</span><span class="sxs-lookup"><span data-stu-id="0210c-136">-Restart</span></span>
<span data-ttu-id="0210c-137">Wskazuje, że to polecenie cmdlet powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0210c-137">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="0210c-138">Ponowne uruchomienie jest często wymagane do wprowadzenia zmiany.</span><span class="sxs-lookup"><span data-stu-id="0210c-138">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="0210c-139">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0210c-139">-TypeHandlerVersion</span></span>
<span data-ttu-id="0210c-140">Określa wersję rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="0210c-140">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="0210c-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="0210c-141">-VMName</span></span>
<span data-ttu-id="0210c-142">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0210c-142">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0210c-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0210c-143">-Confirm</span></span>
<span data-ttu-id="0210c-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0210c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0210c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0210c-145">-WhatIf</span></span>
<span data-ttu-id="0210c-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0210c-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0210c-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0210c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0210c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0210c-148">CommonParameters</span></span>
<span data-ttu-id="0210c-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0210c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0210c-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0210c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0210c-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0210c-151">INPUTS</span></span>

### <span data-ttu-id="0210c-152">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0210c-152">None</span></span>
<span data-ttu-id="0210c-153">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0210c-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0210c-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0210c-154">OUTPUTS</span></span>

### <span data-ttu-id="0210c-155">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0210c-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0210c-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0210c-156">NOTES</span></span>

## <span data-ttu-id="0210c-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0210c-157">RELATED LINKS</span></span>

[<span data-ttu-id="0210c-158">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0210c-158">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
