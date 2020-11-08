---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055498"
---
# <span data-ttu-id="f7992-101">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="f7992-101">Get-AzureVMImage</span></span>

## <span data-ttu-id="f7992-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7992-102">SYNOPSIS</span></span>
<span data-ttu-id="f7992-103">Pobiera właściwości jednej lub listy systemów operacyjnych lub obrazów maszyny wirtualnej w repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="f7992-103">Gets the properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>

## <span data-ttu-id="f7992-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7992-104">SYNTAX</span></span>

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f7992-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7992-105">DESCRIPTION</span></span>
<span data-ttu-id="f7992-106">Polecenie cmdlet **Get-AzureVMImage** pobiera właściwości jednej lub listy systemów operacyjnych lub obrazów maszyny wirtualnej w repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="f7992-106">The **Get-AzureVMImage** cmdlet gets properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>
<span data-ttu-id="f7992-107">Polecenie cmdlet zwraca informacje dotyczące wszystkich obrazów w repozytorium lub informacje o określonym obrazie, jeśli jego nazwa obrazu jest podana.</span><span class="sxs-lookup"><span data-stu-id="f7992-107">The cmdlet returns information for all images in the repository, or about a specific image if its image name is provided.</span></span>

## <span data-ttu-id="f7992-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7992-108">EXAMPLES</span></span>

### <span data-ttu-id="f7992-109">Przykład 1: uzyskiwanie określonego obiektu obrazu z bieżącego repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="f7992-109">Example 1: Get a specific image object from the current image repository.</span></span>
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

<span data-ttu-id="f7992-110">To polecenie pobiera obiekt obrazu o nazwie Image001 z bieżącego repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="f7992-110">This command gets the image object named Image001 from the current image repository.</span></span>

### <span data-ttu-id="f7992-111">Przykład 2: pobieranie wszystkich obrazów z bieżącego repozytorium obrazów</span><span class="sxs-lookup"><span data-stu-id="f7992-111">Example 2: Get all images from the current image repository</span></span>
```
PS C:\> Get-AzureVMImage
```

<span data-ttu-id="f7992-112">To polecenie pobiera wszystkie obrazy z bieżącego repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="f7992-112">This command retrieves all the images from the current image repository.</span></span>

### <span data-ttu-id="f7992-113">Przykład 3: Ustawianie kontekstu subskrypcji, a następnie uzyskiwanie wszystkich obrazów</span><span class="sxs-lookup"><span data-stu-id="f7992-113">Example 3: Set the subscription context and then get all the images</span></span>
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

<span data-ttu-id="f7992-114">To polecenie ustawia kontekst abonamentu, a następnie pobiera wszystkie obrazy z repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="f7992-114">This command sets the subscription context and then retrieves all the images from the image repository.</span></span>

## <span data-ttu-id="f7992-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7992-115">PARAMETERS</span></span>

### <span data-ttu-id="f7992-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="f7992-116">-ImageName</span></span>
<span data-ttu-id="f7992-117">Określa nazwę obrazu systemu operacyjnego lub maszyny wirtualnej w repozytorium obrazów.</span><span class="sxs-lookup"><span data-stu-id="f7992-117">Specifies the name of the operating system or virtual machine image in the image repository.</span></span>
<span data-ttu-id="f7992-118">Jeśli nie podano tego parametru, zostaną zwrócone wszystkie obrazy.</span><span class="sxs-lookup"><span data-stu-id="f7992-118">If you do not specify this parameter, all the images are returned.</span></span>

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

### <span data-ttu-id="f7992-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f7992-119">-InformationAction</span></span>
<span data-ttu-id="f7992-120">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="f7992-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f7992-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f7992-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7992-122">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="f7992-122">Continue</span></span>
- <span data-ttu-id="f7992-123">Ignorować</span><span class="sxs-lookup"><span data-stu-id="f7992-123">Ignore</span></span>
- <span data-ttu-id="f7992-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="f7992-124">Inquire</span></span>
- <span data-ttu-id="f7992-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f7992-125">SilentlyContinue</span></span>
- <span data-ttu-id="f7992-126">Przestaw</span><span class="sxs-lookup"><span data-stu-id="f7992-126">Stop</span></span>
- <span data-ttu-id="f7992-127">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="f7992-127">Suspend</span></span>

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

### <span data-ttu-id="f7992-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f7992-128">-InformationVariable</span></span>
<span data-ttu-id="f7992-129">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="f7992-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f7992-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="f7992-130">-Profile</span></span>
<span data-ttu-id="f7992-131">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7992-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f7992-132">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f7992-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f7992-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7992-133">CommonParameters</span></span>
<span data-ttu-id="f7992-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7992-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7992-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7992-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7992-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7992-136">INPUTS</span></span>

## <span data-ttu-id="f7992-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7992-137">OUTPUTS</span></span>

## <span data-ttu-id="f7992-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7992-138">NOTES</span></span>

## <span data-ttu-id="f7992-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7992-139">RELATED LINKS</span></span>

[<span data-ttu-id="f7992-140">Dodaj-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="f7992-140">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="f7992-141">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="f7992-141">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="f7992-142">Zapisz — AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="f7992-142">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="f7992-143">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="f7992-143">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


