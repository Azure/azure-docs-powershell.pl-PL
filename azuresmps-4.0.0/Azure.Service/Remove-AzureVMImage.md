---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055420"
---
# <span data-ttu-id="58a29-101">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="58a29-101">Remove-AzureVMImage</span></span>

## <span data-ttu-id="58a29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58a29-102">SYNOPSIS</span></span>
<span data-ttu-id="58a29-103">Usuwa obraz systemu operacyjnego z repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="58a29-103">Removes an operating system image from the image repository.</span></span>

## <span data-ttu-id="58a29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58a29-104">SYNTAX</span></span>

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="58a29-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58a29-105">DESCRIPTION</span></span>
<span data-ttu-id="58a29-106">Polecenie cmdlet **Remove-AzureVMImage** usuwa obraz systemu operacyjnego z repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="58a29-106">The **Remove-AzureVMImage** cmdlet removes an operating system image from the image repository.</span></span>
<span data-ttu-id="58a29-107">Domyślnie to polecenie cmdlet nie usuwa skojarzonego obiektu BLOB fizycznego obrazu z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="58a29-107">By default, this cmdlet does not delete the associated physical image blob from the storage account.</span></span>
<span data-ttu-id="58a29-108">Aby usunąć skojarzony wirtualny dysk twardy (VHD), użyj parametru **DeleteVHD** .</span><span class="sxs-lookup"><span data-stu-id="58a29-108">To delete the associated virtual hard drive (VHD), use the **DeleteVHD** parameter.</span></span>

## <span data-ttu-id="58a29-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58a29-109">EXAMPLES</span></span>

### <span data-ttu-id="58a29-110">Przykład 1. Usuwanie obrazu z repozytorium obrazów</span><span class="sxs-lookup"><span data-stu-id="58a29-110">Example 1: Remove an image from the image repository</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

<span data-ttu-id="58a29-111">To polecenie usuwa obraz o nazwie Image001 z repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="58a29-111">This command removes the image named Image001 from the image repository.</span></span>

### <span data-ttu-id="58a29-112">Przykład 2: Usuwanie obrazu z repozytorium obrazów, a także wirtualnego dysku twardego</span><span class="sxs-lookup"><span data-stu-id="58a29-112">Example 2: Remove an image from the image repository and also the VHD</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

<span data-ttu-id="58a29-113">To polecenie powoduje usunięcie obrazu o nazwie Image001 z repozytorium obrazów, a także usunięcie fizycznego obrazu VHD z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="58a29-113">This command removes the image named Image001 from the image repository and also deletes the physical VHD image from the storage account.</span></span>

### <span data-ttu-id="58a29-114">Przykład 3: Ustawianie kontekstu subskrypcji, a następnie Usuwanie wszystkich obrazów</span><span class="sxs-lookup"><span data-stu-id="58a29-114">Example 3: Set a subscription context and then remove all the images</span></span>
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

<span data-ttu-id="58a29-115">To polecenie ustawia kontekst abonamentu, a następnie usuwa wszystkie obrazy z repozytorium obrazów, którego etykieta zawiera nazwę beta.</span><span class="sxs-lookup"><span data-stu-id="58a29-115">This command sets the subscription context and then removes all the images from the image repository whose Label includes the name Beta.</span></span>

## <span data-ttu-id="58a29-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58a29-116">PARAMETERS</span></span>

### <span data-ttu-id="58a29-117">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="58a29-117">-DeleteVHD</span></span>
<span data-ttu-id="58a29-118">Wskazuje, że to polecenie cmdlet usuwa obiekt BLOB obrazu fizycznego dysku VHD z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="58a29-118">Indicates that this cmdlet deletes the physical VHD image blob from the storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58a29-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="58a29-119">-ImageName</span></span>
<span data-ttu-id="58a29-120">Określa obraz systemu operacyjnego lub maszyny wirtualnej do usunięcia z repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="58a29-120">Specifies the operating system or virtual machine image to remove from the image repository.</span></span>

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

### <span data-ttu-id="58a29-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="58a29-121">-InformationAction</span></span>
<span data-ttu-id="58a29-122">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="58a29-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="58a29-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="58a29-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="58a29-124">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="58a29-124">Continue</span></span>
- <span data-ttu-id="58a29-125">Ignorować</span><span class="sxs-lookup"><span data-stu-id="58a29-125">Ignore</span></span>
- <span data-ttu-id="58a29-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="58a29-126">Inquire</span></span>
- <span data-ttu-id="58a29-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="58a29-127">SilentlyContinue</span></span>
- <span data-ttu-id="58a29-128">Przestaw</span><span class="sxs-lookup"><span data-stu-id="58a29-128">Stop</span></span>
- <span data-ttu-id="58a29-129">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="58a29-129">Suspend</span></span>

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

### <span data-ttu-id="58a29-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="58a29-130">-InformationVariable</span></span>
<span data-ttu-id="58a29-131">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="58a29-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="58a29-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="58a29-132">-Profile</span></span>
<span data-ttu-id="58a29-133">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58a29-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="58a29-134">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="58a29-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="58a29-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a29-135">CommonParameters</span></span>
<span data-ttu-id="58a29-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58a29-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a29-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58a29-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a29-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58a29-138">INPUTS</span></span>

## <span data-ttu-id="58a29-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58a29-139">OUTPUTS</span></span>

## <span data-ttu-id="58a29-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58a29-140">NOTES</span></span>

## <span data-ttu-id="58a29-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58a29-141">RELATED LINKS</span></span>

[<span data-ttu-id="58a29-142">Dodaj-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="58a29-142">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="58a29-143">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="58a29-143">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="58a29-144">Zapisz — AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="58a29-144">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="58a29-145">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="58a29-145">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


