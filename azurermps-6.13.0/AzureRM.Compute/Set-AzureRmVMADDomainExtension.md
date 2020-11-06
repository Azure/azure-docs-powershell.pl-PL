---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e0d36e8ddc239d1d075b79e0c91df645d671c6a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553615"
---
# <span data-ttu-id="8aa9f-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="8aa9f-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="8aa9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8aa9f-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa9f-103">Dodaje rozszerzenie domeny usługi AD do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8aa9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8aa9f-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aa9f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8aa9f-105">DESCRIPTION</span></span>
<span data-ttu-id="8aa9f-106">Polecenie cmdlet **Set-AzureRmVMADDomainExtension** dodaje rozszerzenie maszyny wirtualnej domeny usługi Azure Active Directory (AD) do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="8aa9f-107">To rozszerzenie umożliwia dołączenie maszyny wirtualnej do domeny.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="8aa9f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8aa9f-108">EXAMPLES</span></span>

## <span data-ttu-id="8aa9f-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8aa9f-109">PARAMETERS</span></span>

### <span data-ttu-id="8aa9f-110">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="8aa9f-110">-Credential</span></span>
<span data-ttu-id="8aa9f-111">Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="8aa9f-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="8aa9f-112">Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="8aa9f-113">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="8aa9f-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="8aa9f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa9f-114">-DefaultProfile</span></span>
<span data-ttu-id="8aa9f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8aa9f-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8aa9f-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8aa9f-117">Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="8aa9f-118">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="8aa9f-118">-DomainName</span></span>
<span data-ttu-id="8aa9f-119">Określa nazwę domeny.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="8aa9f-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="8aa9f-120">-ForceRerun</span></span>
<span data-ttu-id="8aa9f-121">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="8aa9f-122">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="8aa9f-123">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="8aa9f-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="8aa9f-124">-JoinOption</span></span>
<span data-ttu-id="8aa9f-125">Określa opcję sprzężenia.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-125">Specifies the join option.</span></span> <span data-ttu-id="8aa9f-126">Opcje dołączania zobacz [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="8aa9f-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="8aa9f-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8aa9f-127">-Location</span></span>
<span data-ttu-id="8aa9f-128">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="8aa9f-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8aa9f-129">-Name</span></span>
<span data-ttu-id="8aa9f-130">Określa nazwę rozszerzenia domeny, które należy dodać.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="8aa9f-131">-OUPath</span><span class="sxs-lookup"><span data-stu-id="8aa9f-131">-OUPath</span></span>
<span data-ttu-id="8aa9f-132">Określa jednostkę organizacyjną (OU) dla konta domeny.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-132">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="8aa9f-133">Wprowadź pełną nazwę wyróżniającą jednostki organizacyjnej w cudzysłowie.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-133">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="8aa9f-134">Wartość domyślna to domyślna jednostka organizacyjna dla obiektów komputera w domenie.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-134">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="8aa9f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aa9f-135">-ResourceGroupName</span></span>
<span data-ttu-id="8aa9f-136">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8aa9f-137">-Restart</span><span class="sxs-lookup"><span data-stu-id="8aa9f-137">-Restart</span></span>
<span data-ttu-id="8aa9f-138">Wskazuje, że to polecenie cmdlet powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-138">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="8aa9f-139">Ponowne uruchomienie jest często wymagane do wprowadzenia zmiany.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-139">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="8aa9f-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8aa9f-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="8aa9f-141">Określa wersję rozszerzenia domeny.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-141">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="8aa9f-142">-VMName</span><span class="sxs-lookup"><span data-stu-id="8aa9f-142">-VMName</span></span>
<span data-ttu-id="8aa9f-143">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-143">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="8aa9f-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8aa9f-144">-Confirm</span></span>
<span data-ttu-id="8aa9f-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aa9f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aa9f-146">-WhatIf</span></span>
<span data-ttu-id="8aa9f-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8aa9f-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aa9f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa9f-149">CommonParameters</span></span>
<span data-ttu-id="8aa9f-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aa9f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa9f-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8aa9f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa9f-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8aa9f-152">INPUTS</span></span>

### <span data-ttu-id="8aa9f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="8aa9f-153">System.String</span></span>

### <span data-ttu-id="8aa9f-154">System. Nullable ' 1 [[System. UInt32; mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8aa9f-154">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="8aa9f-155">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="8aa9f-155">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="8aa9f-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8aa9f-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8aa9f-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8aa9f-157">OUTPUTS</span></span>

### <span data-ttu-id="8aa9f-158">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8aa9f-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8aa9f-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8aa9f-159">NOTES</span></span>

## <span data-ttu-id="8aa9f-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8aa9f-160">RELATED LINKS</span></span>

[<span data-ttu-id="8aa9f-161">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="8aa9f-161">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
