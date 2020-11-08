---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A8F07D1-AC20-4950-9019-BDFB4FD3CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7569e203369bf1177b4eecc2bd689f3e20dcd48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055003"
---
# <span data-ttu-id="89fb6-101">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="89fb6-101">Set-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="89fb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="89fb6-103">Ustawia informacje dotyczące niestandardowego rozszerzenia skryptu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="89fb6-103">Sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="89fb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89fb6-104">SYNTAX</span></span>

### <span data-ttu-id="89fb6-105">SetCustomScriptExtensionByContainerAndFileNames (domyślny)</span><span class="sxs-lookup"><span data-stu-id="89fb6-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-ContainerName] <String>
 [-FileName] <String[]> [[-StorageAccountName] <String>] [[-StorageEndpointSuffix] <String>]
 [[-StorageAccountKey] <String>] [[-Run] <String>] [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="89fb6-106">DisableCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="89fb6-106">DisableCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89fb6-107">UninstalleCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="89fb6-107">UninstalleCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89fb6-108">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="89fb6-108">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [[-FileUri] <String[]>]
 [-Run] <String> [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="89fb6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="89fb6-109">DESCRIPTION</span></span>
<span data-ttu-id="89fb6-110">Polecenie cmdlet **Set-AzureVMCustomScriptExtension** ustawia informacje dotyczące niestandardowego rozszerzenia skryptu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="89fb6-110">The **Set-AzureVMCustomScriptExtension** cmdlet sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="89fb6-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89fb6-111">EXAMPLES</span></span>

### <span data-ttu-id="89fb6-112">Przykład 1: Ustawianie informacji dotyczących niestandardowego rozszerzenia skryptu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="89fb6-112">Example 1: Set information for a virtual machine custom script extension</span></span>
```
PS C:\> $VM = Set-AzureVMCustomScriptExtension -VM $VM -ContainerName "Container01" -FileName "script1.ps1","script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> New-AzureVM -Location "West US" -ServiceName $SVC -VM $VM;
```

<span data-ttu-id="89fb6-113">To polecenie ustawia informacje dotyczące niestandardowego rozszerzenia skryptu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89fb6-113">This command sets information for a virtual machine custom script extension.</span></span>

### <span data-ttu-id="89fb6-114">Przykład 2: Ustawianie informacji dotyczących niestandardowego rozszerzenia skryptu maszyny wirtualnej za pomocą ścieżki pliku</span><span class="sxs-lookup"><span data-stu-id="89fb6-114">Example 2: Set information for a virtual machine custom script extension using a file path</span></span>
```
PS C:\> Set-AzureVMCustomScriptExtension -VM $VM -FileUri "http://www.blob.core.contoso.net/bar/script1.ps1","http://www.blob.core.contoso.net/baz/script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> Update-AzureVM -ServiceName $SVC -Name $Name -VM VM;
```

<span data-ttu-id="89fb6-115">To polecenie ustawia informacje dotyczące niestandardowego rozszerzenia skryptu maszyny wirtualnej przy użyciu wielu adresów URL plików.</span><span class="sxs-lookup"><span data-stu-id="89fb6-115">This command sets information for a virtual machine custom script extension using multiple file URLs.</span></span>

## <span data-ttu-id="89fb6-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89fb6-116">PARAMETERS</span></span>

### <span data-ttu-id="89fb6-117">-Argument</span><span class="sxs-lookup"><span data-stu-id="89fb6-117">-Argument</span></span>
<span data-ttu-id="89fb6-118">Określa ciąg, który dostarcza argument, który jest uruchamiany przez to polecenie cmdlet na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89fb6-118">Specifies a string that supplies an argument that this cmdlet runs on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames, SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-119">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="89fb6-119">-ContainerName</span></span>
<span data-ttu-id="89fb6-120">Określa nazwę kontenera na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="89fb6-120">Specifies the container name within the storage account.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-121">-Disable</span><span class="sxs-lookup"><span data-stu-id="89fb6-121">-Disable</span></span>
<span data-ttu-id="89fb6-122">Wskazuje, że to polecenie cmdlet wyłącza stan rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="89fb6-122">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-123">-FileName</span><span class="sxs-lookup"><span data-stu-id="89fb6-123">-FileName</span></span>
<span data-ttu-id="89fb6-124">Określa tablicę ciągów zawierającą nazwy plików BLOB w określonym kontenerze.</span><span class="sxs-lookup"><span data-stu-id="89fb6-124">Specifies a string array that contains the names of the blob files in the specified container.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-125">-FileUri</span><span class="sxs-lookup"><span data-stu-id="89fb6-125">-FileUri</span></span>
<span data-ttu-id="89fb6-126">Określa tablicę ciągów zawierającą adresy URL plików BLOB.</span><span class="sxs-lookup"><span data-stu-id="89fb6-126">Specifies a string array that contains the URLs of the blob files.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-127">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="89fb6-127">-ForceUpdate</span></span>
<span data-ttu-id="89fb6-128">Wskazuje, że ten aplet polecenia ponownie zastosuje konfigurację do rozszerzenia, gdy konfiguracja nie została zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="89fb6-128">Indicates that this cmdlet re-apply a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="89fb6-129">-InformationAction</span></span>
<span data-ttu-id="89fb6-130">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="89fb6-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="89fb6-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="89fb6-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89fb6-132">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="89fb6-132">Continue</span></span>
- <span data-ttu-id="89fb6-133">Ignorować</span><span class="sxs-lookup"><span data-stu-id="89fb6-133">Ignore</span></span>
- <span data-ttu-id="89fb6-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="89fb6-134">Inquire</span></span>
- <span data-ttu-id="89fb6-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="89fb6-135">SilentlyContinue</span></span>
- <span data-ttu-id="89fb6-136">Przestaw</span><span class="sxs-lookup"><span data-stu-id="89fb6-136">Stop</span></span>
- <span data-ttu-id="89fb6-137">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="89fb6-137">Suspend</span></span>

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

### <span data-ttu-id="89fb6-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="89fb6-138">-InformationVariable</span></span>
<span data-ttu-id="89fb6-139">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="89fb6-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="89fb6-140">-Profile</span><span class="sxs-lookup"><span data-stu-id="89fb6-140">-Profile</span></span>
<span data-ttu-id="89fb6-141">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89fb6-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89fb6-142">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="89fb6-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89fb6-143">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="89fb6-143">-ReferenceName</span></span>
<span data-ttu-id="89fb6-144">Określa nazwę odwołania dla rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="89fb6-144">Specifies the reference name for the extension.</span></span>

<span data-ttu-id="89fb6-145">Ten parametr jest ciągiem zdefiniowanym przez użytkownika, którego można używać w celu odwoływania się do rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="89fb6-145">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="89fb6-146">Jest ona określana po pierwszym dodaniu rozszerzenia do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89fb6-146">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="89fb6-147">W przypadku kolejnych aktualizacji należy określić poprzednio zastosowaną nazwę referencyjną podczas aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="89fb6-147">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="89fb6-148">Element *ReferenceName* przypisany do rozszerzenia jest zwracany przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="89fb6-148">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-149">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="89fb6-149">-Run</span></span>
<span data-ttu-id="89fb6-150">Określa polecenie uruchomienie tego polecenia cmdlet przez rozszerzenie na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89fb6-150">Specifies the command this cmdlet runs by the extension on the virtual machine.</span></span>
<span data-ttu-id="89fb6-151">Obsługiwane są tylko "powershell.exe".</span><span class="sxs-lookup"><span data-stu-id="89fb6-151">Only "powershell.exe" is supported.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: RunFile, Command

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: RunFile, Command

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-152">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="89fb6-152">-StorageAccountKey</span></span>
<span data-ttu-id="89fb6-153">Określa klucz konta magazynu</span><span class="sxs-lookup"><span data-stu-id="89fb6-153">Specifies the storage account key</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="89fb6-154">-StorageAccountName</span></span>
<span data-ttu-id="89fb6-155">Określa nazwę konta magazynu w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="89fb6-155">Specifies the storage account name in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-156">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="89fb6-156">-StorageEndpointSuffix</span></span>
<span data-ttu-id="89fb6-157">Określa punkt końcowy usługi Storage Service.</span><span class="sxs-lookup"><span data-stu-id="89fb6-157">Specifies the storage service endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-158">— Odinstalowywanie</span><span class="sxs-lookup"><span data-stu-id="89fb6-158">-Uninstall</span></span>
<span data-ttu-id="89fb6-159">Wskazuje, że to polecenie cmdlet Odinstalowuje niestandardowe rozszerzenie skryptu z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89fb6-159">Indicates that this cmdlet uninstalls the custom script extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstalleCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-160">-Version</span><span class="sxs-lookup"><span data-stu-id="89fb6-160">-Version</span></span>
<span data-ttu-id="89fb6-161">Określa wersję niestandardowego rozszerzenia skryptu.</span><span class="sxs-lookup"><span data-stu-id="89fb6-161">Specifies the version of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb6-162">-VM</span><span class="sxs-lookup"><span data-stu-id="89fb6-162">-VM</span></span>
<span data-ttu-id="89fb6-163">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="89fb6-163">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="89fb6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89fb6-164">CommonParameters</span></span>
<span data-ttu-id="89fb6-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89fb6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89fb6-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89fb6-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89fb6-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89fb6-167">INPUTS</span></span>

## <span data-ttu-id="89fb6-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89fb6-168">OUTPUTS</span></span>

## <span data-ttu-id="89fb6-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89fb6-169">NOTES</span></span>

## <span data-ttu-id="89fb6-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89fb6-170">RELATED LINKS</span></span>

[<span data-ttu-id="89fb6-171">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="89fb6-171">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="89fb6-172">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="89fb6-172">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="89fb6-173">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="89fb6-173">Get-AzureVM</span></span>](./Get-AzureVM.md)


