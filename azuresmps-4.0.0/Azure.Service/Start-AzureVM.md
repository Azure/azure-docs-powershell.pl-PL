---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C60F78AE-3803-4D9F-A4F3-EAA42052C0E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a0708ca37cdb2b700772da2fe9cb684b8b29a30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054737"
---
# <span data-ttu-id="44d00-101">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="44d00-101">Start-AzureVM</span></span>

## <span data-ttu-id="44d00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44d00-102">SYNOPSIS</span></span>
<span data-ttu-id="44d00-103">Rozpoczynanie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="44d00-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="44d00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44d00-104">SYNTAX</span></span>

### <span data-ttu-id="44d00-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="44d00-105">ByName (Default)</span></span>
```
Start-AzureVM [-Name] <String[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="44d00-106">Wprowadzone</span><span class="sxs-lookup"><span data-stu-id="44d00-106">Input</span></span>
```
Start-AzureVM -VM <IPersistentVM[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="44d00-107">Opis</span><span class="sxs-lookup"><span data-stu-id="44d00-107">DESCRIPTION</span></span>
<span data-ttu-id="44d00-108">Polecenie cmdlet **Start-AzureVM** żąda uruchomienia maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="44d00-108">The **Start-AzureVM** cmdlet requests the start of an Azure virtual machine.</span></span>

## <span data-ttu-id="44d00-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44d00-109">EXAMPLES</span></span>

### <span data-ttu-id="44d00-110">Przykład 1. uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="44d00-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04"
```

<span data-ttu-id="44d00-111">To polecenie umożliwia uruchomienie maszyny wirtualnej o nazwie VirtualMachine04 uruchomionej w usłudze Azure o nazwie ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="44d00-111">This command starts the virtual machine named VirtualMachine04 that runs in the Azure service named ContosoService03.</span></span>

### <span data-ttu-id="44d00-112">Przykład 2: Uruchamianie maszyny wirtualnej za pomocą obiektu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="44d00-112">Example 2: Start a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "DatabaseServer" | Start-AzureVM
```

<span data-ttu-id="44d00-113">To polecenie pobiera obiekt maszyny wirtualnej dla maszyny wirtualnej, której nazwa to DatabaseServer, a następnie żąda jej rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="44d00-113">This command retrieves the virtual machine object for the virtual machine whose name is DatabaseServer, and then requests to start it.</span></span>

## <span data-ttu-id="44d00-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44d00-114">PARAMETERS</span></span>

### <span data-ttu-id="44d00-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="44d00-115">-InformationAction</span></span>
<span data-ttu-id="44d00-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="44d00-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="44d00-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="44d00-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="44d00-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="44d00-118">Continue</span></span>
- <span data-ttu-id="44d00-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="44d00-119">Ignore</span></span>
- <span data-ttu-id="44d00-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="44d00-120">Inquire</span></span>
- <span data-ttu-id="44d00-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="44d00-121">SilentlyContinue</span></span>
- <span data-ttu-id="44d00-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="44d00-122">Stop</span></span>
- <span data-ttu-id="44d00-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="44d00-123">Suspend</span></span>

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

### <span data-ttu-id="44d00-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="44d00-124">-InformationVariable</span></span>
<span data-ttu-id="44d00-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="44d00-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="44d00-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44d00-126">-Name</span></span>
<span data-ttu-id="44d00-127">Określa nazwę maszyny wirtualnej, która ma zostać uruchomiona.</span><span class="sxs-lookup"><span data-stu-id="44d00-127">Specifies the name of the virtual machine to start.</span></span>

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

### <span data-ttu-id="44d00-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="44d00-128">-Profile</span></span>
<span data-ttu-id="44d00-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44d00-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44d00-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="44d00-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44d00-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="44d00-131">-ServiceName</span></span>
<span data-ttu-id="44d00-132">Określa nazwę usługi platformy Azure zawierającej maszynę wirtualną do uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="44d00-132">Specifies the name of the Azure service that contains the virtual machine to start.</span></span>

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

### <span data-ttu-id="44d00-133">-VM</span><span class="sxs-lookup"><span data-stu-id="44d00-133">-VM</span></span>
<span data-ttu-id="44d00-134">Określa obiekt maszyny wirtualnej wskazujący, że maszyna wirtualna jest uruchamiana.</span><span class="sxs-lookup"><span data-stu-id="44d00-134">Specifies a virtual machine object that identifies the virtual machine to start.</span></span>

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

### <span data-ttu-id="44d00-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d00-135">CommonParameters</span></span>
<span data-ttu-id="44d00-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44d00-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44d00-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44d00-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d00-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44d00-138">INPUTS</span></span>

## <span data-ttu-id="44d00-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44d00-139">OUTPUTS</span></span>

## <span data-ttu-id="44d00-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44d00-140">NOTES</span></span>

## <span data-ttu-id="44d00-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44d00-141">RELATED LINKS</span></span>

[<span data-ttu-id="44d00-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="44d00-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="44d00-143">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="44d00-143">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="44d00-144">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="44d00-144">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="44d00-145">Zatrzymaj — AzureVM</span><span class="sxs-lookup"><span data-stu-id="44d00-145">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="44d00-146">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="44d00-146">Update-AzureVM</span></span>](./Update-AzureVM.md)


