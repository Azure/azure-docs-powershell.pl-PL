---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: c77fe7985e91386cad746c61f5849072e0366615
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525590"
---
# <span data-ttu-id="3f7dd-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3f7dd-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="3f7dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f7dd-102">SYNOPSIS</span></span>
<span data-ttu-id="3f7dd-103">Dodaje rozszerzenie VMAccess do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f7dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f7dd-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-UserName <String>] [-Password <String>] [-ResourceGroupName] <String>
 [-VMName] <String> [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f7dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f7dd-105">DESCRIPTION</span></span>
<span data-ttu-id="3f7dd-106">Polecenie cmdlet **Set-AzureRmVMAccessExtension** umożliwia dodanie rozszerzenia maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess) do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="3f7dd-107">VMAccess może zresetować nazwę użytkownika i hasło maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-107">VMAccess can reset the virtual machine user name and password.</span></span>

## <span data-ttu-id="3f7dd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f7dd-108">EXAMPLES</span></span>

### <span data-ttu-id="3f7dd-109">Przykład 1: Dodawanie rozszerzenia VMAccess</span><span class="sxs-lookup"><span data-stu-id="3f7dd-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="3f7dd-110">To polecenie umożliwia dodanie rozszerzenia VMAccess dla maszyny wirtualnej o nazwie VirtualMachine07 w ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="3f7dd-111">To polecenie określa nazwę i typ programu obsługi VMAccess.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="3f7dd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f7dd-112">PARAMETERS</span></span>

### <span data-ttu-id="3f7dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f7dd-113">-DefaultProfile</span></span>
<span data-ttu-id="3f7dd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f7dd-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3f7dd-115">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="3f7dd-116">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="3f7dd-116">-ForceRerun</span></span>
<span data-ttu-id="3f7dd-117">Wskazuje, że to polecenie cmdlet Wymusza ponowne uruchomienie tej samej konfiguracji rozszerzenia na maszynie wirtualnej bez odinstalowywania i ponownego instalowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-117">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="3f7dd-118">Wartością może być dowolny ciąg różny od bieżącej wartości.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-118">The value can be any string different from the current value.</span></span>

<span data-ttu-id="3f7dd-119">Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-119">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="3f7dd-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3f7dd-120">-Location</span></span>
<span data-ttu-id="3f7dd-121">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-121">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="3f7dd-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3f7dd-122">-Name</span></span>
<span data-ttu-id="3f7dd-123">Określa nazwę rozszerzenia, które zostało dodane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-123">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="3f7dd-124">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="3f7dd-124">-Password</span></span>
<span data-ttu-id="3f7dd-125">Określa nowe hasło maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-125">Specifies the new password of the virtual machine.</span></span>

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

### <span data-ttu-id="3f7dd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f7dd-126">-ResourceGroupName</span></span>
<span data-ttu-id="3f7dd-127">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3f7dd-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3f7dd-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="3f7dd-129">Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="3f7dd-130">Aby uzyskać wersję, uruchom polecenie cmdlet Get-AzureRmVMExtensionImage z wartością argumentu Microsoft. COMPUTE dla parametru *wydawcy* i VMAccessAgent dla parametru *Type* .</span><span class="sxs-lookup"><span data-stu-id="3f7dd-130">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="3f7dd-131">-UserName</span><span class="sxs-lookup"><span data-stu-id="3f7dd-131">-UserName</span></span>
<span data-ttu-id="3f7dd-132">Określa nową nazwę użytkownika dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-132">Specifies the new user name for the virtual machine.</span></span>

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

### <span data-ttu-id="3f7dd-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="3f7dd-133">-VMName</span></span>
<span data-ttu-id="3f7dd-134">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3f7dd-135">To polecenie cmdlet umożliwia dodanie VMAccess dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f7dd-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3f7dd-136">-Confirm</span></span>
<span data-ttu-id="3f7dd-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f7dd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f7dd-138">-WhatIf</span></span>
<span data-ttu-id="3f7dd-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3f7dd-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f7dd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f7dd-141">CommonParameters</span></span>
<span data-ttu-id="3f7dd-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f7dd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f7dd-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f7dd-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f7dd-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f7dd-144">INPUTS</span></span>

## <span data-ttu-id="3f7dd-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f7dd-145">OUTPUTS</span></span>

## <span data-ttu-id="3f7dd-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f7dd-146">NOTES</span></span>

## <span data-ttu-id="3f7dd-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f7dd-147">RELATED LINKS</span></span>

[<span data-ttu-id="3f7dd-148">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3f7dd-148">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3f7dd-149">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3f7dd-149">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3f7dd-150">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3f7dd-150">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="3f7dd-151">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3f7dd-151">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


