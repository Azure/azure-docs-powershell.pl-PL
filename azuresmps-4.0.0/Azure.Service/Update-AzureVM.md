---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8DC10708-09CE-449C-BE20-1E9E49CCE08A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55d9879d6e6768bf3ad409c84a4fc1052d58d8b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054979"
---
# <span data-ttu-id="eddbe-101">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="eddbe-101">Update-AzureVM</span></span>

## <span data-ttu-id="eddbe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eddbe-102">SYNOPSIS</span></span>
<span data-ttu-id="eddbe-103">Modyfikuje konfigurację maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eddbe-103">Modifies the configuration of an Azure virtual machine.</span></span>

## <span data-ttu-id="eddbe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eddbe-104">SYNTAX</span></span>

```
Update-AzureVM [-Name] <String> -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eddbe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eddbe-105">DESCRIPTION</span></span>
<span data-ttu-id="eddbe-106">Polecenie cmdlet **Update-AzureVM** akceptuje informacje dotyczące aktualizacji określonej maszyny wirtualnej i inicjuje aktualizację.</span><span class="sxs-lookup"><span data-stu-id="eddbe-106">The **Update-AzureVM** cmdlet accepts update information for the specified virtual machine and initiates the update.</span></span>
<span data-ttu-id="eddbe-107">Możesz dodać lub usunąć dyski danych, zmodyfikować tryb pamięci podręcznej danych lub dysków z systemem operacyjnym, zmienić punkty końcowe sieci lub zmienić rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eddbe-107">You can add or remove data disks, modify the cache mode of data or operating system disks, change the network endpoints, or change the size of the virtual machine.</span></span>

## <span data-ttu-id="eddbe-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eddbe-108">EXAMPLES</span></span>

### <span data-ttu-id="eddbe-109">Przykład 1: aktualizowanie rozmiaru maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="eddbe-109">Example 1: Update the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" | Set-AzureVMSize -InstanceSize "Medium" | Update-AzureVM
```

<span data-ttu-id="eddbe-110">To polecenie powoduje zmianę rozmiaru maszyny wirtualnej o nazwie VirtualMachine04, uruchomionej w usłudze o nazwie ContosoService03, na Oredni.</span><span class="sxs-lookup"><span data-stu-id="eddbe-110">This command changes the size of the virtual machine named VirtualMachine04, running in the service named ContosoService03, to Medium.</span></span>

### <span data-ttu-id="eddbe-111">Przykład 2: Dodawanie dysku danych do maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="eddbe-111">Example 2: Add a data disk to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine05" | Add-AzureDataDisk -CreateNew -MediaLocation "https://ContosoStore1.blob.core.azure.com/vhds/Disk22.vhd" -DiskSizeInGB 128 -DiskLabel "Data-128" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="eddbe-112">To polecenie dodaje nowy dysk danych do maszyny wirtualnej o nazwie VirtualMachine05, uruchomionej w usłudze o nazwie ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="eddbe-112">This command adds a new data disk to the virtual machine named VirtualMachine05, running in the service named ContosoService03.</span></span>

## <span data-ttu-id="eddbe-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eddbe-113">PARAMETERS</span></span>

### <span data-ttu-id="eddbe-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="eddbe-114">-InformationAction</span></span>
<span data-ttu-id="eddbe-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="eddbe-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eddbe-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="eddbe-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eddbe-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="eddbe-117">Continue</span></span>
- <span data-ttu-id="eddbe-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="eddbe-118">Ignore</span></span>
- <span data-ttu-id="eddbe-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="eddbe-119">Inquire</span></span>
- <span data-ttu-id="eddbe-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eddbe-120">SilentlyContinue</span></span>
- <span data-ttu-id="eddbe-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="eddbe-121">Stop</span></span>
- <span data-ttu-id="eddbe-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="eddbe-122">Suspend</span></span>

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

### <span data-ttu-id="eddbe-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eddbe-123">-InformationVariable</span></span>
<span data-ttu-id="eddbe-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="eddbe-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="eddbe-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eddbe-125">-Name</span></span>
<span data-ttu-id="eddbe-126">Określa nazwę maszyny wirtualnej do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="eddbe-126">Specifies the name of the virtual machine to update.</span></span>

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

### <span data-ttu-id="eddbe-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="eddbe-127">-Profile</span></span>
<span data-ttu-id="eddbe-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eddbe-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eddbe-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="eddbe-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eddbe-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="eddbe-130">-ServiceName</span></span>
<span data-ttu-id="eddbe-131">Określa nazwę usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eddbe-131">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="eddbe-132">-VM</span><span class="sxs-lookup"><span data-stu-id="eddbe-132">-VM</span></span>
<span data-ttu-id="eddbe-133">Określa obiekt maszyny wirtualnej zawierający zaktualizowane ustawienia.</span><span class="sxs-lookup"><span data-stu-id="eddbe-133">Specifies the virtual machine object that includes updated settings.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eddbe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eddbe-134">CommonParameters</span></span>
<span data-ttu-id="eddbe-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eddbe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eddbe-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eddbe-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eddbe-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eddbe-137">INPUTS</span></span>

## <span data-ttu-id="eddbe-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eddbe-138">OUTPUTS</span></span>

## <span data-ttu-id="eddbe-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eddbe-139">NOTES</span></span>

## <span data-ttu-id="eddbe-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eddbe-140">RELATED LINKS</span></span>

[<span data-ttu-id="eddbe-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="eddbe-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="eddbe-142">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="eddbe-142">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="eddbe-143">Nowe — AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="eddbe-143">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="eddbe-144">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="eddbe-144">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="eddbe-145">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="eddbe-145">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="eddbe-146">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="eddbe-146">Set-AzureVMSize</span></span>](./Set-AzureVMSize.md)

[<span data-ttu-id="eddbe-147">Start — AzureVM</span><span class="sxs-lookup"><span data-stu-id="eddbe-147">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="eddbe-148">Zatrzymaj — AzureVM</span><span class="sxs-lookup"><span data-stu-id="eddbe-148">Stop-AzureVM</span></span>](./Stop-AzureVM.md)


