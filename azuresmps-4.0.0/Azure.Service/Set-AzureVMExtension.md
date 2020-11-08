---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E9FB22-43A8-4D07-AF48-5884E4593CA9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f3baea7440d58812056999ea4f271acf80b8d4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054412"
---
# <span data-ttu-id="54147-101">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="54147-101">Set-AzureVMExtension</span></span>

## <span data-ttu-id="54147-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54147-102">SYNOPSIS</span></span>
<span data-ttu-id="54147-103">Ustawia rozszerzenia zasobów dla maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="54147-103">Sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="54147-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54147-104">SYNTAX</span></span>

### <span data-ttu-id="54147-105">SetByExtensionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="54147-105">SetByExtensionName (Default)</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfiguration] <String>] [[-PrivateConfiguration] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="54147-106">SetByExtensionNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="54147-106">SetByExtensionNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="54147-107">SetByReferenceName</span><span class="sxs-lookup"><span data-stu-id="54147-107">SetByReferenceName</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfiguration] <String>]
 [[-PrivateConfiguration] <String>] [-Disable] [-Uninstall] [[-PublicConfigKey] <String>]
 [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="54147-108">SetByReferenceNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="54147-108">SetByReferenceNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>]
 [-Disable] [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="54147-109">Opis</span><span class="sxs-lookup"><span data-stu-id="54147-109">DESCRIPTION</span></span>
<span data-ttu-id="54147-110">Polecenie cmdlet **Set-AzureVMExtension** ustawia rozszerzenia zasobów dla maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="54147-110">The **Set-AzureVMExtension** cmdlet sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="54147-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54147-111">EXAMPLES</span></span>

### <span data-ttu-id="54147-112">Przykład 1: Tworzenie maszyny wirtualnej z zastosowanymi rozszerzeniami zasobów</span><span class="sxs-lookup"><span data-stu-id="54147-112">Example 1: Create a virtual machine with resource extensions applied</span></span>
```
PS C:\> $X = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $IMG;$X = Add-AzureProvisioningConfig -VM $X -Password $PWD -AdminUsername $USR -Windows;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext1 -Publisher $Publisher -Version $VER -PublicConfiguration $P1 -PrivateConfiguration $P2;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext2 -Publisher $Publisher -Version $VER -PublicConfiguration $P3 -PrivateConfiguration $P4;New-AzureVM -Location $LOC -ServiceName $SVC -VM $X;
```

<span data-ttu-id="54147-113">To polecenie powoduje utworzenie maszyny wirtualnej z zastosowanymi rozszerzeniami zasobów.</span><span class="sxs-lookup"><span data-stu-id="54147-113">This command creates a virtual machine with resource extensions applied.</span></span>

## <span data-ttu-id="54147-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54147-114">PARAMETERS</span></span>

### <span data-ttu-id="54147-115">-Disable</span><span class="sxs-lookup"><span data-stu-id="54147-115">-Disable</span></span>
<span data-ttu-id="54147-116">Wskazuje, że to polecenie cmdlet wyłącza stan rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="54147-116">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-117">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="54147-117">-ExtensionName</span></span>
<span data-ttu-id="54147-118">Określa nazwę rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="54147-118">Specifies the extension name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-119">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="54147-119">-ForceUpdate</span></span>
<span data-ttu-id="54147-120">Wskazuje, że ten aplet polecenia ponownie zastosuje konfigurację do rozszerzenia, gdy konfiguracja nie została zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="54147-120">Indicates that this cmdlet re-applies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54147-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="54147-121">-InformationAction</span></span>
<span data-ttu-id="54147-122">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="54147-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="54147-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="54147-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="54147-124">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="54147-124">Continue</span></span>
- <span data-ttu-id="54147-125">Ignorować</span><span class="sxs-lookup"><span data-stu-id="54147-125">Ignore</span></span>
- <span data-ttu-id="54147-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="54147-126">Inquire</span></span>
- <span data-ttu-id="54147-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="54147-127">SilentlyContinue</span></span>
- <span data-ttu-id="54147-128">Przestaw</span><span class="sxs-lookup"><span data-stu-id="54147-128">Stop</span></span>
- <span data-ttu-id="54147-129">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="54147-129">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54147-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="54147-130">-InformationVariable</span></span>
<span data-ttu-id="54147-131">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="54147-131">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54147-132">-PrivateConfigKey</span><span class="sxs-lookup"><span data-stu-id="54147-132">-PrivateConfigKey</span></span>
<span data-ttu-id="54147-133">Określa prywatny klucz konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="54147-133">Specifies a private configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-134">-PrivateConfigPath</span><span class="sxs-lookup"><span data-stu-id="54147-134">-PrivateConfigPath</span></span>
<span data-ttu-id="54147-135">Określa ścieżkę konfiguracji prywatnej.</span><span class="sxs-lookup"><span data-stu-id="54147-135">Specifies the private configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-136">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="54147-136">-PrivateConfiguration</span></span>
<span data-ttu-id="54147-137">Określa tekst konfiguracji prywatnej.</span><span class="sxs-lookup"><span data-stu-id="54147-137">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="54147-138">-Profile</span></span>
<span data-ttu-id="54147-139">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54147-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54147-140">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="54147-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54147-141">-PublicConfigKey</span><span class="sxs-lookup"><span data-stu-id="54147-141">-PublicConfigKey</span></span>
<span data-ttu-id="54147-142">Umożliwia określenie klucza konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="54147-142">Specifies the public configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-143">-PublicConfigPath</span><span class="sxs-lookup"><span data-stu-id="54147-143">-PublicConfigPath</span></span>
<span data-ttu-id="54147-144">Określa ścieżkę konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="54147-144">Specifies the public configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-145">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="54147-145">-PublicConfiguration</span></span>
<span data-ttu-id="54147-146">Określa tekst konfiguracji publicznej.</span><span class="sxs-lookup"><span data-stu-id="54147-146">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-147">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="54147-147">-Publisher</span></span>
<span data-ttu-id="54147-148">Określa wydawcę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="54147-148">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-149">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="54147-149">-ReferenceName</span></span>
<span data-ttu-id="54147-150">Określa nazwę referencyjną rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="54147-150">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="54147-151">Jest to ciąg zdefiniowany przez użytkownika, za pomocą którego można odwołać się do rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="54147-151">This is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="54147-152">Musisz ją określić, gdy rozszerzenie zostanie dodane do maszyny wirtualnej po raz pierwszy.</span><span class="sxs-lookup"><span data-stu-id="54147-152">You need to specify it when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="54147-153">W przypadku kolejnych aktualizacji należy określić poprzednio zastosowaną nazwę referencyjną podczas aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="54147-153">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="54147-154">Element ReferenceName przypisany do rozszerzenia jest zwracany przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="54147-154">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByReferenceName, SetByReferenceNameAndConfigFile
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-155">— Odinstalowywanie</span><span class="sxs-lookup"><span data-stu-id="54147-155">-Uninstall</span></span>
<span data-ttu-id="54147-156">Wskazuje, że to polecenie cmdlet Odinstalowuje rozszerzenie zasobu z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="54147-156">Indicates that this cmdlet uninstalls the resource extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-157">-Version</span><span class="sxs-lookup"><span data-stu-id="54147-157">-Version</span></span>
<span data-ttu-id="54147-158">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="54147-158">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-159">-VM</span><span class="sxs-lookup"><span data-stu-id="54147-159">-VM</span></span>
<span data-ttu-id="54147-160">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="54147-160">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54147-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54147-161">CommonParameters</span></span>
<span data-ttu-id="54147-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54147-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54147-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54147-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54147-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54147-164">INPUTS</span></span>

## <span data-ttu-id="54147-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54147-165">OUTPUTS</span></span>

## <span data-ttu-id="54147-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54147-166">NOTES</span></span>

## <span data-ttu-id="54147-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54147-167">RELATED LINKS</span></span>

[<span data-ttu-id="54147-168">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="54147-168">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="54147-169">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="54147-169">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="54147-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="54147-170">Get-AzureVM</span></span>](./Get-AzureVM.md)


