---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A1CE31E-0158-441E-BC2D-B5D21C9D9421
online version: ''
schema: 2.0.0
ms.openlocfilehash: a956aa7eaf383b0cf5cdb20b39d2f6b54e292f92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054417"
---
# <span data-ttu-id="e2139-101">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="e2139-101">Save-AzureVMImage</span></span>

## <span data-ttu-id="e2139-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2139-102">SYNOPSIS</span></span>
<span data-ttu-id="e2139-103">Przechwytywanie i zapisywanie obrazu zatrzymanej maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2139-103">Captures and saves the image of a stopped Azure virtual machine.</span></span>

## <span data-ttu-id="e2139-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2139-104">SYNTAX</span></span>

```
Save-AzureVMImage [-ServiceName] <String> [-Name] <String> [-ImageName] <String> [[-ImageLabel] <String>]
 [[-OSState] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e2139-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e2139-105">DESCRIPTION</span></span>
<span data-ttu-id="e2139-106">Polecenie cmdlet **Save-AzureVMImage** umożliwia przechwycenie i zapisanie obrazu zatrzymanej maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2139-106">The **Save-AzureVMImage** cmdlet captures and saves the image of a stopped Azure virtual machine.</span></span>
<span data-ttu-id="e2139-107">W przypadku maszyn wirtualnych systemu Windows uruchom narzędzie Sysprep, aby przygotować obraz przed jego przechwyceniem.</span><span class="sxs-lookup"><span data-stu-id="e2139-107">For Windows virtual machines, run the Sysprep tool to prepare the image before it is captured.</span></span>
<span data-ttu-id="e2139-108">Po przechwyceniu obrazu maszyna wirtualna zostanie usunięta.</span><span class="sxs-lookup"><span data-stu-id="e2139-108">After the image is captured, the virtual machine is deleted.</span></span>

## <span data-ttu-id="e2139-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2139-109">EXAMPLES</span></span>

### <span data-ttu-id="e2139-110">Przykład 1. Zapisz istniejącą maszynę wirtualną, a następnie usuń ją z wdrożenia</span><span class="sxs-lookup"><span data-stu-id="e2139-110">Example 1: Save an existing virtual machine and then delete it from a deployment</span></span>
```
PS C:\> Save-AzureVMImage -ServiceName "MyService" -Name "MyVM" -NewImageName "MyBaseImage" -NewImageLabel "MyBaseVM"
```

<span data-ttu-id="e2139-111">To polecenie umożliwia przechwycenie istniejącej maszyny wirtualnej i usunięcie jej z wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e2139-111">This command captures an existing virtual machine and deletes it from the deployment.</span></span>

## <span data-ttu-id="e2139-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2139-112">PARAMETERS</span></span>

### <span data-ttu-id="e2139-113">-ImageLabel</span><span class="sxs-lookup"><span data-stu-id="e2139-113">-ImageLabel</span></span>
<span data-ttu-id="e2139-114">Określa etykietę obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e2139-114">Specifies the label of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageLabel

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2139-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e2139-115">-ImageName</span></span>
<span data-ttu-id="e2139-116">Określa nazwę obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e2139-116">Specifies the name of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2139-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e2139-117">-InformationAction</span></span>
<span data-ttu-id="e2139-118">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="e2139-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e2139-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e2139-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2139-120">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="e2139-120">Continue</span></span>
- <span data-ttu-id="e2139-121">Ignorować</span><span class="sxs-lookup"><span data-stu-id="e2139-121">Ignore</span></span>
- <span data-ttu-id="e2139-122">Inquire</span><span class="sxs-lookup"><span data-stu-id="e2139-122">Inquire</span></span>
- <span data-ttu-id="e2139-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e2139-123">SilentlyContinue</span></span>
- <span data-ttu-id="e2139-124">Przestaw</span><span class="sxs-lookup"><span data-stu-id="e2139-124">Stop</span></span>
- <span data-ttu-id="e2139-125">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="e2139-125">Suspend</span></span>

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

### <span data-ttu-id="e2139-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e2139-126">-InformationVariable</span></span>
<span data-ttu-id="e2139-127">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="e2139-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e2139-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2139-128">-Name</span></span>
<span data-ttu-id="e2139-129">Określa nazwę źródłowej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e2139-129">Specifies the name of the source virtual machine.</span></span>

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

### <span data-ttu-id="e2139-130">-OSState</span><span class="sxs-lookup"><span data-stu-id="e2139-130">-OSState</span></span>
<span data-ttu-id="e2139-131">Określa stan systemu operacyjnego obrazu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e2139-131">Specifies the operation system state for the virtual machine image.</span></span>
<span data-ttu-id="e2139-132">Użyj tego parametru, jeśli zamierzasz przechwycić obraz maszyny wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e2139-132">Use this parameter if you intend to capture a virtual machine image to Azure.</span></span>

<span data-ttu-id="e2139-133">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e2139-133">Valid values are:</span></span>

- <span data-ttu-id="e2139-134">Uogólniony</span><span class="sxs-lookup"><span data-stu-id="e2139-134">Generalized</span></span>
- <span data-ttu-id="e2139-135">Przeznaczona</span><span class="sxs-lookup"><span data-stu-id="e2139-135">Specialized</span></span>

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

### <span data-ttu-id="e2139-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="e2139-136">-Profile</span></span>
<span data-ttu-id="e2139-137">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2139-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2139-138">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e2139-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2139-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e2139-139">-ServiceName</span></span>
<span data-ttu-id="e2139-140">Określa nazwę usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2139-140">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="e2139-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2139-141">CommonParameters</span></span>
<span data-ttu-id="e2139-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2139-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2139-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2139-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2139-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2139-144">INPUTS</span></span>

## <span data-ttu-id="e2139-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2139-145">OUTPUTS</span></span>

## <span data-ttu-id="e2139-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2139-146">NOTES</span></span>

## <span data-ttu-id="e2139-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2139-147">RELATED LINKS</span></span>

[<span data-ttu-id="e2139-148">Dodaj-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="e2139-148">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="e2139-149">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="e2139-149">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="e2139-150">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="e2139-150">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="e2139-151">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="e2139-151">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


