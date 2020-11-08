---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054785"
---
# <span data-ttu-id="db6f1-101">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="db6f1-101">Set-AzureServiceProject</span></span>

## <span data-ttu-id="db6f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db6f1-102">SYNOPSIS</span></span>
<span data-ttu-id="db6f1-103">Ustawia domyślną lokalizację, subskrypcję, gniazdo i konto magazynu dla bieżącej usługi.</span><span class="sxs-lookup"><span data-stu-id="db6f1-103">Sets default location, subscription, slot, and storage account for the current service.</span></span>

## <span data-ttu-id="db6f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db6f1-104">SYNTAX</span></span>

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="db6f1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="db6f1-105">DESCRIPTION</span></span>
<span data-ttu-id="db6f1-106">Polecenie cmdlet **Set-AzureServiceProject** ustawia lokalizację wdrożenia, gniazdo, konto magazynu i abonament dla bieżącej usługi.</span><span class="sxs-lookup"><span data-stu-id="db6f1-106">The **Set-AzureServiceProject** cmdlet sets the deployment location, slot, storage account, and subscription for the current service.</span></span>
<span data-ttu-id="db6f1-107">Te wartości są używane podczas publikowania usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="db6f1-107">These values are used whenever the service is published to the cloud.</span></span>

## <span data-ttu-id="db6f1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db6f1-108">EXAMPLES</span></span>

### <span data-ttu-id="db6f1-109">Przykład 1: Ustawienia podstawowe</span><span class="sxs-lookup"><span data-stu-id="db6f1-109">Example 1: Basic settings</span></span>
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

<span data-ttu-id="db6f1-110">Ustawia lokalizację wdrożenia usługi na Północno-środkowe region w Stanach Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="db6f1-110">Sets the deployment location for the service to the North Central US region.</span></span>
<span data-ttu-id="db6f1-111">Ustawia miejsce wdrożenia na produkcję.</span><span class="sxs-lookup"><span data-stu-id="db6f1-111">Sets the deployment slot to Production.</span></span> <span data-ttu-id="db6f1-112">Ustawia konto magazynu, które będzie używane do przemieszczenia definicji usługi na myStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="db6f1-112">Sets the storage account that will be used to stage the service definition to myStorageAccount.</span></span>
<span data-ttu-id="db6f1-113">Ustawia subskrypcję, która będzie hostem usługi na stronie Moja subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="db6f1-113">Sets the subscription that will host the service to mySubscription.</span></span>
<span data-ttu-id="db6f1-114">Po opublikowaniu usługi w chmurze będzie ona hostowana w centrum danych w regionie północ w Stanach Zjednoczonych, a to spowoduje zaktualizowanie miejsca wdrożenia, a następnie użyje określonego konta abonamentu i magazynu.</span><span class="sxs-lookup"><span data-stu-id="db6f1-114">Whenever the service is published to the cloud, it will be hosted in a data center in the North Central US region, it will update the deployment slot, and it will use the specified subscription and storage account.</span></span>

## <span data-ttu-id="db6f1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db6f1-115">PARAMETERS</span></span>

### <span data-ttu-id="db6f1-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="db6f1-116">-Location</span></span>
<span data-ttu-id="db6f1-117">Region, w którym usługa będzie hostowana.</span><span class="sxs-lookup"><span data-stu-id="db6f1-117">The region in which the service will be hosted.</span></span>
<span data-ttu-id="db6f1-118">Ta wartość jest używana podczas publikowania usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="db6f1-118">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="db6f1-119">Możliwe wartości: wszędzie tam, gdzie w Europie, na całym świecie, w Stanach Zjednoczonych, Wschodniej, Wschodniej, północno-zachodnim świecie, na północno-wschodnim świecie, w USA, Azji Południowo – Wschodniej, Europa Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="db6f1-119">Possible values are: Anywhere Asia, Anywhere Europe, Anywhere US, East Asia, East US, North Central US, North Europe, South Central US, Southeast Asia, West Europe, West US.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db6f1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db6f1-120">-PassThru</span></span>
<span data-ttu-id="db6f1-121">Wskazuje, że to polecenie cmdlet zwraca obiekt reprezentujący element, na którym działa.</span><span class="sxs-lookup"><span data-stu-id="db6f1-121">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="db6f1-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="db6f1-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6f1-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="db6f1-123">-Profile</span></span>
<span data-ttu-id="db6f1-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db6f1-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="db6f1-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="db6f1-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="db6f1-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="db6f1-126">-Slot</span></span>
<span data-ttu-id="db6f1-127">Miejsce (produkcja lub przemieszczanie), w którym usługa będzie hostowana.</span><span class="sxs-lookup"><span data-stu-id="db6f1-127">The slot (production or staging) in which the service will be hosted.</span></span>
<span data-ttu-id="db6f1-128">Ta wartość jest używana podczas publikowania usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="db6f1-128">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="db6f1-129">Możliwe wartości: produkcja, przemieszczanie.</span><span class="sxs-lookup"><span data-stu-id="db6f1-129">Possible values are: Production, Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db6f1-130">-Storage</span><span class="sxs-lookup"><span data-stu-id="db6f1-130">-Storage</span></span>
<span data-ttu-id="db6f1-131">Konto magazynu, które ma być używane podczas przekazywania pakietu usługi do chmury.</span><span class="sxs-lookup"><span data-stu-id="db6f1-131">The storage account to be used when uploading the service package to the cloud.</span></span>
<span data-ttu-id="db6f1-132">Jeśli konto magazynu nie istnieje, zostanie utworzone po opublikowaniu usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="db6f1-132">If the storage account doesn't exist, it will be created when the service is published to the cloud.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db6f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6f1-133">CommonParameters</span></span>
<span data-ttu-id="db6f1-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6f1-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6f1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6f1-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db6f1-136">INPUTS</span></span>

## <span data-ttu-id="db6f1-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db6f1-137">OUTPUTS</span></span>

## <span data-ttu-id="db6f1-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db6f1-138">NOTES</span></span>
* <span data-ttu-id="db6f1-139">węzły — dev, php — dev, Python — dev</span><span class="sxs-lookup"><span data-stu-id="db6f1-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="db6f1-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db6f1-140">RELATED LINKS</span></span>

[<span data-ttu-id="db6f1-141">Nowe — AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="db6f1-141">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="db6f1-142">Publikowanie — AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="db6f1-142">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="db6f1-143">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="db6f1-143">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


