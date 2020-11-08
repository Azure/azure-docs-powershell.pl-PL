---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054707"
---
# <span data-ttu-id="4c137-101">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4c137-101">Stop-AzureVM</span></span>

## <span data-ttu-id="4c137-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c137-102">SYNOPSIS</span></span>
<span data-ttu-id="4c137-103">Zamykanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4c137-103">Shuts down an Azure virtual machine.</span></span>

## <span data-ttu-id="4c137-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c137-104">SYNTAX</span></span>

### <span data-ttu-id="4c137-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4c137-105">ByName (Default)</span></span>
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4c137-106">Wprowadzone</span><span class="sxs-lookup"><span data-stu-id="4c137-106">Input</span></span>
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c137-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4c137-107">DESCRIPTION</span></span>
<span data-ttu-id="4c137-108">Polecenie cmdlet **stop-AzureVM** zamyka maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="4c137-108">The **Stop-AzureVM** cmdlet shuts down a virtual machine.</span></span>

## <span data-ttu-id="4c137-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c137-109">EXAMPLES</span></span>

### <span data-ttu-id="4c137-110">Przykład 1: zamykanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4c137-110">Example 1: Shut down a virtual machine</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

<span data-ttu-id="4c137-111">To polecenie zamyka maszynę wirtualną, którą zawiera określona usługa.</span><span class="sxs-lookup"><span data-stu-id="4c137-111">This command shuts down a virtual machine that the specified service contains.</span></span>

### <span data-ttu-id="4c137-112">Przykład 2: zamykanie maszyny wirtualnej za pomocą obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4c137-112">Example 2: Shut down a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

<span data-ttu-id="4c137-113">To polecenie zamyka maszynę wirtualną, którą określona usługa zawiera, przy użyciu obiektu maszyna wirtualna, który zwraca **-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="4c137-113">This command shuts down a virtual machine that the specified service contains, by using the virtual machine object that **Get-AzureVM** returns.</span></span>

### <span data-ttu-id="4c137-114">Przykład 3: zamykanie maszyny wirtualnej i zachowywanie zainicjowanej obsługi maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="4c137-114">Example 3: Shut down a VM and keep the VM provisioned</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

<span data-ttu-id="4c137-115">To polecenie zamyka maszynę wirtualną, którą określona usługa zawiera, i utrzymuje jej obsługę administracyjną.</span><span class="sxs-lookup"><span data-stu-id="4c137-115">This command shuts down a virtual machine that the specified service contains, and keeps it provisioned.</span></span>

### <span data-ttu-id="4c137-116">Przykład 4: zamykanie maszyny wirtualnej i Zezwalanie na przydział ostatniej maszyny wirtualnej we wdrożeniu</span><span class="sxs-lookup"><span data-stu-id="4c137-116">Example 4: Shut down a VM and allow deallocation of the last VM in the deployment</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

<span data-ttu-id="4c137-117">To polecenie zamyka maszynę wirtualną, którą określona usługa zawiera i zezwala na oddzielenie ostatniej maszyny wirtualnej we wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="4c137-117">This command shuts down a virtual machine that the specified service contains and allows deallocation of the last virtual machine in the deployment.</span></span>

### <span data-ttu-id="4c137-118">Przykład 5: zamykanie wielu maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="4c137-118">Example 5: Shut down multiple VMs</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

<span data-ttu-id="4c137-119">To polecenie zamyka wiele maszyn wirtualnych, które zawiera określona usługa.</span><span class="sxs-lookup"><span data-stu-id="4c137-119">This command shuts down multiple virtual machines that the specified service contains.</span></span>

## <span data-ttu-id="4c137-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c137-120">PARAMETERS</span></span>

### <span data-ttu-id="4c137-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4c137-121">-Force</span></span>
<span data-ttu-id="4c137-122">Określa, czy należy zezwolić na oddzielenie ostatniej maszyny wirtualnej we wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="4c137-122">Specifies whether to allow the deallocation of the last virtual machine in a deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c137-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4c137-123">-InformationAction</span></span>
<span data-ttu-id="4c137-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="4c137-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4c137-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4c137-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4c137-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="4c137-126">Continue</span></span>
- <span data-ttu-id="4c137-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="4c137-127">Ignore</span></span>
- <span data-ttu-id="4c137-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="4c137-128">Inquire</span></span>
- <span data-ttu-id="4c137-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4c137-129">SilentlyContinue</span></span>
- <span data-ttu-id="4c137-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="4c137-130">Stop</span></span>
- <span data-ttu-id="4c137-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="4c137-131">Suspend</span></span>

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

### <span data-ttu-id="4c137-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4c137-132">-InformationVariable</span></span>
<span data-ttu-id="4c137-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="4c137-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4c137-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c137-134">-Name</span></span>
<span data-ttu-id="4c137-135">Określa nazwę maszyny wirtualnej do zamknięcia.</span><span class="sxs-lookup"><span data-stu-id="4c137-135">Specifies the name of the virtual machine to shut down.</span></span>

<span data-ttu-id="4c137-136">Używanie znaku wieloznacznego do asynchronicznego zatrzymywania wielu maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="4c137-136">Use the wildcard character to stop multiple virtual machines asynchronously.</span></span>
<span data-ttu-id="4c137-137">W przypadku symboli wieloznacznych to polecenie cmdlet wywołuje operację role zamknięcia https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) zamiast operacji roli Shutdown https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx ( https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4c137-137">With a wildcard character, this cmdlet calls the Shutdown Roleshttps://msdn.microsoft.com/en-us/library/azure/dn469421.aspx operation (https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx), instead of the Shutdown Rolehttps://msdn.microsoft.com/en-us/library/azure/jj157195.aspx operation (https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx).</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c137-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="4c137-138">-Profile</span></span>
<span data-ttu-id="4c137-139">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c137-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c137-140">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4c137-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4c137-141">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4c137-141">-ServiceName</span></span>
<span data-ttu-id="4c137-142">Określa nazwę usługi platformy Azure zawierającej maszynę wirtualną do zamknięcia.</span><span class="sxs-lookup"><span data-stu-id="4c137-142">Specifies the name of the Azure service that contains the virtual machine to shut down.</span></span>

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

### <span data-ttu-id="4c137-143">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="4c137-143">-StayProvisioned</span></span>
<span data-ttu-id="4c137-144">Określa, że w tym poleceniu cmdlet jest zachowywana obsługa administracyjna maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4c137-144">Specifies that this cmdlet keeps the virtual machine provisioned.</span></span>

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

### <span data-ttu-id="4c137-145">-VM</span><span class="sxs-lookup"><span data-stu-id="4c137-145">-VM</span></span>
<span data-ttu-id="4c137-146">Określa obiekt maszyny wirtualnej wskazujący, że maszyna wirtualna zostanie zamknięta.</span><span class="sxs-lookup"><span data-stu-id="4c137-146">Specifies a virtual machine object that identifies the virtual machine to shut down.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c137-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c137-147">CommonParameters</span></span>
<span data-ttu-id="4c137-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c137-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c137-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c137-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c137-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c137-150">INPUTS</span></span>

## <span data-ttu-id="4c137-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c137-151">OUTPUTS</span></span>

## <span data-ttu-id="4c137-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c137-152">NOTES</span></span>

## <span data-ttu-id="4c137-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c137-153">RELATED LINKS</span></span>

[<span data-ttu-id="4c137-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4c137-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="4c137-155">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="4c137-155">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="4c137-156">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4c137-156">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="4c137-157">Start — AzureVM</span><span class="sxs-lookup"><span data-stu-id="4c137-157">Start-AzureVM</span></span>](./Start-AzureVM.md)


