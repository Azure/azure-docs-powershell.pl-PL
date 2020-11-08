---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 40AE50AA-6807-4481-8B77-A038914D462E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a4c6997a7ae70a72a21800cce1d4f5f32475a85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055413"
---
# <span data-ttu-id="67396-101">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="67396-101">Remove-AzureVMDscExtension</span></span>

## <span data-ttu-id="67396-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67396-102">SYNOPSIS</span></span>
<span data-ttu-id="67396-103">Usuwa rozszerzenie Azure DSC z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="67396-103">Removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="67396-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67396-104">SYNTAX</span></span>

```
Remove-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67396-105">Opis</span><span class="sxs-lookup"><span data-stu-id="67396-105">DESCRIPTION</span></span>
<span data-ttu-id="67396-106">Polecenie cmdlet **Remove-AzureVMDscExtension** usuwa rozszerzenie Azure DSC z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="67396-106">The **Remove-AzureVMDscExtension** cmdlet removes an Azure DSC extension from a virtual machine.</span></span>
<span data-ttu-id="67396-107">Wyniki tego polecenia cmdlet muszą być przekazywane do polecenia cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="67396-107">The output of this cmdlet needs to be piped to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="67396-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67396-108">EXAMPLES</span></span>

### <span data-ttu-id="67396-109">Przykład 1: Usuwanie rozszerzenia DSC z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="67396-109">Example 1: Remove a DSC extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDscExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="67396-110">To polecenie usuwa rozszerzenie Azure DSC z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="67396-110">This command removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="67396-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67396-111">PARAMETERS</span></span>

### <span data-ttu-id="67396-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="67396-112">-InformationAction</span></span>
<span data-ttu-id="67396-113">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="67396-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="67396-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="67396-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67396-115">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="67396-115">Continue</span></span>
- <span data-ttu-id="67396-116">Ignorować</span><span class="sxs-lookup"><span data-stu-id="67396-116">Ignore</span></span>
- <span data-ttu-id="67396-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="67396-117">Inquire</span></span>
- <span data-ttu-id="67396-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="67396-118">SilentlyContinue</span></span>
- <span data-ttu-id="67396-119">Przestaw</span><span class="sxs-lookup"><span data-stu-id="67396-119">Stop</span></span>
- <span data-ttu-id="67396-120">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="67396-120">Suspend</span></span>

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

### <span data-ttu-id="67396-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="67396-121">-InformationVariable</span></span>
<span data-ttu-id="67396-122">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="67396-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="67396-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="67396-123">-Profile</span></span>
<span data-ttu-id="67396-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67396-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67396-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="67396-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="67396-126">-VM</span><span class="sxs-lookup"><span data-stu-id="67396-126">-VM</span></span>
<span data-ttu-id="67396-127">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="67396-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="67396-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67396-128">-Confirm</span></span>
<span data-ttu-id="67396-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67396-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67396-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67396-130">-WhatIf</span></span>
<span data-ttu-id="67396-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67396-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67396-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="67396-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67396-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67396-133">CommonParameters</span></span>
<span data-ttu-id="67396-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67396-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67396-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67396-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67396-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67396-136">INPUTS</span></span>

## <span data-ttu-id="67396-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67396-137">OUTPUTS</span></span>

## <span data-ttu-id="67396-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67396-138">NOTES</span></span>

## <span data-ttu-id="67396-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67396-139">RELATED LINKS</span></span>

[<span data-ttu-id="67396-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="67396-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="67396-141">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="67396-141">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="67396-142">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="67396-142">Update-AzureVM</span></span>](./Update-AzureVM.md)


