---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055549"
---
# <span data-ttu-id="08a52-101">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="08a52-101">Update-AzureVMImage</span></span>

## <span data-ttu-id="08a52-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08a52-102">SYNOPSIS</span></span>
<span data-ttu-id="08a52-103">Umożliwia zaktualizowanie etykiety obrazu systemu operacyjnego w repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="08a52-103">Updates the label of an operating system image in the image repository.</span></span>

## <span data-ttu-id="08a52-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08a52-104">SYNTAX</span></span>

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="08a52-105">Opis</span><span class="sxs-lookup"><span data-stu-id="08a52-105">DESCRIPTION</span></span>
<span data-ttu-id="08a52-106">Polecenie cmdlet **Update-AzureVMImage** aktualizuje etykietę obrazu systemu operacyjnego w repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="08a52-106">The **Update-AzureVMImage** cmdlet updates the label on an operating system image in the image repository.</span></span>
<span data-ttu-id="08a52-107">Zwraca obiekt obrazu z informacją o zaktualizowanym obrazie.</span><span class="sxs-lookup"><span data-stu-id="08a52-107">It returns an image object with information about the updated image.</span></span>

## <span data-ttu-id="08a52-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08a52-108">EXAMPLES</span></span>

### <span data-ttu-id="08a52-109">Przykład 1: aktualizowanie obrazu przez zmianę etykiety obrazu</span><span class="sxs-lookup"><span data-stu-id="08a52-109">Example 1: Update an image by changing the image label</span></span>
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

<span data-ttu-id="08a52-110">To polecenie aktualizuje obraz o nazwie Windows-Server-2008-SP2, zmieniając etykietę obrazu na DoNotUse.</span><span class="sxs-lookup"><span data-stu-id="08a52-110">This command updates the image named Windows-Server-2008-SP2 by changing the image label to DoNotUse.</span></span>

### <span data-ttu-id="08a52-111">Przykład 2: uzyskiwanie wszystkich systemów operacyjnych według etykiet, a następnie aktualizowanie etykiety</span><span class="sxs-lookup"><span data-stu-id="08a52-111">Example 2: Get all operating systems by label and then update the label</span></span>
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

<span data-ttu-id="08a52-112">To polecenie pobiera wszystkie obrazy systemu operacyjnego oznaczone etykietą DoNotUse i zmienia etykietę na zaktualizowaną.</span><span class="sxs-lookup"><span data-stu-id="08a52-112">This command gets all the operating system images labeled DoNotUse and changes the label to Updated.</span></span>

## <span data-ttu-id="08a52-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08a52-113">PARAMETERS</span></span>

### <span data-ttu-id="08a52-114">— Opis</span><span class="sxs-lookup"><span data-stu-id="08a52-114">-Description</span></span>
<span data-ttu-id="08a52-115">Umożliwia określenie opisu obrazu systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="08a52-115">Specifies the description of the operating system image.</span></span>

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

### <span data-ttu-id="08a52-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="08a52-116">-DiskConfig</span></span>
<span data-ttu-id="08a52-117">Określa konfigurację dysku systemu operacyjnego i dysku danych dla obrazu maszyny wirtualnej utworzonego za pomocą poleceń cmdlet **New-AzureVMImageDiskConfigSet** , **Set-AzureVMImageOSDiskConfig** i **Set-AzureVMImageDataDiskConfig** .</span><span class="sxs-lookup"><span data-stu-id="08a52-117">Specifies the operating system disk and data disk configuration for the virtual machine image created by using the **New-AzureVMImageDiskConfigSet** , **Set-AzureVMImageOSDiskConfig** , and **Set-AzureVMImageDataDiskConfig** cmdlets.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08a52-118">-DontShowInGui</span><span class="sxs-lookup"><span data-stu-id="08a52-118">-DontShowInGui</span></span>
<span data-ttu-id="08a52-119">Wskazuje, że ten aplet polecenia nie wyświetla obrazu w interfejsie GUI.</span><span class="sxs-lookup"><span data-stu-id="08a52-119">Indicates that this cmdlet does not show the image in the GUI.</span></span>

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

### <span data-ttu-id="08a52-120">— Umowa licencyjna użytkownika</span><span class="sxs-lookup"><span data-stu-id="08a52-120">-Eula</span></span>
<span data-ttu-id="08a52-121">Określa umowę licencyjną użytkownika końcowego.</span><span class="sxs-lookup"><span data-stu-id="08a52-121">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="08a52-122">Zalecamy, aby wartość była adresem URL.</span><span class="sxs-lookup"><span data-stu-id="08a52-122">We recommend that the value is a URL.</span></span>

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

### <span data-ttu-id="08a52-123">-Iconname</span><span class="sxs-lookup"><span data-stu-id="08a52-123">-IconName</span></span>
<span data-ttu-id="08a52-124">Określa standardową nazwę ikony dla systemu operacyjnego lub obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="08a52-124">Specifies the standard icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="08a52-125">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="08a52-125">-ImageFamily</span></span>
<span data-ttu-id="08a52-126">Określa wartość, która może być używana do grupowania obrazów systemu operacyjnego lub maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="08a52-126">Specifies a value that can be used to group operating system or virtual machine images.</span></span>

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

### <span data-ttu-id="08a52-127">-ImageName</span><span class="sxs-lookup"><span data-stu-id="08a52-127">-ImageName</span></span>
<span data-ttu-id="08a52-128">Określa nazwę obrazu do zaktualizowania w repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="08a52-128">Specifies the name of the image to update in the image repository.</span></span>

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

### <span data-ttu-id="08a52-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="08a52-129">-InformationAction</span></span>
<span data-ttu-id="08a52-130">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="08a52-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="08a52-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="08a52-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08a52-132">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="08a52-132">Continue</span></span>
- <span data-ttu-id="08a52-133">Ignorować</span><span class="sxs-lookup"><span data-stu-id="08a52-133">Ignore</span></span>
- <span data-ttu-id="08a52-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="08a52-134">Inquire</span></span>
- <span data-ttu-id="08a52-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="08a52-135">SilentlyContinue</span></span>
- <span data-ttu-id="08a52-136">Przestaw</span><span class="sxs-lookup"><span data-stu-id="08a52-136">Stop</span></span>
- <span data-ttu-id="08a52-137">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="08a52-137">Suspend</span></span>

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

### <span data-ttu-id="08a52-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="08a52-138">-InformationVariable</span></span>
<span data-ttu-id="08a52-139">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="08a52-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="08a52-140">-Label</span><span class="sxs-lookup"><span data-stu-id="08a52-140">-Label</span></span>
<span data-ttu-id="08a52-141">Określa nową etykietę obrazu.</span><span class="sxs-lookup"><span data-stu-id="08a52-141">Specifies the new label of the image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08a52-142">-Language</span><span class="sxs-lookup"><span data-stu-id="08a52-142">-Language</span></span>
<span data-ttu-id="08a52-143">Określa język systemu operacyjnego w obrazie maszyny wirtualnej lub systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="08a52-143">Specifies the language for the operating system in the virtual machine or operating system image.</span></span>

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

### <span data-ttu-id="08a52-144">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="08a52-144">-PrivacyUri</span></span>
<span data-ttu-id="08a52-145">Określa identyfikator URI wskazujący dokument zawierający zasady ochrony danych osobowych związane z obrazem systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="08a52-145">Specifies the URI that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08a52-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="08a52-146">-Profile</span></span>
<span data-ttu-id="08a52-147">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08a52-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="08a52-148">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="08a52-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08a52-149">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="08a52-149">-PublishedDate</span></span>
<span data-ttu-id="08a52-150">Określa datę dodania obrazu systemu operacyjnego do repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="08a52-150">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08a52-151">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="08a52-151">-RecommendedVMSize</span></span>
<span data-ttu-id="08a52-152">Określa rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="08a52-152">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="08a52-153">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="08a52-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08a52-154">Pożywkę</span><span class="sxs-lookup"><span data-stu-id="08a52-154">Medium</span></span>
- <span data-ttu-id="08a52-155">Większej</span><span class="sxs-lookup"><span data-stu-id="08a52-155">Large</span></span>
- <span data-ttu-id="08a52-156">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="08a52-156">ExtraLarge</span></span>
- <span data-ttu-id="08a52-157">A5</span><span class="sxs-lookup"><span data-stu-id="08a52-157">A5</span></span>
- <span data-ttu-id="08a52-158">A6</span><span class="sxs-lookup"><span data-stu-id="08a52-158">A6</span></span>
- <span data-ttu-id="08a52-159">A7</span><span class="sxs-lookup"><span data-stu-id="08a52-159">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08a52-160">-SmallIconName</span><span class="sxs-lookup"><span data-stu-id="08a52-160">-SmallIconName</span></span>
<span data-ttu-id="08a52-161">Określa małą nazwę ikony dla systemu operacyjnego lub obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="08a52-161">Specifies the small icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="08a52-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08a52-162">CommonParameters</span></span>
<span data-ttu-id="08a52-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08a52-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08a52-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08a52-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08a52-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08a52-165">INPUTS</span></span>

## <span data-ttu-id="08a52-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08a52-166">OUTPUTS</span></span>

### <span data-ttu-id="08a52-167">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="08a52-167">OSImageContext</span></span>

## <span data-ttu-id="08a52-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08a52-168">NOTES</span></span>

## <span data-ttu-id="08a52-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08a52-169">RELATED LINKS</span></span>

[<span data-ttu-id="08a52-170">Dodaj-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="08a52-170">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="08a52-171">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="08a52-171">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="08a52-172">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="08a52-172">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="08a52-173">Zapisz — AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="08a52-173">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="08a52-174">Nowe — AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="08a52-174">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="08a52-175">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="08a52-175">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="08a52-176">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="08a52-176">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


