---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 455DB2C0-08A0-4D62-B8EE-7C3DB9AD8A8C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85040f07914aef02355f69baab093c75ce7e4afd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054482"
---
# <span data-ttu-id="665e5-101">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="665e5-101">Remove-AzureVM</span></span>

## <span data-ttu-id="665e5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="665e5-102">SYNOPSIS</span></span>
<span data-ttu-id="665e5-103">Usuwa maszynę wirtualną platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="665e5-103">Removes an Azure virtual machine.</span></span>

## <span data-ttu-id="665e5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="665e5-104">SYNTAX</span></span>

```
Remove-AzureVM [-Name] <String> [-DeleteVHD] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="665e5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="665e5-105">DESCRIPTION</span></span>
<span data-ttu-id="665e5-106">Polecenie cmdlet **Remove-AzureVM** umożliwia usunięcie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="665e5-106">The **Remove-AzureVM** cmdlet deletes an Azure virtual machine.</span></span>
<span data-ttu-id="665e5-107">Ten proces nie powoduje usunięcia podstawowych plików VHD dysków zainstalowanych na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="665e5-107">This process does not delete the underlying .vhd files of the disks mounted on that virtual machine.</span></span>

## <span data-ttu-id="665e5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="665e5-108">EXAMPLES</span></span>

### <span data-ttu-id="665e5-109">Przykład 1: usuwanie maszyny wirtualnej z usługi</span><span class="sxs-lookup"><span data-stu-id="665e5-109">Example 1: Remove a virtual machine from a service</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine03"
```

<span data-ttu-id="665e5-110">To polecenie umożliwia usunięcie maszyny wirtualnej o nazwie VirtualMachine03 uruchomionej w usłudze ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="665e5-110">This command removes the virtual machine named VirtualMachine03 that runs in the ContosoService03 service.</span></span>

### <span data-ttu-id="665e5-111">Przykład 2: usunięcie maszyny wirtualnej i usuwanie plików VHD</span><span class="sxs-lookup"><span data-stu-id="665e5-111">Example 2: Remove a virtual machine and delete the .vhd files</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" -DeleteVHD
```

<span data-ttu-id="665e5-112">To polecenie umożliwia usunięcie maszyny wirtualnej VirtualMachine04 działającej w usłudze ContosoService03 i określenie, że pliki VHD mają być usuwane przy użyciu parametru *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="665e5-112">This command removes the VirtualMachine04 virtual machine that runs in the ContosoService03 service, and specifies to remove the .vhd files using the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="665e5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="665e5-113">PARAMETERS</span></span>

### <span data-ttu-id="665e5-114">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="665e5-114">-DeleteVHD</span></span>
<span data-ttu-id="665e5-115">Określa, czy to polecenie cmdlet umożliwia usunięcie maszyny wirtualnej i obiektów BLOB dysku źródłowego.</span><span class="sxs-lookup"><span data-stu-id="665e5-115">Specifies whether this cmdlet removes the virtual machine and the underlying disk blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="665e5-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="665e5-116">-InformationAction</span></span>
<span data-ttu-id="665e5-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="665e5-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="665e5-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="665e5-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="665e5-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="665e5-119">Continue</span></span>
- <span data-ttu-id="665e5-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="665e5-120">Ignore</span></span>
- <span data-ttu-id="665e5-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="665e5-121">Inquire</span></span>
- <span data-ttu-id="665e5-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="665e5-122">SilentlyContinue</span></span>
- <span data-ttu-id="665e5-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="665e5-123">Stop</span></span>
- <span data-ttu-id="665e5-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="665e5-124">Suspend</span></span>

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

### <span data-ttu-id="665e5-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="665e5-125">-InformationVariable</span></span>
<span data-ttu-id="665e5-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="665e5-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="665e5-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="665e5-127">-Name</span></span>
<span data-ttu-id="665e5-128">Określa nazwę usuniętej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="665e5-128">Specifies the name of the virtual machine being removed.</span></span>

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

### <span data-ttu-id="665e5-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="665e5-129">-Profile</span></span>
<span data-ttu-id="665e5-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="665e5-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="665e5-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="665e5-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="665e5-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="665e5-132">-ServiceName</span></span>
<span data-ttu-id="665e5-133">Określa nazwę usługi platformy Azure, z której maszyna wirtualna jest usuwana.</span><span class="sxs-lookup"><span data-stu-id="665e5-133">Specifies the name of the Azure service from which the virtual machine is being removed.</span></span>

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

### <span data-ttu-id="665e5-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="665e5-134">-Confirm</span></span>
<span data-ttu-id="665e5-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="665e5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="665e5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="665e5-136">-WhatIf</span></span>
<span data-ttu-id="665e5-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="665e5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="665e5-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="665e5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="665e5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="665e5-139">CommonParameters</span></span>
<span data-ttu-id="665e5-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="665e5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="665e5-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="665e5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="665e5-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="665e5-142">INPUTS</span></span>

## <span data-ttu-id="665e5-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="665e5-143">OUTPUTS</span></span>

## <span data-ttu-id="665e5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="665e5-144">NOTES</span></span>

## <span data-ttu-id="665e5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="665e5-145">RELATED LINKS</span></span>

[<span data-ttu-id="665e5-146">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="665e5-146">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="665e5-147">Nowe — AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="665e5-147">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="665e5-148">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="665e5-148">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="665e5-149">Start — AzureVM</span><span class="sxs-lookup"><span data-stu-id="665e5-149">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="665e5-150">Zatrzymaj — AzureVM</span><span class="sxs-lookup"><span data-stu-id="665e5-150">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="665e5-151">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="665e5-151">Update-AzureVM</span></span>](./Update-AzureVM.md)


