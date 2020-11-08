---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A05B39BF-87EB-471E-9FCD-F7807CB46B4D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1aa7cff6d655bf33fa1a317516fda20237f6fc14
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055004"
---
# <span data-ttu-id="b4a79-101">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b4a79-101">Set-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="b4a79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4a79-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a79-103">Konfiguruje rozszerzenie Diagnostyka platformy Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4a79-103">Configures the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="b4a79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4a79-104">SYNTAX</span></span>

### <span data-ttu-id="b4a79-105">SetDiagnosticsExtension (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b4a79-105">SetDiagnosticsExtension (Default)</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4a79-106">SetDiagnosticsWithReferenceExtension</span><span class="sxs-lookup"><span data-stu-id="b4a79-106">SetDiagnosticsWithReferenceExtension</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b4a79-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b4a79-107">DESCRIPTION</span></span>
<span data-ttu-id="b4a79-108">Polecenie cmdlet **Set-AzureVMDiagnosticsExtension** konfiguruje rozszerzenie Diagnostyka platformy Microsoft Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4a79-108">The **Set-AzureVMDiagnosticsExtension** cmdlet configures the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="b4a79-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4a79-109">EXAMPLES</span></span>

### <span data-ttu-id="b4a79-110">Przykład 1: Tworzenie maszyny wirtualnej z zastosowanym rozszerzeniem usługi Azure Diagnostics</span><span class="sxs-lookup"><span data-stu-id="b4a79-110">Example 1: Create a virtual machine with Azure Diagnostics extension applied</span></span>
```
PS C:\> $VM = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $VMImage
PS C:\> $VM = Add-AzureProvisioningConfig -VM $VM -AdminUsername $Username -Password $Password -Windows
PS C:\> $VM = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> New-AzureVM -Location $Location -ServiceName $Service_Name -VM $VM
```

<span data-ttu-id="b4a79-111">Te polecenia umożliwiają włączenie rozszerzenia Diagnostyka platformy Azure na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4a79-111">These commands enable the Azure Diagnostics extension on a virtual machine.</span></span>

### <span data-ttu-id="b4a79-112">Przykład 2: Włączanie rozszerzenia Diagnostyka platformy Azure na istniejącej maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b4a79-112">Example 2: Enable an Azure Diagnostics extension on an existing virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName $Service_Name -Name $VM_Name
PS C:\> $VM_Update = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> Update-AzureVM -ServiceName $Service_Name -Name $VM_Name -VM $VM_Update.VM
```

<span data-ttu-id="b4a79-113">W pierwszym poleceniu jest używana funkcja cmdlet **Get-AzureVM** w celu uzyskania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4a79-113">The first command uses the **Get-AzureVM** cmdlet to get a virtual machine.</span></span>

<span data-ttu-id="b4a79-114">Drugie polecenie używa polecenia cmdlet **Set-AzureVMDiagnosticsExtension** w celu zaktualizowania konfiguracji maszyny wirtualnej w celu uwzględnienia rozszerzenia diagnostycznego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b4a79-114">The second command uses the **Set-AzureVMDiagnosticsExtension** cmdlet to update the virtual machine configuration to include the Azure Diagnostics extension.</span></span>

<span data-ttu-id="b4a79-115">Polecenie ostatnie powoduje zastosowanie zaktualizowanej konfiguracji do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4a79-115">The final command applies the updated configuration to the virtual machine.</span></span>

## <span data-ttu-id="b4a79-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4a79-116">PARAMETERS</span></span>

### <span data-ttu-id="b4a79-117">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="b4a79-117">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="b4a79-118">Określa ścieżkę do konfiguracji diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="b4a79-118">Specifies a path for the diagnostics configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a79-119">-Disable</span><span class="sxs-lookup"><span data-stu-id="b4a79-119">-Disable</span></span>
<span data-ttu-id="b4a79-120">Wskazuje, że to polecenie cmdlet wyłącza rozszerzenie Diagnostyka na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4a79-120">Indicates that this cmdlet disables the diagnostics extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a79-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b4a79-121">-InformationAction</span></span>
<span data-ttu-id="b4a79-122">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="b4a79-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b4a79-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b4a79-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4a79-124">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="b4a79-124">Continue</span></span>
- <span data-ttu-id="b4a79-125">Ignorować</span><span class="sxs-lookup"><span data-stu-id="b4a79-125">Ignore</span></span>
- <span data-ttu-id="b4a79-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="b4a79-126">Inquire</span></span>
- <span data-ttu-id="b4a79-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b4a79-127">SilentlyContinue</span></span>
- <span data-ttu-id="b4a79-128">Przestaw</span><span class="sxs-lookup"><span data-stu-id="b4a79-128">Stop</span></span>
- <span data-ttu-id="b4a79-129">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="b4a79-129">Suspend</span></span>

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

### <span data-ttu-id="b4a79-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b4a79-130">-InformationVariable</span></span>
<span data-ttu-id="b4a79-131">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="b4a79-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b4a79-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="b4a79-132">-Profile</span></span>
<span data-ttu-id="b4a79-133">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4a79-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4a79-134">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b4a79-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4a79-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="b4a79-135">-ReferenceName</span></span>
<span data-ttu-id="b4a79-136">Określa nazwę referencyjną rozszerzenia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="b4a79-136">Specifies the reference name for the diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: SetDiagnosticsWithReferenceExtension
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a79-137">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4a79-137">-StorageAccountEndpoint</span></span>
<span data-ttu-id="b4a79-138">Określa punkt końcowy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b4a79-138">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a79-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b4a79-139">-StorageAccountKey</span></span>
<span data-ttu-id="b4a79-140">Określa klucz konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b4a79-140">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a79-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4a79-141">-StorageAccountName</span></span>
<span data-ttu-id="b4a79-142">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b4a79-142">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="b4a79-143">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="b4a79-143">-StorageContext</span></span>
<span data-ttu-id="b4a79-144">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="b4a79-144">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a79-145">-Version</span><span class="sxs-lookup"><span data-stu-id="b4a79-145">-Version</span></span>
<span data-ttu-id="b4a79-146">Określa wersję rozszerzenia jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="b4a79-146">Specifies the extension version as a string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a79-147">-VM</span><span class="sxs-lookup"><span data-stu-id="b4a79-147">-VM</span></span>
<span data-ttu-id="b4a79-148">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b4a79-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="b4a79-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a79-149">CommonParameters</span></span>
<span data-ttu-id="b4a79-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4a79-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a79-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4a79-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a79-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4a79-152">INPUTS</span></span>

## <span data-ttu-id="b4a79-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4a79-153">OUTPUTS</span></span>

## <span data-ttu-id="b4a79-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4a79-154">NOTES</span></span>

## <span data-ttu-id="b4a79-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4a79-155">RELATED LINKS</span></span>

[<span data-ttu-id="b4a79-156">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b4a79-156">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="b4a79-157">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b4a79-157">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="b4a79-158">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b4a79-158">Update-AzureVM</span></span>](./Update-AzureVM.md)


