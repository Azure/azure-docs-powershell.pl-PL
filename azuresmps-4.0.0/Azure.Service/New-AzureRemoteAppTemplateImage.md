---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DBC4A0B8-A34A-47AC-930B-EFE23A95A216
online version: ''
schema: 2.0.0
ms.openlocfilehash: 178349299767eefb1d89c31a0199f53373bd2ae2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054961"
---
# <span data-ttu-id="1a187-101">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1a187-101">New-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="1a187-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a187-102">SYNOPSIS</span></span>
<span data-ttu-id="1a187-103">Umożliwia przekazywanie lub importowanie obrazu szablonu usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="1a187-103">Uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="1a187-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a187-104">SYNTAX</span></span>

### <span data-ttu-id="1a187-105">UploadLocalVhd (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1a187-105">UploadLocalVhd (Default)</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> [-Path] <String> [-Resume]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1a187-106">AzureVmUpload</span><span class="sxs-lookup"><span data-stu-id="1a187-106">AzureVmUpload</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> -AzureVmImageName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1a187-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1a187-107">DESCRIPTION</span></span>
<span data-ttu-id="1a187-108">Polecenie cmdlet **New-AzureRemoteAppTemplateImage** umożliwia przekazywanie lub importowanie obrazu szablonu usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="1a187-108">The **New-AzureRemoteAppTemplateImage** cmdlet uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="1a187-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a187-109">EXAMPLES</span></span>

### <span data-ttu-id="1a187-110">Przykład 1: przekazywanie pliku VHD w celu utworzenia obrazu szablonu</span><span class="sxs-lookup"><span data-stu-id="1a187-110">Example 1: Upload a VHD file to create a template image</span></span>
```
PS C:\> New-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -Location "North Europe" -Path "C:\RemoteAppImages\ContosoApps.vhd"
```

<span data-ttu-id="1a187-111">To polecenie umożliwia przekazywanie C:\RemoteAppImages\ContosoApps.vhd w celu utworzenia obrazu szablonu o nazwie ContosoApps w centrum danych w Europie Europy Północnej.</span><span class="sxs-lookup"><span data-stu-id="1a187-111">This command uploads C:\RemoteAppImages\ContosoApps.vhd to create a template image named ContosoApps in the North Europe data center.</span></span>

## <span data-ttu-id="1a187-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a187-112">PARAMETERS</span></span>

### <span data-ttu-id="1a187-113">-AzureVmImageName</span><span class="sxs-lookup"><span data-stu-id="1a187-113">-AzureVmImageName</span></span>
<span data-ttu-id="1a187-114">Określa nazwę maszyny wirtualnej platformy Azure, która ma być używana jako obraz szablonu.</span><span class="sxs-lookup"><span data-stu-id="1a187-114">Specifies the name of an Azure virtual machine to use as a template image.</span></span>

```yaml
Type: String
Parameter Sets: AzureVmUpload
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a187-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="1a187-115">-ImageName</span></span>
<span data-ttu-id="1a187-116">Określa nazwę obrazu szablonu usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="1a187-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a187-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1a187-117">-Location</span></span>
<span data-ttu-id="1a187-118">Określa obszar Azure obrazu szablonu.</span><span class="sxs-lookup"><span data-stu-id="1a187-118">Specifies the Azure region of the template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a187-119">-Path</span><span class="sxs-lookup"><span data-stu-id="1a187-119">-Path</span></span>
<span data-ttu-id="1a187-120">Określa ścieżkę pliku obrazu szablonu.</span><span class="sxs-lookup"><span data-stu-id="1a187-120">Specifies the file path of the template image.</span></span>

```yaml
Type: String
Parameter Sets: UploadLocalVhd
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a187-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="1a187-121">-Profile</span></span>
<span data-ttu-id="1a187-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a187-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a187-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1a187-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a187-124">-Życiorys</span><span class="sxs-lookup"><span data-stu-id="1a187-124">-Resume</span></span>
<span data-ttu-id="1a187-125">Wskazuje, że to polecenie cmdlet zostanie wznowione, jeśli przekazywanie obrazu szablonu zostanie przerwane.</span><span class="sxs-lookup"><span data-stu-id="1a187-125">Indicates that this cmdlet resumes if the upload of a template image is interrupted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UploadLocalVhd
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a187-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a187-126">CommonParameters</span></span>
<span data-ttu-id="1a187-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a187-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a187-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a187-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a187-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a187-129">INPUTS</span></span>

## <span data-ttu-id="1a187-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a187-130">OUTPUTS</span></span>

## <span data-ttu-id="1a187-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a187-131">NOTES</span></span>

## <span data-ttu-id="1a187-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a187-132">RELATED LINKS</span></span>

[<span data-ttu-id="1a187-133">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1a187-133">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="1a187-134">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1a187-134">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="1a187-135">Zmień nazwę — AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1a187-135">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


