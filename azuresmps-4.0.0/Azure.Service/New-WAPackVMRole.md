---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6617AA59-CDD1-4BA9-84A7-F3914BF1D4B7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14e201dc916f15b63b0e825f4ca2e37015aaa9bc
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061860"
---
# <span data-ttu-id="beb61-101">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="beb61-101">New-WAPackVMRole</span></span>

## <span data-ttu-id="beb61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="beb61-102">SYNOPSIS</span></span>
<span data-ttu-id="beb61-103">Tworzy rolę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="beb61-103">Creates a virtual machine role.</span></span>

## <span data-ttu-id="beb61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="beb61-104">SYNTAX</span></span>

### <span data-ttu-id="beb61-105">QuickCreate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="beb61-105">QuickCreate (Default)</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="beb61-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="beb61-106">FromCloudService</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 -CloudService <CloudService> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="beb61-107">Opis</span><span class="sxs-lookup"><span data-stu-id="beb61-107">DESCRIPTION</span></span>
<span data-ttu-id="beb61-108">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="beb61-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="beb61-109">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="beb61-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="beb61-110">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="beb61-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="beb61-111">Polecenie cmdlet **New-WAPackVMRole** tworzy rolę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="beb61-111">The **New-WAPackVMRole** cmdlet creates a virtual machine role.</span></span>

## <span data-ttu-id="beb61-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="beb61-112">EXAMPLES</span></span>

### <span data-ttu-id="beb61-113">Przykład 1. Tworzenie roli maszyny wirtualnej (emulowanie zachowania WAP)</span><span class="sxs-lookup"><span data-stu-id="beb61-113">Example 1: Create a virtual machine role (emulating WAP behavior)</span></span>
```
PS C:\> New-WAPackVMRole -Name "ContosoVMRole01" -Label "ContosoVMRoleLabel01" -ResourceDefinition $resdef
```

<span data-ttu-id="beb61-114">Ponieważ nie określamy żadnej usługi w chmurze (emulowanej funkcji WAP), polecenie utworzy dla nas usługę w chmurze, która będzie mieć taką samą nazwę jak rola maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="beb61-114">Since we do not specify any cloud service (emulating WAP behavior), the command will create a cloud service for us which will have the same name as the virtual machine role.</span></span>
<span data-ttu-id="beb61-115">W tym przypadku następujące polecenie utworzy rolę maszyny wirtualnej z nazwą ContosoVMRole01, etykietą ContosoVMRoleLabel01.</span><span class="sxs-lookup"><span data-stu-id="beb61-115">In this case, the following command will create a virtual machine role with the name ContosoVMRole01, label ContosoVMRoleLabel01.</span></span>
<span data-ttu-id="beb61-116">Pamiętaj, że definicja zasobu, która jest używana tutaj, musi być utworzona ręcznie, chociaż program PowerShell.</span><span class="sxs-lookup"><span data-stu-id="beb61-116">Note that the resource definition being used here has to be manually created though PowerShell.</span></span>

## <span data-ttu-id="beb61-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="beb61-117">PARAMETERS</span></span>

### <span data-ttu-id="beb61-118">-CloudService</span><span class="sxs-lookup"><span data-stu-id="beb61-118">-CloudService</span></span>
<span data-ttu-id="beb61-119">Określa usługę w chmurze dla roli maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="beb61-119">Specifies a cloud service for the virtual machine role.</span></span>

```yaml
Type: CloudService
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beb61-120">-Label</span><span class="sxs-lookup"><span data-stu-id="beb61-120">-Label</span></span>
<span data-ttu-id="beb61-121">Określa etykietę roli maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="beb61-121">Specifies a label for the virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beb61-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="beb61-122">-Name</span></span>
<span data-ttu-id="beb61-123">Określa nazwę roli maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="beb61-123">Specifies a name for the virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beb61-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="beb61-124">-Profile</span></span>
<span data-ttu-id="beb61-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="beb61-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="beb61-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="beb61-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="beb61-127">-ResourceDefinition</span><span class="sxs-lookup"><span data-stu-id="beb61-127">-ResourceDefinition</span></span>
<span data-ttu-id="beb61-128">Określa definicję zasobu dla roli maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="beb61-128">Specifies a resource definition for the virtual machine role.</span></span>

```yaml
Type: VMRoleResourceDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beb61-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beb61-129">CommonParameters</span></span>
<span data-ttu-id="beb61-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beb61-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beb61-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beb61-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beb61-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="beb61-132">INPUTS</span></span>

## <span data-ttu-id="beb61-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="beb61-133">OUTPUTS</span></span>

## <span data-ttu-id="beb61-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="beb61-134">NOTES</span></span>

## <span data-ttu-id="beb61-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="beb61-135">RELATED LINKS</span></span>

[<span data-ttu-id="beb61-136">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="beb61-136">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="beb61-137">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="beb61-137">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="beb61-138">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="beb61-138">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


