---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 78099E89-63C9-4019-A4ED-EF37D2383A09
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23e6165e50c227320875fa70e97d63b0cdd78781
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054643"
---
# <span data-ttu-id="2140b-101">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2140b-101">Export-AzureVM</span></span>

## <span data-ttu-id="2140b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2140b-102">SYNOPSIS</span></span>
<span data-ttu-id="2140b-103">Eksportuje stan maszyny wirtualnej platformy Azure do pliku.</span><span class="sxs-lookup"><span data-stu-id="2140b-103">Exports an Azure virtual machine state to a file.</span></span>

## <span data-ttu-id="2140b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2140b-104">SYNTAX</span></span>

```
Export-AzureVM [-ServiceName] <String> [-Name] <String> [-Path] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2140b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2140b-105">DESCRIPTION</span></span>
<span data-ttu-id="2140b-106">Polecenie cmdlet **Export-AzureVM** eksportuje stan maszyny wirtualnej do pliku XML.</span><span class="sxs-lookup"><span data-stu-id="2140b-106">The **Export-AzureVM** cmdlet exports the state of a virtual machine to an .xml file.</span></span>

<span data-ttu-id="2140b-107">Uruchomienie programu **Export-AzureVM** , a następnie polecenie **Remove-AzureVM** , a następnie polecenie **Import-AzureVM** w celu ponownego utworzenia maszyny wirtualnej może spowodować, że wynikowy komputer wirtualny będzie miał inny adres IP niż oryginalny.</span><span class="sxs-lookup"><span data-stu-id="2140b-107">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="2140b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2140b-108">EXAMPLES</span></span>

### <span data-ttu-id="2140b-109">Przykład 1: eksportowanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2140b-109">Example 1: Export a virtual machine</span></span>
```
PS C:\> Export-AzureVM -ServiceName "ContosoService" -Name "ContosoRole06" -Path "C:\vms\VMstate.xml"
```

<span data-ttu-id="2140b-110">To polecenie eksportuje stan określonej maszyny wirtualnej do pliku VMstate.xml.</span><span class="sxs-lookup"><span data-stu-id="2140b-110">This command exports the state of the specified virtual machine to the VMstate.xml file.</span></span>

## <span data-ttu-id="2140b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2140b-111">PARAMETERS</span></span>

### <span data-ttu-id="2140b-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2140b-112">-InformationAction</span></span>
<span data-ttu-id="2140b-113">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="2140b-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2140b-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2140b-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2140b-115">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="2140b-115">Continue</span></span>
- <span data-ttu-id="2140b-116">Ignorować</span><span class="sxs-lookup"><span data-stu-id="2140b-116">Ignore</span></span>
- <span data-ttu-id="2140b-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="2140b-117">Inquire</span></span>
- <span data-ttu-id="2140b-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2140b-118">SilentlyContinue</span></span>
- <span data-ttu-id="2140b-119">Przestaw</span><span class="sxs-lookup"><span data-stu-id="2140b-119">Stop</span></span>
- <span data-ttu-id="2140b-120">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="2140b-120">Suspend</span></span>

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

### <span data-ttu-id="2140b-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2140b-121">-InformationVariable</span></span>
<span data-ttu-id="2140b-122">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="2140b-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2140b-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2140b-123">-Name</span></span>
<span data-ttu-id="2140b-124">Określa nazwę maszyny wirtualnej, dla której jest eksportowany stan polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2140b-124">Specifies the name of the virtual machine for which this cmdlet exports state.</span></span>

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

### <span data-ttu-id="2140b-125">-Path</span><span class="sxs-lookup"><span data-stu-id="2140b-125">-Path</span></span>
<span data-ttu-id="2140b-126">Określa ścieżkę i nazwę pliku, w którym to polecenie cmdlet zapisuje stan maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2140b-126">Specifies the path and file name to which this cmdlet saves the virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2140b-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="2140b-127">-Profile</span></span>
<span data-ttu-id="2140b-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2140b-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2140b-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2140b-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2140b-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2140b-130">-ServiceName</span></span>
<span data-ttu-id="2140b-131">Określa nazwę usługi platformy Azure obsługującej maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="2140b-131">Specifies the name of the Azure service that hosts the virtual machine.</span></span>

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

### <span data-ttu-id="2140b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2140b-132">CommonParameters</span></span>
<span data-ttu-id="2140b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2140b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2140b-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2140b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2140b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2140b-135">INPUTS</span></span>

## <span data-ttu-id="2140b-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2140b-136">OUTPUTS</span></span>

## <span data-ttu-id="2140b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2140b-137">NOTES</span></span>

## <span data-ttu-id="2140b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2140b-138">RELATED LINKS</span></span>

[<span data-ttu-id="2140b-139">Import — AzureVM</span><span class="sxs-lookup"><span data-stu-id="2140b-139">Import-AzureVM</span></span>](./Import-AzureVM.md)


