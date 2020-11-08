---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DECCEE-86C8-4662-9ED0-D1BDB4E687C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68efd1c750646abffa90eb8318d0df189a4c9eb9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054681"
---
# <span data-ttu-id="73551-101">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="73551-101">Add-AzureVMImage</span></span>

## <span data-ttu-id="73551-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73551-102">SYNOPSIS</span></span>
<span data-ttu-id="73551-103">Dodaje nowy obraz systemu operacyjnego lub nowy obraz maszyny wirtualnej do repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="73551-103">Adds a new operating system image or a new virtual machine image to the image repository.</span></span>

## <span data-ttu-id="73551-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73551-104">SYNTAX</span></span>

### <span data-ttu-id="73551-105">OSImage (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73551-105">OSImage (Default)</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-MediaLocation] <String> [-OS] <String> [[-Label] <String>]
 [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>]
 [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>] [[-SmallIconName] <String>]
 [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="73551-106">VMImage</span><span class="sxs-lookup"><span data-stu-id="73551-106">VMImage</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-OS] <String>]
 [[-Label] <String>] [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>]
 [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="73551-107">Opis</span><span class="sxs-lookup"><span data-stu-id="73551-107">DESCRIPTION</span></span>
<span data-ttu-id="73551-108">Polecenie cmdlet **Add-AzureVMImage** umożliwia dodanie nowego obrazu systemu operacyjnego lub nowego obrazu maszyny wirtualnej do repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="73551-108">The **Add-AzureVMImage** cmdlet adds a new operating system image or a new virtual machine image to the image repository.</span></span>
<span data-ttu-id="73551-109">Obraz jest uogólnionym obrazem systemu operacyjnego za pomocą narzędzia Sysprep dla systemu Windows lub w systemie Linux przy użyciu odpowiedniego narzędzia do dystrybucji.</span><span class="sxs-lookup"><span data-stu-id="73551-109">The image is a generalized operating system image, using either Sysprep for Windows or, for Linux, using the appropriate tool for the distribution.</span></span>

## <span data-ttu-id="73551-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73551-110">EXAMPLES</span></span>

### <span data-ttu-id="73551-111">Przykład 1: Dodawanie obrazu systemu operacyjnego do repozytorium</span><span class="sxs-lookup"><span data-stu-id="73551-111">Example 1: Add an operating system image to the repository</span></span>
```
PS C:\> $S = New-AzureVMImageDiskConfigSet
PS C:\> Set-AzureVMImageOSDiskConfig -DiskConfig $S -HostCaching ReadWrite -OSState "Generalized" -OS "Windows" -MediaLink $Link
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test1" -HostCaching ReadWrite -Lun 0 -MediaLink $Link1
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4" -HostCaching ReadWrite -Lun 0 -MediaLink $Link
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4"
PS C:\> $IMGName = "TestCREATEvmimage2";
PS C:\> Add-AzureVMImage -ImageName $IMGName -Label "Test1" -Description "Test1" -DiskConfig $S -Eula "http://www.contoso.com" -ImageFamily Windows -PublishedDate (Get-Date) -PrivacyUri "http://www.test.com" -RecommendedVMSize Small -IconName "Icon01" -SmallIconName "SmallIcon01" -ShowInGui
```

<span data-ttu-id="73551-112">W tym przykładzie przedstawiono Dodawanie obrazu systemu operacyjnego do repozytorium.</span><span class="sxs-lookup"><span data-stu-id="73551-112">This example adds an operating system image to the repository.</span></span>

## <span data-ttu-id="73551-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73551-113">PARAMETERS</span></span>

### <span data-ttu-id="73551-114">— Opis</span><span class="sxs-lookup"><span data-stu-id="73551-114">-Description</span></span>
<span data-ttu-id="73551-115">Umożliwia określenie opisu obrazu systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="73551-115">Specifies the description of the operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73551-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="73551-116">-DiskConfig</span></span>
<span data-ttu-id="73551-117">Określa konfigurację dysku systemu operacyjnego dla obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="73551-117">Specifies the operating system disk configuration for the virtual machine image.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: VMImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73551-118">— Umowa licencyjna użytkownika</span><span class="sxs-lookup"><span data-stu-id="73551-118">-Eula</span></span>
<span data-ttu-id="73551-119">Określa umowę licencyjną użytkownika końcowego.</span><span class="sxs-lookup"><span data-stu-id="73551-119">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="73551-120">Zaleca się używanie adresu URL dla tej wartości.</span><span class="sxs-lookup"><span data-stu-id="73551-120">It is recommended that you use an URL for this value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73551-121">-Iconname</span><span class="sxs-lookup"><span data-stu-id="73551-121">-IconName</span></span>
<span data-ttu-id="73551-122">Określa nazwę ikony używanej podczas dodawania obrazu do repozytorium.</span><span class="sxs-lookup"><span data-stu-id="73551-122">Specifies the name of the icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73551-123">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="73551-123">-ImageFamily</span></span>
<span data-ttu-id="73551-124">Określa wartość używaną do grupowania obrazów systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="73551-124">Specifies a value that is used to group operating system images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73551-125">-ImageName</span><span class="sxs-lookup"><span data-stu-id="73551-125">-ImageName</span></span>
<span data-ttu-id="73551-126">Określa nazwę obrazu dodawanego do repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="73551-126">Specifies the name of the image being added to the image repository.</span></span>

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

### <span data-ttu-id="73551-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="73551-127">-InformationAction</span></span>
<span data-ttu-id="73551-128">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="73551-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="73551-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="73551-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73551-130">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="73551-130">Continue</span></span>
- <span data-ttu-id="73551-131">Ignorować</span><span class="sxs-lookup"><span data-stu-id="73551-131">Ignore</span></span>
- <span data-ttu-id="73551-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="73551-132">Inquire</span></span>
- <span data-ttu-id="73551-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="73551-133">SilentlyContinue</span></span>
- <span data-ttu-id="73551-134">Przestaw</span><span class="sxs-lookup"><span data-stu-id="73551-134">Stop</span></span>
- <span data-ttu-id="73551-135">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="73551-135">Suspend</span></span>

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

### <span data-ttu-id="73551-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="73551-136">-InformationVariable</span></span>
<span data-ttu-id="73551-137">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="73551-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="73551-138">-Label</span><span class="sxs-lookup"><span data-stu-id="73551-138">-Label</span></span>
<span data-ttu-id="73551-139">Określa etykietę, która ma nadawać obraz.</span><span class="sxs-lookup"><span data-stu-id="73551-139">Specifies a label to give the image.</span></span>

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

### <span data-ttu-id="73551-140">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="73551-140">-MediaLocation</span></span>
<span data-ttu-id="73551-141">Określa lokalizację fizycznej strony obiektu BLOB, w której znajduje się obraz.</span><span class="sxs-lookup"><span data-stu-id="73551-141">Specifies the location of the physical blob page where the image resides.</span></span>
<span data-ttu-id="73551-142">To jest link do strony obiektu BLOB w magazynie bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="73551-142">This is a link to a blob page in the current subscription's storage.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73551-143">-OS</span><span class="sxs-lookup"><span data-stu-id="73551-143">-OS</span></span>
<span data-ttu-id="73551-144">Określa wersję systemu operacyjnego obrazu.</span><span class="sxs-lookup"><span data-stu-id="73551-144">Specifies the operating system version of the image.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: VMImage
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73551-145">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="73551-145">-PrivacyUri</span></span>
<span data-ttu-id="73551-146">Określa adres URL wskazujący dokument zawierający zasady ochrony danych osobowych związane z obrazem systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="73551-146">Specifies the URL that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73551-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="73551-147">-Profile</span></span>
<span data-ttu-id="73551-148">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73551-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73551-149">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="73551-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="73551-150">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="73551-150">-PublishedDate</span></span>
<span data-ttu-id="73551-151">Określa datę dodania obrazu systemu operacyjnego do repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="73551-151">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73551-152">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="73551-152">-RecommendedVMSize</span></span>
<span data-ttu-id="73551-153">Określa rozmiar, który ma być używany dla maszyny wirtualnej utworzonej na podstawie obrazu systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="73551-153">Specifies the size to use for the virtual machine that is created from the operating system image.</span></span>

<span data-ttu-id="73551-154">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="73551-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73551-155">Pożywkę</span><span class="sxs-lookup"><span data-stu-id="73551-155">Medium</span></span>
- <span data-ttu-id="73551-156">Większej</span><span class="sxs-lookup"><span data-stu-id="73551-156">Large</span></span>
- <span data-ttu-id="73551-157">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="73551-157">ExtraLarge</span></span>
- <span data-ttu-id="73551-158">A5</span><span class="sxs-lookup"><span data-stu-id="73551-158">A5</span></span>
- <span data-ttu-id="73551-159">A6</span><span class="sxs-lookup"><span data-stu-id="73551-159">A6</span></span>
- <span data-ttu-id="73551-160">A7</span><span class="sxs-lookup"><span data-stu-id="73551-160">A7</span></span>

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

### <span data-ttu-id="73551-161">-ShowInGui</span><span class="sxs-lookup"><span data-stu-id="73551-161">-ShowInGui</span></span>
<span data-ttu-id="73551-162">Wskazuje, że ten aplet polecenia wyświetla obraz w interfejsie GUI.</span><span class="sxs-lookup"><span data-stu-id="73551-162">Indicates that this cmdlet shows the image in the GUI.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73551-163">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="73551-163">-SmallIconName</span></span>
<span data-ttu-id="73551-164">Określa nazwę małej ikony, która jest używana podczas dodawania obrazu do repozytorium.</span><span class="sxs-lookup"><span data-stu-id="73551-164">Specifies the name of the small icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73551-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73551-165">CommonParameters</span></span>
<span data-ttu-id="73551-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73551-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73551-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73551-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73551-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73551-168">INPUTS</span></span>

## <span data-ttu-id="73551-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73551-169">OUTPUTS</span></span>

### <span data-ttu-id="73551-170">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="73551-170">OSImageContext</span></span>

## <span data-ttu-id="73551-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73551-171">NOTES</span></span>

## <span data-ttu-id="73551-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73551-172">RELATED LINKS</span></span>

[<span data-ttu-id="73551-173">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="73551-173">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="73551-174">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="73551-174">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="73551-175">Zapisz — AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="73551-175">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="73551-176">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="73551-176">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


