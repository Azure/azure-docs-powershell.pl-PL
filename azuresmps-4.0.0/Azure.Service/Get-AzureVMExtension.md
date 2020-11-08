---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7ED074F0-1E9E-40C2-A543-D19A49831DD3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f0b8ca9acfe5a62b002944bd44e11acfcd38ec1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055499"
---
# <span data-ttu-id="2ab22-101">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="2ab22-101">Get-AzureVMExtension</span></span>

## <span data-ttu-id="2ab22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ab22-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab22-103">Pobiera rozszerzenia zasobów zastosowane do maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="2ab22-103">Gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="2ab22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ab22-104">SYNTAX</span></span>

### <span data-ttu-id="2ab22-105">ListByReferenceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2ab22-105">ListByReferenceName (Default)</span></span>
```
Get-AzureVMExtension [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2ab22-106">ListByExtensionName</span><span class="sxs-lookup"><span data-stu-id="2ab22-106">ListByExtensionName</span></span>
```
Get-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ab22-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2ab22-107">DESCRIPTION</span></span>
<span data-ttu-id="2ab22-108">Polecenie cmdlet **Get-AzureVMExtension** umożliwia stosowanie rozszerzeń zasobów na maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="2ab22-108">The **Get-AzureVMExtension** cmdlet gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="2ab22-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ab22-109">EXAMPLES</span></span>

### <span data-ttu-id="2ab22-110">Przykład 1: uzyskiwanie rozszerzeń zasobów zastosowanych do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2ab22-110">Example 1: Get the resource extensions applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName $SVC -Name $VM | Get-AzureVMExtension;
```

<span data-ttu-id="2ab22-111">To polecenie pobiera rozszerzenia zasobów zastosowane do określonej maszyny wirtualnej jako przechowywane w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="2ab22-111">This command gets the resource extensions applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="2ab22-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ab22-112">PARAMETERS</span></span>

### <span data-ttu-id="2ab22-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="2ab22-113">-ExtensionName</span></span>
<span data-ttu-id="2ab22-114">Określa nazwę rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ab22-114">Specifies the virtual machine extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab22-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2ab22-115">-InformationAction</span></span>
<span data-ttu-id="2ab22-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="2ab22-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2ab22-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2ab22-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ab22-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="2ab22-118">Continue</span></span>
- <span data-ttu-id="2ab22-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="2ab22-119">Ignore</span></span>
- <span data-ttu-id="2ab22-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="2ab22-120">Inquire</span></span>
- <span data-ttu-id="2ab22-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2ab22-121">SilentlyContinue</span></span>
- <span data-ttu-id="2ab22-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="2ab22-122">Stop</span></span>
- <span data-ttu-id="2ab22-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="2ab22-123">Suspend</span></span>

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

### <span data-ttu-id="2ab22-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2ab22-124">-InformationVariable</span></span>
<span data-ttu-id="2ab22-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="2ab22-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2ab22-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="2ab22-126">-Profile</span></span>
<span data-ttu-id="2ab22-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ab22-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ab22-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2ab22-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ab22-129">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="2ab22-129">-Publisher</span></span>
<span data-ttu-id="2ab22-130">Określa wydawcę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="2ab22-130">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab22-131">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="2ab22-131">-ReferenceName</span></span>
<span data-ttu-id="2ab22-132">Określa nazwę referencyjną rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="2ab22-132">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByReferenceName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab22-133">-Version</span><span class="sxs-lookup"><span data-stu-id="2ab22-133">-Version</span></span>
<span data-ttu-id="2ab22-134">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="2ab22-134">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ab22-135">-VM</span><span class="sxs-lookup"><span data-stu-id="2ab22-135">-VM</span></span>
<span data-ttu-id="2ab22-136">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ab22-136">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="2ab22-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab22-137">CommonParameters</span></span>
<span data-ttu-id="2ab22-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab22-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab22-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ab22-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab22-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ab22-140">INPUTS</span></span>

## <span data-ttu-id="2ab22-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ab22-141">OUTPUTS</span></span>

## <span data-ttu-id="2ab22-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ab22-142">NOTES</span></span>

## <span data-ttu-id="2ab22-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ab22-143">RELATED LINKS</span></span>

[<span data-ttu-id="2ab22-144">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="2ab22-144">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="2ab22-145">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="2ab22-145">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


