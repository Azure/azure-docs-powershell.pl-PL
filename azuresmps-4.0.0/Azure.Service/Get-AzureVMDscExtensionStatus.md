---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 19A87B24-C5A6-4505-BB54-973B24BCC68E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821927fc465ed5af048a2f27ed84da8c12b9caa5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055502"
---
# <span data-ttu-id="44325-101">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="44325-101">Get-AzureVMDscExtensionStatus</span></span>

## <span data-ttu-id="44325-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44325-102">SYNOPSIS</span></span>
<span data-ttu-id="44325-103">Pobiera stan rozszerzenia DSC dla wszystkich maszyn wirtualnych wdrożonych w usłudze chmury lub dla konkretnej maszyny wirtualnej w usłudze.</span><span class="sxs-lookup"><span data-stu-id="44325-103">Gets the DSC extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="44325-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44325-104">SYNTAX</span></span>

### <span data-ttu-id="44325-105">GetStatusByServiceAndVMName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="44325-105">GetStatusByServiceAndVMName (Default)</span></span>
```
Get-AzureVMDscExtensionStatus [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="44325-106">GetStatusByVM</span><span class="sxs-lookup"><span data-stu-id="44325-106">GetStatusByVM</span></span>
```
Get-AzureVMDscExtensionStatus -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="44325-107">Opis</span><span class="sxs-lookup"><span data-stu-id="44325-107">DESCRIPTION</span></span>
<span data-ttu-id="44325-108">Polecenie cmdlet **Get-AzureVMDscExtensionStatus** Pobiera stan rozszerzenia konfiguracji stanu (DSC) dla wszystkich maszyn wirtualnych wdrożonych w usłudze chmury lub dla konkretnej maszyny wirtualnej w usłudze.</span><span class="sxs-lookup"><span data-stu-id="44325-108">The **Get-AzureVMDscExtensionStatus** cmdlet gets the Desired State Configuration (DSC) extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="44325-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44325-109">EXAMPLES</span></span>

### <span data-ttu-id="44325-110">1:1</span><span class="sxs-lookup"><span data-stu-id="44325-110">1:</span></span>
```

```

## <span data-ttu-id="44325-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44325-111">PARAMETERS</span></span>

### <span data-ttu-id="44325-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="44325-112">-InformationAction</span></span>
<span data-ttu-id="44325-113">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="44325-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="44325-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="44325-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44325-115">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="44325-115">Continue</span></span>
- <span data-ttu-id="44325-116">Ignorować</span><span class="sxs-lookup"><span data-stu-id="44325-116">Ignore</span></span>
- <span data-ttu-id="44325-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="44325-117">Inquire</span></span>
- <span data-ttu-id="44325-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="44325-118">SilentlyContinue</span></span>
- <span data-ttu-id="44325-119">Przestaw</span><span class="sxs-lookup"><span data-stu-id="44325-119">Stop</span></span>
- <span data-ttu-id="44325-120">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="44325-120">Suspend</span></span>

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

### <span data-ttu-id="44325-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="44325-121">-InformationVariable</span></span>
<span data-ttu-id="44325-122">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="44325-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="44325-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44325-123">-Name</span></span>
<span data-ttu-id="44325-124">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="44325-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44325-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="44325-125">-Profile</span></span>
<span data-ttu-id="44325-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44325-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44325-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="44325-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44325-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="44325-128">-ServiceName</span></span>
<span data-ttu-id="44325-129">Określa nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="44325-129">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44325-130">-VM</span><span class="sxs-lookup"><span data-stu-id="44325-130">-VM</span></span>
<span data-ttu-id="44325-131">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="44325-131">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: GetStatusByVM
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44325-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44325-132">CommonParameters</span></span>
<span data-ttu-id="44325-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44325-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44325-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44325-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44325-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44325-135">INPUTS</span></span>

## <span data-ttu-id="44325-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44325-136">OUTPUTS</span></span>

### <span data-ttu-id="44325-137">Microsoft. platformy windowsazure. Commands. servicemanagement. IaaS. Extensions. VirtualMachineDscExtensionStatusContext</span><span class="sxs-lookup"><span data-stu-id="44325-137">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionStatusContext</span></span>

## <span data-ttu-id="44325-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44325-138">NOTES</span></span>

## <span data-ttu-id="44325-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44325-139">RELATED LINKS</span></span>

[<span data-ttu-id="44325-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="44325-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="44325-141">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="44325-141">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="44325-142">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="44325-142">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


