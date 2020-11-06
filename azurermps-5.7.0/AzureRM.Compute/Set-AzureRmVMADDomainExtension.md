---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: b0af0f205f26862c20dd50e6181d2c11cd050dd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525277"
---
# <span data-ttu-id="b3150-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b3150-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="b3150-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3150-102">SYNOPSIS</span></span>
<span data-ttu-id="b3150-103">Dodaje rozszerzenie domeny usługi AD do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b3150-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3150-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3150-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3150-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b3150-105">DESCRIPTION</span></span>
<span data-ttu-id="b3150-106">Polecenie cmdlet **Set-AzureRmVMADDomainExtension** dodaje rozszerzenie maszyny wirtualnej domeny usługi Azure Active Directory (AD) do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b3150-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="b3150-107">To rozszerzenie umożliwia dołączenie maszyny wirtualnej do domeny.</span><span class="sxs-lookup"><span data-stu-id="b3150-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="b3150-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3150-108">EXAMPLES</span></span>

## <span data-ttu-id="b3150-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3150-109">PARAMETERS</span></span>

### <span data-ttu-id="b3150-110">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="b3150-110">-Credential</span></span>
<span data-ttu-id="b3150-111">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="b3150-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="b3150-112">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="b3150-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="b3150-113">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b3150-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="b3150-114">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b3150-114">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b3150-115">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b3150-115">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="b3150-116">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="b3150-116">-DomainName</span></span>
<span data-ttu-id="b3150-117">Określa nazwę domeny.</span><span class="sxs-lookup"><span data-stu-id="b3150-117">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="b3150-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="b3150-118">-ForceRerun</span></span>
<span data-ttu-id="b3150-119">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b3150-119">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="b3150-120">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="b3150-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="b3150-121">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="b3150-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="b3150-122">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="b3150-122">-JoinOption</span></span>
<span data-ttu-id="b3150-123">Określa opcję sprzężenia.</span><span class="sxs-lookup"><span data-stu-id="b3150-123">Specifies the join option.</span></span>

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

### <span data-ttu-id="b3150-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b3150-124">-Location</span></span>
<span data-ttu-id="b3150-125">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b3150-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="b3150-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3150-126">-Name</span></span>
<span data-ttu-id="b3150-127">Określa nazwę rozszerzenia domeny, które należy dodać.</span><span class="sxs-lookup"><span data-stu-id="b3150-127">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="b3150-128">-OUPath</span><span class="sxs-lookup"><span data-stu-id="b3150-128">-OUPath</span></span>
<span data-ttu-id="b3150-129">Określa jednostkę organizacyjną (OU) dla konta domeny.</span><span class="sxs-lookup"><span data-stu-id="b3150-129">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="b3150-130">Wprowadź pełną nazwę wyróżniającą jednostki organizacyjnej w cudzysłowie.</span><span class="sxs-lookup"><span data-stu-id="b3150-130">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="b3150-131">Wartość domyślna to domyślna jednostka organizacyjna dla obiektów komputera w domenie.</span><span class="sxs-lookup"><span data-stu-id="b3150-131">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="b3150-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3150-132">-ResourceGroupName</span></span>
<span data-ttu-id="b3150-133">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b3150-133">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b3150-134">-Restart</span><span class="sxs-lookup"><span data-stu-id="b3150-134">-Restart</span></span>
<span data-ttu-id="b3150-135">Wskazuje, że to polecenie cmdlet powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b3150-135">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="b3150-136">Ponowne uruchomienie jest często wymagane do wprowadzenia zmiany.</span><span class="sxs-lookup"><span data-stu-id="b3150-136">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="b3150-137">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b3150-137">-TypeHandlerVersion</span></span>
<span data-ttu-id="b3150-138">Określa wersję rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="b3150-138">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="b3150-139">-VMName</span><span class="sxs-lookup"><span data-stu-id="b3150-139">-VMName</span></span>
<span data-ttu-id="b3150-140">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b3150-140">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="b3150-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3150-141">-Confirm</span></span>
<span data-ttu-id="b3150-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3150-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3150-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3150-143">-WhatIf</span></span>
<span data-ttu-id="b3150-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3150-144">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b3150-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3150-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3150-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3150-146">CommonParameters</span></span>
<span data-ttu-id="b3150-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3150-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3150-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3150-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3150-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3150-149">INPUTS</span></span>

### <span data-ttu-id="b3150-150">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b3150-150">None</span></span>
<span data-ttu-id="b3150-151">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b3150-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b3150-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3150-152">OUTPUTS</span></span>

## <span data-ttu-id="b3150-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3150-153">NOTES</span></span>

## <span data-ttu-id="b3150-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3150-154">RELATED LINKS</span></span>

[<span data-ttu-id="b3150-155">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b3150-155">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
