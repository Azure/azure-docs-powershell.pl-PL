---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 596B8A6F-D3C2-4170-BCD7-B7A1CDB656D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee767e1ba4c5008837e7cef98aafa4017465829
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055039"
---
# <span data-ttu-id="80b66-101">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="80b66-101">Restart-AzureVM</span></span>

## <span data-ttu-id="80b66-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80b66-102">SYNOPSIS</span></span>
<span data-ttu-id="80b66-103">Ponowne uruchamianie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80b66-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="80b66-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80b66-104">SYNTAX</span></span>

### <span data-ttu-id="80b66-105">RestartByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="80b66-105">RestartByName (Default)</span></span>
```
Restart-AzureVM [-Name] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80b66-106">RedeployByName</span><span class="sxs-lookup"><span data-stu-id="80b66-106">RedeployByName</span></span>
```
Restart-AzureVM [-Name] <String> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80b66-107">InitiateMaintenanceByName</span><span class="sxs-lookup"><span data-stu-id="80b66-107">InitiateMaintenanceByName</span></span>
```
Restart-AzureVM [-Name] <String> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80b66-108">RestartInput</span><span class="sxs-lookup"><span data-stu-id="80b66-108">RestartInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80b66-109">RedeployInput</span><span class="sxs-lookup"><span data-stu-id="80b66-109">RedeployInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80b66-110">InitiateMaintenanceInput</span><span class="sxs-lookup"><span data-stu-id="80b66-110">InitiateMaintenanceInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="80b66-111">Opis</span><span class="sxs-lookup"><span data-stu-id="80b66-111">DESCRIPTION</span></span>
<span data-ttu-id="80b66-112">Polecenie cmdlet **restart-AzureVM** żąda ponownego uruchomienia maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="80b66-112">The **Restart-AzureVM** cmdlet requests a restart of an Azure virtual machine.</span></span>

## <span data-ttu-id="80b66-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80b66-113">EXAMPLES</span></span>

### <span data-ttu-id="80b66-114">Przykład 1: ponowne uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="80b66-114">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureVM -ServiceName "MyService01" -Name "MyVM"
```

<span data-ttu-id="80b66-115">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej VirtualMachine27 uruchomionej w usłudze Azure o nazwie Service01.</span><span class="sxs-lookup"><span data-stu-id="80b66-115">This command restarts the VirtualMachine27 virtual machine running in the Azure service named Service01.</span></span>

### <span data-ttu-id="80b66-116">Przykład 2: ponowne uruchomienie maszyny wirtualnej za pomocą obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="80b66-116">Example 2: Restart a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MyService01" -Name "VirtualMachine27" | Restart-AzureVM
```

<span data-ttu-id="80b66-117">To polecenie pobiera obiekt maszyny wirtualnej z maszyny wirtualnej o nazwie MyVM, a następnie ponownie go uruchamia.</span><span class="sxs-lookup"><span data-stu-id="80b66-117">This command retrieves the virtual machine object for the virtual machine named MyVM and then restarts it.</span></span>

## <span data-ttu-id="80b66-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80b66-118">PARAMETERS</span></span>

### <span data-ttu-id="80b66-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="80b66-119">-InformationAction</span></span>
<span data-ttu-id="80b66-120">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="80b66-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="80b66-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="80b66-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80b66-122">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="80b66-122">Continue</span></span>
- <span data-ttu-id="80b66-123">Ignorować</span><span class="sxs-lookup"><span data-stu-id="80b66-123">Ignore</span></span>
- <span data-ttu-id="80b66-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="80b66-124">Inquire</span></span>
- <span data-ttu-id="80b66-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="80b66-125">SilentlyContinue</span></span>
- <span data-ttu-id="80b66-126">Przestaw</span><span class="sxs-lookup"><span data-stu-id="80b66-126">Stop</span></span>
- <span data-ttu-id="80b66-127">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="80b66-127">Suspend</span></span>

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

### <span data-ttu-id="80b66-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="80b66-128">-InformationVariable</span></span>
<span data-ttu-id="80b66-129">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="80b66-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="80b66-130">-InitiateMaintenance</span><span class="sxs-lookup"><span data-stu-id="80b66-130">-InitiateMaintenance</span></span>
<span data-ttu-id="80b66-131">Rozpoczynanie konserwacji na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="80b66-131">Initiate Maintenance on the Virtual Machine</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: InitiateMaintenanceByName, InitiateMaintenanceInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b66-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="80b66-132">-Name</span></span>
<span data-ttu-id="80b66-133">Określa nazwę maszyny wirtualnej do ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="80b66-133">Specifies the name of the virtual machine to restart.</span></span>

```yaml
Type: String
Parameter Sets: RestartByName, RedeployByName, InitiateMaintenanceByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b66-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="80b66-134">-Profile</span></span>
<span data-ttu-id="80b66-135">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80b66-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80b66-136">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="80b66-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80b66-137">-Deploy</span><span class="sxs-lookup"><span data-stu-id="80b66-137">-Redeploy</span></span>
<span data-ttu-id="80b66-138">Wskazuje, że polecenie cmdlet powoduje ponowne wdrożenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="80b66-138">Indicates that the cmdlet redeploys the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployByName, RedeployInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b66-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="80b66-139">-ServiceName</span></span>
<span data-ttu-id="80b66-140">Określa nazwę usługi platformy Azure zawierającej maszynę wirtualną do ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="80b66-140">Specifies the name of the Azure service that contains the virtual machine to restart.</span></span>

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

### <span data-ttu-id="80b66-141">-VM</span><span class="sxs-lookup"><span data-stu-id="80b66-141">-VM</span></span>
<span data-ttu-id="80b66-142">Określa obiekt maszyny wirtualnej identyfikujący maszynę wirtualną do ponownego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="80b66-142">Specifies a virtual machine object that identifies the virtual machine to restart.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: RestartInput, RedeployInput, InitiateMaintenanceInput
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80b66-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b66-143">CommonParameters</span></span>
<span data-ttu-id="80b66-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b66-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b66-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b66-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b66-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80b66-146">INPUTS</span></span>

## <span data-ttu-id="80b66-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80b66-147">OUTPUTS</span></span>

## <span data-ttu-id="80b66-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80b66-148">NOTES</span></span>

## <span data-ttu-id="80b66-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80b66-149">RELATED LINKS</span></span>

[<span data-ttu-id="80b66-150">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="80b66-150">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="80b66-151">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="80b66-151">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="80b66-152">Start — AzureVM</span><span class="sxs-lookup"><span data-stu-id="80b66-152">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="80b66-153">Zatrzymaj — AzureVM</span><span class="sxs-lookup"><span data-stu-id="80b66-153">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="80b66-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="80b66-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


