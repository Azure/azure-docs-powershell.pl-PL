---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7EB9FE4-BDEB-43A5-B6D3-FEAB16BC2711
online version: ''
schema: 2.0.0
ms.openlocfilehash: 388277115281cbbacfb634ebdac5cdd9aa86b709
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061884"
---
# <span data-ttu-id="c9fec-101">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="c9fec-101">Get-WAPackVMRole</span></span>

## <span data-ttu-id="c9fec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9fec-102">SYNOPSIS</span></span>

## <span data-ttu-id="c9fec-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9fec-103">SYNTAX</span></span>

### <span data-ttu-id="c9fec-104">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c9fec-104">Empty (Default)</span></span>
```
Get-WAPackVMRole [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c9fec-105">Odname</span><span class="sxs-lookup"><span data-stu-id="c9fec-105">FromName</span></span>
```
Get-WAPackVMRole -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c9fec-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="c9fec-106">FromCloudService</span></span>
```
Get-WAPackVMRole -Name <String> -CloudServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c9fec-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c9fec-107">DESCRIPTION</span></span>
<span data-ttu-id="c9fec-108">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="c9fec-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="c9fec-109">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c9fec-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c9fec-110">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c9fec-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="c9fec-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9fec-111">EXAMPLES</span></span>

### <span data-ttu-id="c9fec-112">Przykład 1: uzyskiwanie roli maszyny wirtualnej (utworzonej za pośrednictwem portalu)</span><span class="sxs-lookup"><span data-stu-id="c9fec-112">Example 1: Get a virtual machine role (created through the portal)</span></span>
```
PS C:\> Get-WAPackVMRole -Name "ContosoVMRole01"
```

<span data-ttu-id="c9fec-113">To polecenie pobiera rolę maszyny wirtualnej utworzoną za pośrednictwem portalu o nazwie ContosoVMRole01.</span><span class="sxs-lookup"><span data-stu-id="c9fec-113">This command gets a virtual machine role which has been created through the portal named ContosoVMRole01.</span></span>

### <span data-ttu-id="c9fec-114">Przykład 2: uzyskiwanie roli maszyny wirtualnej za pomocą nazwy i nazwy usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="c9fec-114">Example 2: Get a virtual machine role by using a name and a cloud service name</span></span>
```
PS C:\> Get-WAPackVMRole -CloudServiceName "ContosoCloudService01" -Name "ContosoVMRole02"
```

<span data-ttu-id="c9fec-115">To polecenie uzyskuje rolę maszyny wirtualnej o nazwie ContosoVMRole02, która jest podstawiona na usługę w chmurze o nazwie ContosoCloudService01.</span><span class="sxs-lookup"><span data-stu-id="c9fec-115">This command gets a virtual machine role named ContosoVMRole02 which stand on a cloud service named ContosoCloudService01.</span></span>

### <span data-ttu-id="c9fec-116">Przykład 3: pobieranie całej roli maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="c9fec-116">Example 3: Get all virtual machine role</span></span>
```
PS C:\> Get-WAPackVMRole
```

<span data-ttu-id="c9fec-117">To polecenie pobiera całą istniejącą rolę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c9fec-117">This command gets all existing virtual machine role.</span></span>

## <span data-ttu-id="c9fec-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9fec-118">PARAMETERS</span></span>

### <span data-ttu-id="c9fec-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="c9fec-119">-CloudServiceName</span></span>
<span data-ttu-id="c9fec-120">Określa nazwę usługi w chmurze dla roli maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="c9fec-120">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9fec-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9fec-121">-Name</span></span>
<span data-ttu-id="c9fec-122">Określa nazwę roli maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c9fec-122">Specifies the name of a virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromName, FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9fec-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="c9fec-123">-Profile</span></span>
<span data-ttu-id="c9fec-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9fec-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c9fec-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c9fec-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9fec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9fec-126">CommonParameters</span></span>
<span data-ttu-id="c9fec-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9fec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9fec-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9fec-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9fec-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9fec-129">INPUTS</span></span>

## <span data-ttu-id="c9fec-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9fec-130">OUTPUTS</span></span>

## <span data-ttu-id="c9fec-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9fec-131">NOTES</span></span>

## <span data-ttu-id="c9fec-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9fec-132">RELATED LINKS</span></span>

[<span data-ttu-id="c9fec-133">Nowe — WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="c9fec-133">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="c9fec-134">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="c9fec-134">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="c9fec-135">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="c9fec-135">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


