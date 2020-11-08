---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054903"
---
# <span data-ttu-id="78132-101">Test-AzureName</span><span class="sxs-lookup"><span data-stu-id="78132-101">Test-AzureName</span></span>

## <span data-ttu-id="78132-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78132-102">SYNOPSIS</span></span>
<span data-ttu-id="78132-103">Sprawdza, czy istnieje nazwa obszaru nazw usługi w chmurze platformy Microsoft Azure, nazwa usługi Storage lub Magistrala usług.</span><span class="sxs-lookup"><span data-stu-id="78132-103">Tests whether a Microsoft Azure cloud service name, storage service name or service bus namespace name exists or not.</span></span>

## <span data-ttu-id="78132-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78132-104">SYNTAX</span></span>

### <span data-ttu-id="78132-105">Służby</span><span class="sxs-lookup"><span data-stu-id="78132-105">Service</span></span>
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="78132-106">Chowan</span><span class="sxs-lookup"><span data-stu-id="78132-106">Storage</span></span>
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="78132-107">ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="78132-107">ServiceBusNamespace</span></span>
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="78132-108">Firmy</span><span class="sxs-lookup"><span data-stu-id="78132-108">Website</span></span>
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="78132-109">Opis</span><span class="sxs-lookup"><span data-stu-id="78132-109">DESCRIPTION</span></span>
<span data-ttu-id="78132-110">Jeśli nazwa istnieje, polecenie cmdlet zwraca $True.</span><span class="sxs-lookup"><span data-stu-id="78132-110">If the name exists, the cmdlet returns $True.</span></span>
<span data-ttu-id="78132-111">Jeśli ta nazwa nie istnieje, zwracana jest $False.</span><span class="sxs-lookup"><span data-stu-id="78132-111">If the name does not exist, it returns $False.</span></span>

## <span data-ttu-id="78132-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78132-112">EXAMPLES</span></span>

### <span data-ttu-id="78132-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="78132-113">Example 1</span></span>
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

<span data-ttu-id="78132-114">To polecenie umożliwia sprawdzenie, czy nazwa "MyNameService1" jest istniejącą nazwą usługi w chmurze platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="78132-114">This command tests to see if the "MyNameService1" is an existing Microsoft Azure cloud service name.</span></span>

### <span data-ttu-id="78132-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="78132-115">Example 2</span></span>
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

<span data-ttu-id="78132-116">To polecenie sprawdza, czy nazwa "mystorename1" jest istniejącą nazwą usługi magazynu platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="78132-116">This command tests to see if the "mystorename1" is an existing Microsoft Azure storage service name.</span></span>

### <span data-ttu-id="78132-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="78132-117">Example 3</span></span>
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

<span data-ttu-id="78132-118">To polecenie sprawdza, czy "Moja przestrzeń nazw" jest istniejącą nazwą przestrzeni nazw usługi Microsoft Azure Service Bus.</span><span class="sxs-lookup"><span data-stu-id="78132-118">This command tests to see if the "mynamespace" is an existing Microsoft Azure service bus namespace name.</span></span>

## <span data-ttu-id="78132-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78132-119">PARAMETERS</span></span>

### <span data-ttu-id="78132-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78132-120">-Name</span></span>
<span data-ttu-id="78132-121">Określa nazwę konta usługi lub magazynu do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="78132-121">Specifies the name of the service or storage account to test.</span></span>

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

### <span data-ttu-id="78132-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="78132-122">-Profile</span></span>
<span data-ttu-id="78132-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78132-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="78132-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="78132-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="78132-125">-Service</span><span class="sxs-lookup"><span data-stu-id="78132-125">-Service</span></span>
<span data-ttu-id="78132-126">Określa, że należy przetestować istniejące konto usługi.</span><span class="sxs-lookup"><span data-stu-id="78132-126">Specifies to test for an existing service account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78132-127">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="78132-127">-ServiceBusNamespace</span></span>
<span data-ttu-id="78132-128">Określa, że należy przetestować istniejący obszar nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="78132-128">Specifies to test for an existing service bus namespace.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78132-129">-Storage</span><span class="sxs-lookup"><span data-stu-id="78132-129">-Storage</span></span>
<span data-ttu-id="78132-130">Określa, że należy przetestować istniejące konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="78132-130">Specifies to test for an existing storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78132-131">-Witryna sieci Web</span><span class="sxs-lookup"><span data-stu-id="78132-131">-Website</span></span>
<span data-ttu-id="78132-132">Określa, że należy testować istniejącą witrynę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="78132-132">Specifies to test for an existing website.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78132-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78132-133">CommonParameters</span></span>
<span data-ttu-id="78132-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78132-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78132-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78132-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78132-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78132-136">INPUTS</span></span>

## <span data-ttu-id="78132-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78132-137">OUTPUTS</span></span>

## <span data-ttu-id="78132-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78132-138">NOTES</span></span>
* <span data-ttu-id="78132-139">węzły — dev, php — dev, Python — dev</span><span class="sxs-lookup"><span data-stu-id="78132-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="78132-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78132-140">RELATED LINKS</span></span>

