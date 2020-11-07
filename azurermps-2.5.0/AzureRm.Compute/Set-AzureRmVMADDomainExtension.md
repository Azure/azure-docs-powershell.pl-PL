---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaddomainextension
schema: 2.0.0
ms.openlocfilehash: 140f1ccdedd6f3b3402601a8a844092bf3d7ab0e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899139"
---
# <span data-ttu-id="dddb3-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="dddb3-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="dddb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dddb3-102">SYNOPSIS</span></span>
<span data-ttu-id="dddb3-103">Dodaje rozszerzenie domeny usługi AD do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dddb3-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dddb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dddb3-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dddb3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dddb3-105">DESCRIPTION</span></span>
<span data-ttu-id="dddb3-106">Polecenie cmdlet **Set-AzureRmVMADDomainExtension** dodaje rozszerzenie maszyny wirtualnej domeny usługi Azure Active Directory (AD) do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dddb3-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="dddb3-107">To rozszerzenie umożliwia dołączenie maszyny wirtualnej do domeny.</span><span class="sxs-lookup"><span data-stu-id="dddb3-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="dddb3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dddb3-108">EXAMPLES</span></span>

## <span data-ttu-id="dddb3-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dddb3-109">PARAMETERS</span></span>

### <span data-ttu-id="dddb3-110">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="dddb3-110">-Credential</span></span>
<span data-ttu-id="dddb3-111">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="dddb3-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="dddb3-112">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="dddb3-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="dddb3-113">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="dddb3-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="dddb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dddb3-114">-DefaultProfile</span></span>
<span data-ttu-id="dddb3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dddb3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dddb3-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="dddb3-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="dddb3-117">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="dddb3-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="dddb3-118">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="dddb3-118">-DomainName</span></span>
<span data-ttu-id="dddb3-119">Określa nazwę domeny.</span><span class="sxs-lookup"><span data-stu-id="dddb3-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="dddb3-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="dddb3-120">-ForceRerun</span></span>
<span data-ttu-id="dddb3-121">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="dddb3-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="dddb3-122">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="dddb3-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="dddb3-123">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="dddb3-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="dddb3-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="dddb3-124">-JoinOption</span></span>
<span data-ttu-id="dddb3-125">Określa opcję sprzężenia.</span><span class="sxs-lookup"><span data-stu-id="dddb3-125">Specifies the join option.</span></span>

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

### <span data-ttu-id="dddb3-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dddb3-126">-Location</span></span>
<span data-ttu-id="dddb3-127">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dddb3-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="dddb3-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dddb3-128">-Name</span></span>
<span data-ttu-id="dddb3-129">Określa nazwę rozszerzenia domeny, które należy dodać.</span><span class="sxs-lookup"><span data-stu-id="dddb3-129">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="dddb3-130">-OUPath</span><span class="sxs-lookup"><span data-stu-id="dddb3-130">-OUPath</span></span>
<span data-ttu-id="dddb3-131">Określa jednostkę organizacyjną (OU) dla konta domeny.</span><span class="sxs-lookup"><span data-stu-id="dddb3-131">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="dddb3-132">Wprowadź pełną nazwę wyróżniającą jednostki organizacyjnej w cudzysłowie.</span><span class="sxs-lookup"><span data-stu-id="dddb3-132">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="dddb3-133">Wartość domyślna to domyślna jednostka organizacyjna dla obiektów komputera w domenie.</span><span class="sxs-lookup"><span data-stu-id="dddb3-133">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="dddb3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dddb3-134">-ResourceGroupName</span></span>
<span data-ttu-id="dddb3-135">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dddb3-135">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="dddb3-136">-Restart</span><span class="sxs-lookup"><span data-stu-id="dddb3-136">-Restart</span></span>
<span data-ttu-id="dddb3-137">Wskazuje, że to polecenie cmdlet powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dddb3-137">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="dddb3-138">Ponowne uruchomienie jest często wymagane do wprowadzenia zmiany.</span><span class="sxs-lookup"><span data-stu-id="dddb3-138">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="dddb3-139">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="dddb3-139">-TypeHandlerVersion</span></span>
<span data-ttu-id="dddb3-140">Określa wersję rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="dddb3-140">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="dddb3-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="dddb3-141">-VMName</span></span>
<span data-ttu-id="dddb3-142">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dddb3-142">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="dddb3-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dddb3-143">-Confirm</span></span>
<span data-ttu-id="dddb3-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dddb3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dddb3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dddb3-145">-WhatIf</span></span>
<span data-ttu-id="dddb3-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dddb3-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="dddb3-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dddb3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dddb3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dddb3-148">CommonParameters</span></span>
<span data-ttu-id="dddb3-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dddb3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dddb3-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dddb3-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dddb3-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dddb3-151">INPUTS</span></span>

### <span data-ttu-id="dddb3-152">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dddb3-152">None</span></span>
<span data-ttu-id="dddb3-153">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="dddb3-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dddb3-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dddb3-154">OUTPUTS</span></span>

### <span data-ttu-id="dddb3-155">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="dddb3-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="dddb3-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dddb3-156">NOTES</span></span>

## <span data-ttu-id="dddb3-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dddb3-157">RELATED LINKS</span></span>

[<span data-ttu-id="dddb3-158">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="dddb3-158">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
